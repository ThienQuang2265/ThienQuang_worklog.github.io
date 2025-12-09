---
title: "Week 2 Worklog"
date: "2025-09-15"
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

**Week Duration: September 15 - September 21, 2025**

### Week 2 Objectives:

* Strengthen foundational understanding of cloud computing concepts.
* Learn the architecture and essential components of Amazon VPC (Virtual Private Cloud).
* Understand how traffic flows inside a VPC using subnets, route tables, NAT Gateway, and Internet Gateway.
* Gain a basic understanding of Amazon EC2, its features, and how to launch EC2 instances into a configured VPC.
* Practice hands-on configuration of networking components using AWS Console.

---

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | ---------------- | ------------------ |
| Monday | - Learned fundamental cloud computing concepts through video lessons | 09/15/2025 | 09/15/2025 | YouTube cloud basics playlist |
| Tuesday | - Participated in CloudDay event | 09/16/2025 | 09/16/2025 | — |
| Wednesday | - Practice configuring VPC and its components: subnets, route tables, IGW, NAT Gateway | 09/17/2025 | 09/17/2025 | https://000003.awsstudygroup.com/ |
| Thursday | - Study EC2 basics and learned how to launch an EC2 instance inside a VPC | 09/18/2025 | 09/18/2025 | https://000004.awsstudygroup.com/, YouTube EC2 tutorial |
| Friday | - Team meeting and decide on the final prioject | 09/19/2025 | 09/19/2025 | — |

---

### Week 2 Achievements:

#### **Cloud Fundamentals**

* Understood key cloud computing concepts:
  * What cloud infrastructure is.
  * Why elasticity and scalability help prevent websites or applications from crashing during spikes in demand.
  * Why cloud adoption is essential in a modern tech landscape where demand increases but not every organization can afford physical infrastructure.

---

#### **VPC (Virtual Private Cloud) Skills**

* Gained practical experience building a functional AWS VPC:
  * Created public and private subnets.
  * Learned how **CIDR blocks** define IP ranges in a VPC.
  * Attached an **Internet Gateway (IGW)** to provide internet access to public subnets.
  * Created a **NAT Gateway** to allow private subnets to securely access the internet.
  * Configured **route tables** to control traffic flow and enhance security.

* Understood the logic behind:
  * Public subnets → route through IGW.
  * Private subnets → route through NAT Gateway or internal resources.

* Learned the security benefits of separating workloads into public and private subnets.

---

#### **EC2 (Elastic Compute Cloud) Skills**

* Understood fundamental EC2 concepts:
  * Instance types (general-purpose, compute-optimized, memory-optimized, etc.)
  * AMIs (operating system and base configuration)
  * SSH key pairs and authentication
  * Security Groups for traffic control

* Practiced launching EC2 instances into:
  * A selected VPC
  * A specific subnet
  * Using configured security groups and key pairs
