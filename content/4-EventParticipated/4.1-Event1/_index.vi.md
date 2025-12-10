---
title: "Sự kiện: Vietnam Cloud Day 2025"
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# **Vietnam Cloud Day 2025:**

# **Ho Chi Minh City Connect Edition for Builders - GenAI và Data Track**

**Địa điểm**: AWS Event Hall, L26 Bitexco Tower, HCMC

**Ngày**: Thứ Năm, 18 tháng 9, 2025

# Báo cáo học tập: "Vietnam Cloud Day 2025: GenAI và Data Track"

### Mục tiêu sự kiện

- Giới thiệu tổng quan về **Agentic AI** và quan điểm của AWS về xu hướng AI
- Học cách xây dựng **Nền tảng Dữ liệu Thống nhất** để hỗ trợ các hoạt động AI và phân tích dữ liệu trên AWS
- Phân tích lộ trình triển khai GenAI, **Kiến trúc AI Agent**, và các thách thức khi đưa vào môi trường sản xuất
- Tìm hiểu **Vòng đời Phát triển Dựa trên AI (AI-DLC)**
- Hiểu các nguyên tắc về **Bảo mật, Quản lý Rủi ro và AI Có trách nhiệm** trong Generative AI
- Giới thiệu **các dịch vụ AWS mới** hỗ trợ AI Agents và nâng cao hiệu quả doanh nghiệp

---

### Danh sách diễn giả

- **Jun Kai Loke** - Chuyên gia Kiến trúc Giải pháp AI/ML, AWS
- **Kien Nguyen** - Kiến trúc sư giải pháp, AWS
- **Tamelly Lim** - Chuyên gia Kiến trúc Giải pháp Lưu trữ, AWS
- **Binh Tran** - Kiến trúc sư cấp cao, AWS
- **Taiki Dang** - Kiến trúc sư giải pháp, AWS
- **Christal Poon** - Chuyên gia Kiến trúc Giải pháp, AWS

---

### Nội dung chính

#### Tổng quan về Agentic AI – Jun Kai Loke

- **Agentic AI** tập trung vào việc xây dựng các hệ thống tự chủ, giảm sự can thiệp của con người và tự động hóa các quy trình phức tạp
- Ví dụ thực tế: Katalon, Apero, Techcom Securities
- **Amazon Bedrock** là nền tảng AI chính, cung cấp:
  - Triển khai an toàn và quy mô lớn
  - Tích hợp công cụ và bộ nhớ
  - Giám sát toàn diện từ đầu đến cuối

#### Xây dựng Nền tảng Dữ liệu Thống nhất – Kien Nguyen

- **Thách thức hiện tại**: Nhiều doanh nghiệp chưa sẵn sàng cho triển khai GenAI; chỉ 52% CDO đánh giá nền tảng dữ liệu đủ khả năng (HBR)
- Nguyên nhân chính: dữ liệu phân mảnh, con người phân tách, các bộ phận riêng lẻ
- **Chiến lược dữ liệu toàn diện**: Kết hợp **Nhà sản xuất (Producers)**, **Nền tảng (Foundations)** và **Người tiêu dùng (Consumers)**
- **Dịch vụ AWS chính**:
  - **Amazon Bedrock** (nền tảng GenAI)
  - **Cơ sở dữ liệu** (RDS và hỗ trợ tìm kiếm vector)
  - **Analytics & ML** (SageMaker, Unified Studio)
  - **Quản trị Dữ liệu & AI**
  - **Kiến trúc Lake House** (S3, Redshift, Iceberg API)
  - **Amazon DataZone** (quản lý và chia sẻ dữ liệu)

#### Lộ trình GenAI & Kiến trúc AI Agent – Jun Kai Loke & Tamelly Lim

- Bản thiết kế AI Agents: Năng lực model & ứng dụng, và framework công cụ
- **Amazon Bedrock AgentCore** giải quyết các vấn đề khi triển khai sản xuất
- **Thành phần AgentCore**: Runtime, Gateway, Memory, Agent Browser, Code Interpreter; tăng cường **bảo mật** và **khả năng mở rộng**

#### Vòng đời Phát triển Dựa trên AI (AI-DLC) – Binh Tran

- AI-DLC là mô hình phát triển phần mềm tự động hóa, gồm 3 giai đoạn:

1. **Khởi đầu**: Xác định bối cảnh, tạo user story, lên kế hoạch
2. **Xây dựng**: Lập trình, test, bổ sung kiến trúc, triển khai IaC và kiểm thử
3. **Vận hành**: Triển khai sản xuất với IaC và quản lý sự cố

#### Bảo mật trong Generative AI – Taiki Dang

- **Các yếu tố bảo mật cốt lõi**: Tuân thủ & quản trị, pháp lý & quyền riêng tư, kiểm soát, quản lý rủi ro, khả năng phục hồi
- **Phân tích rủi ro theo lớp**: 
  - Người dùng cuối: hallucination, bản quyền, pháp lý  
  - Fine-tuning: lưu trữ dữ liệu  
  - Nhà cung cấp model: dữ liệu huấn luyện, xây dựng model
- **Chiến lược giảm thiểu**: Prompt engineering, Fine-tuning, RAG, điều chỉnh tham số, **Bedrock Guardrails**, prompt bảo mật
- Các chuẩn áp dụng: AWS Well-Architected, MITRE ATLAS, OWASP Top 10 LLM Apps, NIST AI 600-1, ISO 42001, EU AI Act

#### AI Agents nâng cao năng suất – Christal Poon

- Các loại AI Agent: Chuyên biệt, Quản lý toàn diện, DIY
- Dịch vụ hỗ trợ năng suất: **Amazon QuickSight** (phân tích), **Amazon Q** (dashboard, báo cáo, tóm tắt, kịch bản AI)

---

### Thành tựu

#### Tư duy & Chiến lược

- **Agentic AI** giúp tự động hóa nhiều quy trình, tập trung vào các việc quan trọng
- **Nền tảng dữ liệu mạnh mẽ** đảm bảo an toàn với khối lượng dữ liệu lớn (ví dụ: S3)
- **AI-DLC** tự động hóa toàn bộ quá trình phát triển từ lập kế hoạch đến triển khai

#### Kiến trúc & Công nghệ

- Hiểu **kiến trúc AI Agent** và **AgentCore** giải quyết vấn đề bảo mật & mở rộng khi triển khai sản xuất
- **Bảo mật** cần tích hợp ở mọi lớp AI stack, tuân thủ tiêu chuẩn quốc tế

#### Ứng dụng công nghệ

- AWS mở rộng hệ sinh thái **AI Agents & Enterprise AI** thông qua Amazon Q và QuickSuite (sắp ra mắt)

---

### Ứng dụng tại công việc

- **Tối ưu quy trình**: Tích hợp **AI Agents** vào các tác vụ lặp lại
- **Quản lý chất lượng**: Dùng **Bedrock, Amazon Q, Guardrails** để kiểm soát chất lượng, hạn chế hallucination
- **Xây dựng hạ tầng**: Đảm bảo nền tảng dữ liệu thống nhất trước khi triển khai GenAI
- **Áp dụng AI-DLC**: Thử nghiệm mô hình phát triển AI-DLC trong dự án nội bộ
- **Phân tích kinh doanh**: Sử dụng **QuickSight và Amazon Q** để tạo dashboard và báo cáo nhanh

---

### Trải nghiệm sự kiện

Workshop cung cấp hướng dẫn thực tiễn từ tự động hóa truyền thống đến **Agentic AI**. Trình bày về **AgentCore, Bedrock, AI-DLC, Amazon Q** minh họa toàn bộ hành trình AI, từ nền tảng dữ liệu đến vận hành an toàn.

- Thêm hình ảnh sự kiện tại đây

> Sự kiện cung cấp kiến thức kỹ thuật sâu và khuyến khích tích hợp AI một cách chiến lược, trách nhiệm vào mọi hoạt động kinh doanh.

### Diễn giả khác

- **Jignesh Shah** – Giám đốc, Open Source Databases
- **Erica Liu** – Chuyên gia GTM cao cấp, AppMod
- **Fabrianne Effendi** – Chuyên viên SA, Serverless AWS

### Điểm nổi bật

#### Thách thức kiến trúc cũ

- Chu kỳ phát hành sản phẩm dài → lỡ cơ hội
- Hoạt động kém hiệu quả → chi phí cao, năng suất thấp
- Lỗ hổng bảo mật → mất uy tín, rủi ro vi phạm

#### Kiến trúc hiện đại – Microservices

- Thiết kế mô-đun: các service độc lập giao tiếp qua sự kiện
- Trụ cột: **Quản lý Queue**, **Caching**, **Xử lý Message**

#### Domain-Driven Design (DDD)

- **4 bước**: Xác định domain events → timeline → actor → bounded context
- Case study bookstore minh họa DDD
- Context mapping: 7 mẫu tích hợp bounded context

#### Event-Driven Architecture

- **Mẫu tích hợp**: Pub/Sub, point-to-point, streaming
- Lợi ích: loose coupling, khả năng mở rộng, resilient
- So sánh sync vs async

#### Compute Evolution

- **Shared Responsibility**: EC2 → ECS → Fargate → Lambda
- Serverless: tự động mở rộng, không quản lý server
- Quyết định giữa function và container

#### Amazon Q Developer

- **Tự động SDLC**: từ lập kế hoạch đến bảo trì
- **Chuyển đổi code**: Java, .NET
- **AWS Transform agents**: VMware, Mainframe, .NET

### Bài học chính

#### Tư duy thiết kế

- **Ưu tiên kinh doanh**: bắt đầu từ domain, không phải công nghệ
- **Ngôn ngữ chung**: đồng bộ giao tiếp giữa các team
- **Bounded context**: quản lý phức tạp hệ thống lớn

#### Kiến thức kỹ thuật

- Event storming để mô hình hóa quy trình kinh doanh
- Giao tiếp event-driven thay cho call đồng bộ
- Chọn mẫu tích hợp phù hợp
- Lựa chọn compute: VM, container, serverless

#### Chiến lược hiện đại hóa

- **Tiến trình theo giai đoạn**, tuân theo roadmap
- **Khung 7Rs**: chọn phương án phù hợp theo ứng dụng
- **Đo ROI**: tiết kiệm chi phí + tăng agility

### Ứng dụng thực tế

- Thực hiện **DDD** với các team kinh doanh
- Xác định ranh giới microservices theo **bounded context**
- Thay sync call bằng async messaging
- Thử nghiệm **AWS Lambda** serverless
- Tích hợp **Amazon Q Developer** trong workflow

### Trải nghiệm sự kiện

Workshop **“GenAI-powered App-DB Modernization”** rất giá trị, trình bày kỹ thuật hiện đại hóa ứng dụng và database.

#### Học hỏi từ chuyên gia

- AWS và chuyên gia ngành chia sẻ **best practices** kiến trúc hiện đại
- Case study minh họa **DDD** và Event-Driven Architecture

#### Thực hành

- **Event storming** giúp chuyển quy trình kinh doanh thành domain events
- Học cách chia microservices và xác định **bounded context**
- Hiểu trade-offs giữa sync vs async và các pattern pub/sub, point-to-point, streaming

#### Sử dụng công cụ

- Thử **Amazon Q Developer** hỗ trợ SDLC
- Tự động hóa **code modernization** và thử serverless

#### Networking

- Trao đổi với chuyên gia, peer, cải thiện **ngôn ngữ chung**
- Case thực tế nhấn mạnh **business-first approach**

#### Bài học rút ra

- DDD + event-driven pattern tăng **khả năng mở rộng**, giảm coupling
- Modernization cần theo giai đoạn và **theo dõi ROI**
- AI tool như Amazon Q Developer giúp **tăng năng suất**

#### Hình ảnh sự kiện

- [Ảnh 1](/images/CloudDay_1.jpg)
- [Ảnh 2](/images/CloudDay_2.jpg)
- [Ảnh 3](/images/CloudDay_3.jpg)
- [Ảnh 4](/images/CloudDay_4.jpg)
> Tổng quan, workshop cung cấp kiến thức kỹ thuật và góc nhìn mới về thiết kế ứng dụng, hiện đại hóa hệ thống và hợp tác giữa các team.
