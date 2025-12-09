---

title: "Blog Vận hành AWS Cloud – Quản lý AWS Config Rules with Remediation"
date: "2025-05-05"
weight: 1
chapter: false
pre: " <b> 3.2. </b> "
----------------------

# **Manage Custom AWS Config Rules with Remediation Using AWS Config Conformance Pack**

**Tác giả:** Eswar Sesha Sai Kamineni, Ravindra Kori, Samrat Lamichhane, and Prathik Chintha
**Ngày:** 05 MAY 2025
**Chuyên mục:** AWS Command Line Interface, AWS Config, Centralized operations management, Configuration, compliance, and auditing, Management Tools

---

# **Introduction**

Organizations face unique compliance requirements across their AWS resources and accounts. While AWS Config provides managed rules, many organizations need custom rules and automated remediation capabilities that can scale across their AWS Organization. This blog post demonstrates how to use AWS Config custom conformance pack to deploy and manage custom rules with remediation actions across organization-wide while maintaining centralized control.

---

# **Solution Overview**

This solution implements a centralized compliance framework using:

* AWS Config custom rules with automated remediation
* Conformance packs for organization-wide deployment
* AWS Lambda functions for evaluation
* AWS Systems Manager for remediation

![Figure 1: Architecture](/images/Blog/blog2_1.png)

The AWS Config custom rule configured in member accounts, invokes the evaluation Lambda function residing in the AWS delegated administrator account.
The evaluation Lambda function residing in delegated admin account assesses target resources (e.g. AWS EC2 Security Group) against predefined compliance criteria and updates the evaluation result as either “Compliant” or “Non-Compliant” in AWS Config member account.
Upon detection of non-compliant resources in the member account, the AWS Config rule will automatically trigger a remediation workflow through AWS Systems Manager Automation document.
The AWS Systems Manager Automation document will trigger a Lambda function which is maintained in the delegated admin account, executes the defined actions to bring resources into compliant.

---

# **Key Components**

There are two key components, delegated admin and member accounts

## **Delegated admin account stores and manages:**

* Lambda functions for rule evaluation and remediation
* AWS Config custom rule logic
* Systems Manager Automation runbooks

## **Member Accounts:**

* AWS Config enabled
* Cross-account access for centralized management

In this blog post, we will demonstrate the solution by implementing a compliance control that checks for AWS EC2 Security group inbound rules. The rule identifies and remediates security groups allowing access from CIDR blocks larger than /16 (e.g., 10.0.0.0/10 or 10.0.0.0/1).

---

# **Implementation Guide**

## **Prerequisites**

* Verify access in AWS delegated admin and member accounts.
* Enable AWS Config in delegated admin and member accounts either through AWS CLI or AWS Management console
* Make a note of AWS Delegated admin account ID.

---

## **Step 1: Deploy resources in the delegated admin account**

* Download the CloudFormation template from this link.
* Sign in to the AWS Management Console and navigate to the CloudFormation service.
* Choose Create stack > With new resources (standard).
* Under Specify template, choose Upload a template file.
* Select the downloaded template and choose Next.

The CloudFormation stack creates several interconnected components that work together to enable our compliance solution:

First, it deploys two essential Lambda functions:

* **ConformancePackSecurityGroup** function serves as our compliance evaluator, examining security group rules against our defined requirements.
* **AutomationSecurityGroupConformance** function handles remediation, automatically fixing any non-compliant resource configurations.

To support these functions, the stack creates three IAM roles with specific permissions:

* **ConformancePackSecurityGroupLambdaRole** enables security group evaluation
* **AutomationSecurityGroupConformanceLambdaRole** permits security group modifications
* **SSMDocumentRole** facilitates Systems Manager automation execution

Finally, it creates the **SecurityGroupAutomation SSMDocument** in Systems Manager, which defines our automated remediation workflows.

---

## **Step 2: Deploy cross-account IAM roles using CloudFormation StackSets**

* Download the CloudFormation StackSet template from this link.
* Follow the steps in the documentation to create StackSets.
* Enter AWS Delegated Admin Account ID in parameters.
* Deploy StackSet across AWS Organizational Units.

---

## **Step 3: Configure Lambda Permissions**

```bash
aws lambda add-permission \
  --function-name "ConformancePackSecurityGroupFunction" \
  --statement-id "AllowConfigCrossAccount" \
  --action "lambda:InvokeFunction" \
  --principal "config.amazonaws.com" \
  --source-account ${MEMBER_ACCOUNT_ID}
```

---

## **Step 4: Share AWS Systems Manager Automation Runbook**

```bash
aws ssm modify-document-permission \
  --name "SecurityGroupAutomationSSMDocument" \
  --permission-type Share \
  --account-ids-to-add "111111111111" "222222222222" "333333333333"
```

---

## **Step 5: Deploy the Conformance Pack**

```bash
aws configservice put-organization-conformance-pack \
    --organization-conformance-pack-name "SecurityGroupConformancePack" \
    --template-body file://SecurityGroupConformancePack.yaml \
    --delivery-s3-bucket YOUR-S3-BUCKET-NAME \
    --conformance-pack-input-parameters \
        ParameterName=ManagementAccountId,ParameterValue=YOUR-Management-ACCOUNT-ID
```

---

# **Testing the Solution**

To verify that the AWS Config Conformance Pack will detect and remediate the security group rule, let’s test it by creating a non-compliant security group and evaluating the automated remediation process.

First, create a test security group in a member account:

* Navigate to the EC2 console and create a new security group
* Add an inbound rule allowing SSH (port 22) from **10.0.0.0/8**
* Tag the security group appropriately for identification

![Figure 2: Non-compliant Security Group Inbound rule](/images/Blog/blog2_2.png)

Within few minutes of creation, AWS Config will evaluate this security group.

In the member account:

* Check the AWS Config console
* Evaluate the security group status change from “Compliant” to “Non-compliant”

![Figure 3: Conformance package identifying resources](/images/Blog/blog2_3.png)

In the delegated admin account:

* Review CloudWatch Logs for both Lambda functions
* Confirm the evaluation detected the non-compliant CIDR
* Verify the remediation action completed successfully

The solution should automatically detect and remove the CIDR range (10.0.0.0/8), maintaining only compliant rules (those with /16 or smaller CIDR blocks).

---

# **Cleanup**

* Delete the conformance pack
* Delete the CloudFormation Stack
* Empty and delete the S3 bucket used for the conformance pack delivery

---

# **Conclusion**

In this blog post, we demonstrated a solution for implementing organization-wide compliance using AWS Config conformance packs. By combining AWS Config, Lambda, Systems Manager, and AWS Organizations, we created a scalable framework that automatically detects and remediates security group misconfigurations across multiple AWS accounts. The solution showcases how to centrally manage custom compliance rules while maintaining automated remediation workflows.
