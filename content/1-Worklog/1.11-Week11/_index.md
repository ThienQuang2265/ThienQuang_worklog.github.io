---
title: "Week 11 Worklog"
date: "2025-11-17"
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

**Week Duration: November 17 - 23, 2025**

### Week 11 Objectives:

- Attempt to deploy the RAG system into the AWS environment.
- Explore multiple deployment strategies (Lambda layers, ECR container).
- Research Bedrock Knowledge Base features and pricing.
- Evaluate whether Bedrock Knowledge is a better alternative to manual RAG deployment.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ----- | ---------- | --------------- | ------------------ |
| Monday | - Participating in AWS Mastery 2: AWS DevOps & Modern Operations <br> | 11/17/2025 | 11/17/2025 | Project Docs |
| Tuesday | - Attempt deployment of RAG system to AWS environment <br> &emsp;+ Initial Lambda setup | 11/18/2025 | 11/18/2025 | Project Docs |
| Wednesday-Thursday | - Try multiple deployment methods <br> &emsp;+ Lambda layer (dependency test) <br> &emsp;+ ECR container build and deploy <br> &emsp;+ Debug dependency failures | 11/19/2025 | 11/20/2025 | AWS Lambda + ECR Docs |
| Friday  | - Research Amazon Bedrock Knowledge Base <br> - Study pricing and architecture <br> - Compare with custom RAG deployment | 11/21/2025 | 11/21/2025 | Bedrock Docs |

### Week 11 Achievements:

- Understood the deployment challenges caused by heavy dependencies in RAG pipelines.
- Realized Lambda layers and ECR containers introduce complexity and size limitations.
- Shifted strategy to using Bedrock Knowledge Base instead of manually deploying RAG.
- Studied Knowledge Base pricing and learned how it simplifies ingestion and retrieval.
- Gain fundamental knowledge of DevOp, CI/CD, etc and how AWS services like ECR, ECS could support those tasks