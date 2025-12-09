---
title: "Week 3 Worklog"
date: "2025-09-22"
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

**Week Duration: September 22 - September 28, 2025**

### Week 3 Objectives:

- Understand how synthetic (AI-generated) data works and its limitations in ML training  
- Learn the process of assessing data quality: distribution checks, feature consistency, logical behavior  
- Re-generate synthetic data with improved structure and realistic patterns  
- Receive mentor feedback and refine dataset creation strategy  
- Gain hands-on experience with Amazon S3 fundamentals and core operations  

### Tasks to be carried out this week:

| Day | Task                                                                                                                                                                                                                                                  | Start Date | Completion Date | Reference Material           |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------- | --------------- | ---------------------------- |
| Monday  | - **Synthetic Data Generation:** <br>&emsp; + Generate initial synthetic dataset for the ML model <br>&emsp; + Study synthetic generation methods (prompt-based, schema-based) <br>&emsp; + Ensure feature alignment with actual model requirements      | 09/22/2025 | 09/22/2025      | Project Dataset Docs         |
| Tuesday-Wednesday | - **Data Quality Assessment:** <br>&emsp; + Check distribution of each feature <br>&emsp; + Detect unrealistic patterns and missing logical relationships <br>&emsp; + Compare synthetic vs. real-world expectations <br>&emsp; + Regenerate dataset     | 09/23/2025 | 09/24/2025      | Data Validation Guidelines   |
| Thursday | - **Mentor Consultation:** <br>&emsp; + Discuss issues with synthetic-only data <br>&emsp; + Learn hybrid-data strategy <br>&emsp; + Learn how to avoid uniform patterns and low variance <br>&emsp; + Plan improved data generation pipeline           | 09/25/2025 | 09/25/2025      | Mentor Session Notes         |
| Friday | - **Amazon S3 Fundamentals:** <br>&emsp; + Learn S3 concepts: buckets, objects, regions <br>&emsp; + Study storage classes and cost impact <br>&emsp; + Practice uploading/downloading files <br>&emsp; + Configure S3 versioning and lifecycle rules | 09/26/2025 | 09/26/2025      | https://000057.awsstudygroup.com/ |

### Week 3 Achievements:

- **Understanding Synthetic Data Limitations:**
  - Learned why synthetic data cannot serve as the only training source  
  - Recognized low variance due to single-model generation  
  - Identified unrealistic data behaviors and missing edge cases  
  - Understood overfitting risks from overly clean synthetic distributions  

- **Improved Data Strategy After Mentor Feedback:**
  - Planned hybrid data generation using multiple AI models  
  - Added small real data samples to improve realism  
  - Incorporated controlled randomness to mimic natural variability  
  - Applied validation through distribution checks, correlation checks, and logical consistency tests  

- **Amazon S3 Skills:**
  - Gained strong understanding of S3 object storage concepts  
  - Learned differences in bucket-level vs. object-level permissions  
  - Studied S3 storage classes: Standard, Standard-IA, One Zone-IA, Glacier tiers  
  - Practiced creating buckets, uploading objects, enabling versioning, and configuring lifecycle rules  
  - Learned S3’s role in ML pipelines, static hosting, backups, and integration with Lambda, EC2, and Athena  

- **Technical Competencies:**
  - Data generation and validation workflow  
  - Hybrid synthetic–real data design  
  - Hands-on AWS S3 operations and configuration  
  - Improved understanding of data quality and ML model robustness  

- **Readiness for Next Steps:**
  - Established strong foundation in data quality assessment  
  - Built a refined strategy for future dataset generation  
  - Prepared S3 storage structure for upcoming project datasets  
  - Ready to proceed to Week 4 with improved ML and AWS fundamentals  
