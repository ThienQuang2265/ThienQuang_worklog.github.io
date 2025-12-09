---
title: "Week 9 Worklog"
date: "2025-11-03"
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

**Week Duration: November 3 - 9, 2025**

### Week 9 Objectives:

- Deploy the auto_scoring ML model into the AWS environment.
- Learn how Lambda layers work and how to package dependencies.
- Practice building Docker images and pushing them to Amazon ECR.
- Deploy the model successfully using ECR-based Lambda.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ----- | ---------- | --------------- | ------------------ |
| Monday | - Deploy auto_scoring model to AWS environment <br> &emsp;+ Test basic inference | 11/03/2025 | 11/03/2025 | Project Docs |
| Tuesday-Wednesday | - Study Lambda dependency management <br> &emsp;+ Create Lambda layers <br> &emsp;+ Check size limitations <br> &emsp;+ Explore alternative deployment methods | 11/04/2025 | 11/05/2025 | AWS Lambda Docs |
| Thursday   | - Build Docker image for model <br> - Push image to Amazon ECR <br> - Configure IAM permissions | 11/06/2025 | 11/06/2025 | AWS ECR Docs |
| Friday   | - Deploy Lambda using ECR container <br> - Run model inference tests | 11/07/2025 | 11/07/2025 | AWS Lambda + ECR Docs |

### Week 9 Achievements:

- Learned the file-size limitations of Lambda layers.
- Successfully packaged the ML model using a Docker image.
- Uploaded the image to Amazon ECR and deployed it to Lambda.
- Fully deployed the auto_scoring model into AWS with container-based execution.
- Understood how ECR is essential for large machine learning models with many dependencies.