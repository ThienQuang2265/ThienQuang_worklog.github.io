---
title: "Event: Vietnam Cloud Day 2025"
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# **Vietnam Cloud Day 2025:**

# **Ho Chi Minh City Connect Edition for Builders - GenAI and Data Track**

**Location**: AWS Event Hall, L26 Bitexco Tower, HCMC

**Date**: Thursday, September 18, 2025

# Learning Report: "Vietnam Cloud Day 2025: GenAI and Data Track"

### Event Goals

- Present an overview of **Agentic AI** and AWS’s perspective on AI trends
- Learn how to create a **Unified Data Foundation** to enable AI initiatives and analytics on AWS
- Examine the GenAI deployment roadmap, **AI Agent Architecture**, and challenges in production adoption
- Explore the **AI-Driven Development Lifecycle (AI-DLC)** model
- Understand key practices for **Security, Risk Management, and Responsible AI** in Generative AI
- Introduce **new AWS services** designed to enhance AI Agents and business efficiency

---

### Speaker Roster

- **Jun Kai Loke** - AI/ML Solution Architecture Expert, AWS
- **Kien Nguyen** - Solution Architect, AWS
- **Tamelly Lim** - Storage Solution Architecture Expert, AWS
- **Binh Tran** - Senior Solution Architect, AWS
- **Taiki Dang** - Solution Architect, AWS
- **Christal Poon** - Solution Architecture Expert, AWS

---

### Key Takeaways from Presentations

#### Agentic AI Overview – Jun Kai Loke

- **Agentic AI** focuses on building autonomous systems that minimize human involvement and automate complex workflows
- Successful real-world examples: Techcombank, ELSA Speak
- **Amazon Bedrock** as the primary AI platform, offering:
  - Secure and scalable deployment
  - Tool and memory integration
  - Full end-to-end monitoring

#### Creating a Unified Data Foundation – Kien Nguyen

- **Current Issues**: Many organizations are unprepared for GenAI deployment; only 52% of CDOs rate their platforms as ready (HBR)
- Main obstacles: data silos, personnel silos, disconnected business units
- **Comprehensive Data Strategy**: Combines **Producers**, **Foundations**, and **Consumers**
- **Key AWS Data Services**:
  - **Amazon Bedrock** (GenAI platform)
  - **Databases** (RDS and specialized vector-search support)
  - **Analytics & ML** (SageMaker, Unified Studio)
  - **Data & AI Governance**
  - **Lake House Architecture** (S3, Redshift, Iceberg API)
  - **Amazon DataZone** (Data management and sharing)

#### GenAI Roadmap & AI Agent Architecture – Jun Kai Loke & Tamelly Lim

- Blueprint for AI Agents: Model & application capabilities, plus tool frameworks
- **Amazon Bedrock AgentCore** helps tackle production challenges
- **AgentCore Components**: Runtime, Gateway, Memory, Agent Browser, Code Interpreter; enhances **security** and **scalability**

#### AI-Driven Development Lifecycle (AI-DLC) – Binh Tran

- AI-DLC automates software development, comprising three stages:

1. **Inception**: Define context, user stories, and plan work units
2. **Construction**: Code, test, enhance architecture, deploy IaC, and validate
3. **Operation**: Production deployment with IaC and incident management

#### Security in Generative AI – Taiki Dang

- **Core Security Elements**: Compliance, governance, legal/privacy, controls, risk management, resilience
- **Risk Assessment by Layer**: 
  - End-user: hallucination, IP, legal issues  
  - Fine-tuning: data retention  
  - Model provider: training data, model construction
- **Mitigation Techniques**: Prompt engineering, fine-tuning, RAG, parameter adjustments, **Bedrock Guardrails**, secure prompts
- Standards to follow: AWS Well-Architected, MITRE ATLAS, OWASP Top 10 LLM Apps, NIST AI 600-1, ISO 42001, EU AI Act

#### AI Agents for Business Productivity – Christal Poon

- AI Agent categories: Specialized, Fully-managed, DIY
- Productivity tools: **Amazon QuickSight** (analytics), **Amazon Q** (dashboards, reports, summaries, AI scenarios)

---

### Achievements

#### Mindset & Strategy

- **Agentic AI** can automate routine processes, allowing focus on strategic work
- **Robust data platforms** are crucial to handle growing data volumes securely (e.g., S3)
- **AI-DLC** automates development from planning to deployment

#### Architecture & Technology

- Understanding **AI Agent architecture** and **AgentCore** resolves production security and scalability issues
- **Security integration** is required at all levels of the AI stack, adhering to international regulations

#### Technology Application

- AWS is expanding the **AI Agents & Enterprise AI** ecosystem with services like Amazon Q and QuickSuite (upcoming)

---

### Application to Work

- **Process Optimization**: Integrate **AI Agents** into repetitive tasks
- **Quality Control**: Leverage **Bedrock, Amazon Q, Guardrails** to ensure quality and prevent hallucinations
- **Infrastructure Development**: Build a **unified data platform** with clear governance for GenAI projects
- **Implement AI-DLC**: Apply AI-DLC methodology in internal development
- **Business Insights**: Use **QuickSight and Amazon Q** for dashboards and reports

---

### Event Experience

The workshop offered practical guidance for transitioning from traditional automation to **Agentic AI**. Presentations on **AgentCore, Bedrock, AI-DLC, and Amazon Q** demonstrated the full spectrum of AI adoption, from data platforms to secure operations.

- Add your event photos here

> The event provided deep technical insights and encouraged strategic, responsible integration of AI into business processes.

### Additional Speakers

- **Jignesh Shah** – Director, Open Source Databases
- **Erica Liu** – Sr. GTM Specialist, AppMod
- **Fabrianne Effendi** – Assoc. Specialist SA, Serverless AWS

### Key Points

#### Legacy Architecture Challenges

- Slow release cycles → missed opportunities
- Inefficient operations → higher costs and lower productivity
- Security gaps → breaches and reputation risks

#### Modern Architecture – Microservices

- Modular design: independent services communicating via events
- Core pillars: **Queue Management**, **Caching**, **Message Handling**

#### Domain-Driven Design (DDD)

- **4-step method**: Identify domain events → timeline → actors → bounded contexts
- Bookstore case study demonstrates DDD in action
- Context mapping: 7 patterns for bounded context integration

#### Event-Driven Architecture

- **Integration patterns**: Pub/Sub, point-to-point, streaming
- Benefits: loose coupling, scalability, resilience
- Sync vs async trade-offs

#### Compute Evolution

- **Shared Responsibility**: EC2 → ECS → Fargate → Lambda
- Serverless: auto-scaling, no server maintenance
- Choosing between functions and containers

#### Amazon Q Developer

- **SDLC automation**: planning to maintenance
- **Code transformation**: Java, .NET modernization
- **AWS Transform agents**: VMware, Mainframe, .NET migration

### Key Lessons

#### Design Thinking

- **Business-first mindset**: start with domain, not tech
- **Shared vocabulary**: unify communication between teams
- **Bounded contexts**: manage large-system complexity

#### Technical Insights

- Event storming to model business processes
- Event-driven communication over synchronous calls
- Appropriate integration pattern selection
- Compute choice: VM, containers, serverless

#### Modernization Approach

- **Phased modernization**: follow a clear roadmap
- **7Rs framework**: choose the best path per application
- **ROI assessment**: measure cost reduction and agility gains

### Applying Insights at Work

- Conduct **DDD sessions** with business teams
- Define microservice boundaries using **bounded contexts**
- Replace sync calls with async messaging patterns
- Pilot **AWS Lambda** for serverless projects
- Integrate **Amazon Q Developer** into workflows

### Event Experience

The **“GenAI-powered App-DB Modernization”** workshop was highly valuable, showing modern techniques for application and database modernization.

#### Learning from Experts

- AWS and industry professionals shared **best practices** in modern architecture
- Case studies deepened understanding of **DDD** and **Event-Driven Architecture**

#### Hands-on Exposure

- **Event storming** sessions helped translate business processes into domain events
- Learned how to split microservices and define **bounded contexts**
- Explored sync vs async communication and patterns (pub/sub, point-to-point, streaming)

#### Leveraging Tools

- Tested **Amazon Q Developer** for SDLC support
- Learned to automate **code modernization** and pilot **serverless**

#### Networking

- Exchanged ideas with experts and peers, improving **shared vocabulary**
- Real-world cases emphasized **business-first approach**

#### Lessons Learned

- DDD and event-driven patterns improve **scalability** and reduce coupling
- Modernization requires phased execution and **ROI tracking**
- AI tools like Amazon Q Developer can **boost productivity**

#### Event Photos

- [Image 1](/images/CloudDay_1.jpg)
- [Image 2](/images/CloudDay_2.jpg)
- [Image 3](/images/CloudDay_3.jpg)
- [Image 4](/images/CloudDay_4.jpg)


> Overall, the workshop provided both technical knowledge and a new perspective on application design, system modernization, and team collaboration.

