---
title: "Đề Xuất"
date: "2025-09-22"
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

**[📥 Tải Xuống Proposal ](/Proposal.pdf)**

---

## AWS First Cloud AI Journey – Kế Hoạch Dự Án

[SKYLINE2] – [University] – [INSIGHTHR]  
[09-12-2025]

---

## Mục Lục

1. [BACKGROUND và MOTIVATION](#background-and-motivation)

   - 1.1 [Executive Summary](#executive-summary)
   - 1.2 [Project Success Criteria](#project-success-criteria)
   - 1.3 [Assumptions](#assumptions)

2. [SOLUTION ARCHITECTURE / ARCHITECTURAL DIAGRAM](#solution-architecture)

   - 2.1 [Technical Architecture Diagram](#technical-architecture-diagram)
   - 2.2 [Technical Plan](#technical-plan)
   - 2.3 [Project Plan](#project-plan)
   - 2.4 [Security Considerations](#security-considerations)

3. [Activities AND Deliverables](#activities-and-deliverables)

   - 3.1 [Activities and deliverables](#activities-and-deliverables-detail)
   - 3.2 [Out of Scope](#out-of-scope)
   - 3.3 [Path to Production](#path-to-production)

4. [EXPECTED AWS COST BREAKDOWN BY SERVICES](#cost-breakdown)

5. [TEAM](#team)

6. [RESOURCES & COST ESTIMATES](#resources-and-cost-estimates)

7. [ACCEPTANCE](#acceptance)

---

## BACKGROUND AND MOTIVATION {#background-and-motivation}

### 1.1 Executive Summary {#executive-summary}

Tổ chức đối mặt với các vấn đề về hiệu quả đánh giá nhân sự do xử lý dữ liệu thủ công, thiếu tính minh bạch trong các quy trình đánh giá và theo dõi chỉ số.

InsightHR cung cấp tự động hóa HR thông qua quản lý đánh giá linh hoạt, tính điểm tự động và AI insights. AWS cung cấp khả năng mở rộng serverless, hiệu quả chi phí, bảo mật cho dữ liệu nhạy cảm, AI Chatbot thông qua Bedrock và triển khai nhanh chóng.

**Custom KPI, tính điểm hiệu suất tự động, bảng điều khiển đa cấp, trợ lý AI cho truy vấn ngôn ngữ tự nhiên, thông báo tự động, quyền truy cập dựa trên vai trò (Admin/Manager/Employee), hỗ trợ đa thuê.**

Cung cấp toàn diện bao gồm thiết kế Well-Architected, backend serverless (Lambda, DynamoDB, API Gateway), frontend (S3 + CloudFront), xác thực/bảo mật (Cognito, IAM), KPI/formula builder, chatbot AI (Bedrock + Lambda truy vấn dữ liệu từ bảng thông tin), thông báo (SNS, SES), CI/CD, giám sát và chuyển giao kiến thức.

### 1.2 Project Success Criteria {#project-success-criteria}

Thành công được định nghĩa bằng việc chứng minh một MVP chức năng chứng tỏ khả năng của nền tảng tự động hóa các đánh giá HR và cung cấp giá trị kinh doanh có thể đo lường được.

**1. Functional Criteria:**

- Xác thực với quyền truy cập dựa trên vai trò (Admin/HR, Manager, Employee)
- HR tạo KPIs tùy chỉnh mà không cần hỗ trợ kỹ thuật
- Tải lên CSV kích hoạt tính điểm Lambda tự động
- Bảng điều khiển hiển thị hiệu suất cá nhân/nhóm với biểu đồ
- Chatbot AI trả lời các truy vấn ngôn ngữ tự nhiên từ dữ liệu DynamoDB
- SES gửi thông báo email tự động

**2. Technical Criteria:**

- 99.9%+ uptime
- <300ms API latency (95th percentile)
- 95%+ scoring accuracy vs tính toán thủ công
- 90%+ AI response relevance
- Zero critical security vulnerabilities

**3. Performance & Cost:**

- ~$33.14/month AWS cost
- End-to-end workflow (tải lên → điểm → hình dung) hoàn tất trong <5 phút

**4. Business Impact:**

- Chứng minh khả năng giảm thời gian HR 60%+
- Người dùng không kỹ thuật vận hành KPI builder và chatbot độc lập

**5. Delivery:**

- Week 8: MVP (xác thực, quản lý KPI/công thức, tính điểm, bảng điều khiển cơ bản)
- Week 12: Tính năng đầy đủ (chatbot, thông báo, bảng điều khiển nâng cao)

### 1.3 Assumptions {#assumptions}

**1. Assumptions:**

- Ước tính chi phí AWS hiện tại khoảng $33.14/tháng là chính xác cho tải và sử dụng ban đầu được dự báo.
- Định dạng dữ liệu cần thiết và logic ánh xạ cho dữ liệu hiệu suất nhân viên có thể được định rõ ràng và do Nhóm HR cung cấp cho engine tính điểm tự động.
- Large Language Model được cung cấp bởi Amazon Bedrock hỗ trợ HR.
- Hệ thống tính điểm tự động được huấn luyện cục bộ. Các tệp đánh giá kỹ thuật của mỗi nhóm được đánh giá theo tiêu chí của công ty và phải tuân theo định dạng do khách hàng cung cấp.

**2. Constraints:**

- Việc cung cấp dự án phải tuân thủ lịch trình 12 tuần sử dụng framework Agile Scrum.
- Giải pháp phải được xây dựng hoàn toàn trên các dịch vụ AWS serverless để đáp ứng các mục tiêu về khả năng mở rộng, hiệu quả chi phí và giảm chi phí hoạt động.
- Chi phí AWS sản xuất cuối cùng phải ở mức ~$33.14/tháng.

**3. Risks:**

- **Data Security/Compliance:** Không thể hiểu đầy đủ hoặc triển khai tất cả các yêu cầu xác nhận kiểm soát quy định cụ thể của khách hàng có thể ảnh hưởng đến khả năng của dự án đáp ứng các mục tiêu bảo mật.
- **Feature Creep:** Yêu cầu các tính năng được xác định là "Out of Scope" có thể làm trật khỏi lịch trình cung cấp MVP 12 tuần.

---

## SOLUTION ARCHITECTURE / ARCHITECTURAL DIAGRAM {#solution-architecture}

### 2.1 Technical Architecture Diagram {#technical-architecture-diagram}

Nền tảng InsightHR được xây dựng trên kiến trúc serverless sử dụng các dịch vụ AWS, cung cấp khả năng mở rộng, hiệu quả chi phí và tính khả dụng cao. Kiến trúc bao gồm:

**1. Frontend & Content Delivery:**

- **Amazon S3:** Lưu trữ trang web tĩnh và lưu trữ các tệp do người dùng tải lên (CSV, mô hình AI). S3 Vector để lưu trữ vector (embeddings cho dữ liệu văn bản), S3 Standard để lưu trữ các tài liệu thô.
- **Amazon CloudFront:** Phân phối nội dung tĩnh và động trên toàn cầu với độ trễ thấp.

**2. Backend & Compute:**

- **AWS Lambda:** Thực thi tất cả logic kinh doanh, bao gồm xác thực, tính điểm tùy chỉnh và chức năng chatbot.
- **Amazon API Gateway:** Quản lý API làm cổng giao tiếp giữa frontend và backend.

**3. Data Storage:**

- **Amazon DynamoDB:** Lưu trữ dữ liệu có cấu trúc như thông tin người dùng/nhân viên, KPI công ty, công thức tính điểm và kết quả đánh giá hiệu suất.

**4. AI & Machine Learning:**

- **Amazon Bedrock:** Cung cấp Large Language Models (LLMs) cho chatbot trợ lý HR.
- **The ML Model system is trained locally for scoring function.**

**5. Security & Identity:**

- **Amazon Cognito:** Quản lý xác thực người dùng, đăng ký và quy trình xác định danh tính.
- **AWS IAM:** Quản lý kiểm soát truy cập và quyền cho các dịch vụ AWS.
- **AWS KMS:** Mã hóa dữ liệu nhạy cảm trong DynamoDB và S3.

**6. Monitoring & Notifications:**

- **Amazon CloudWatch & CloudWatch Logs:** Giám sát các hàm Lambda, API Gateway và quyền truy cập cơ sở dữ liệu.
- **Amazon SNS:** Gửi thông báo (ví dụ: nhắc nhở, thông báo kết quả) cho nhân viên.

**7. Architecture Benefits:**

- Serverless: Không quản lý máy chủ và tự động mở rộng.
- Cost-Effective: Hầu hết các dịch vụ theo kiểu trả tiền khi sử dụng.
- High Availability: Dự phòng tích hợp trên các vùng AWS.
- Scalable: Có thể xử lý tăng trưởng từ các nhóm nhỏ đến các doanh nghiệp lớn.
- Flexible: Dễ dàng sửa đổi và mở rộng chức năng.

**8. Proposed Architecture Diagram:**

![Architecture Diagram](/images/diagram.png)

**9. Tools Proposed for This Project:**

- **Amazon CloudFront:** Để phân phối nội dung toàn cầu và lưu trữ nội dung web tĩnh và động.
- **Amazon S3:** Để lưu trữ tài sản web tĩnh và lưu trữ tài liệu, embeddings vector và các tệp khác được xử lý bởi hệ thống.
- **Amazon API Gateway:** Để cung cấp giao diện RESTful an toàn, hoạt động như lớp giao tiếp giữa các máy khách frontend và các dịch vụ backend.
- **AWS Lambda:** Để chạy logic kinh doanh backend bao gồm bảng điều khiển người dùng, tính điểm tự động, trợ lý HR và quy trình quản lý dữ liệu.
- **Amazon DynamoDB:** Để lưu trữ dữ liệu ứng dụng như thông tin người dùng, hồ sơ HR, kết quả tính điểm và siêu dữ liệu vector với hiệu suất độ trễ thấp.
- **Amazon Cognito:** Để quản lý xác thực người dùng, ủy quyền, đăng ký, MFA và truy cập an toàn vào API và các ứng dụng frontend.
- **AWS Identity and Access Management (IAM):** Để xác định các chính sách truy cập chi tiết và kiểm soát quyền giữa các dịch vụ và người dùng.
- **AWS Key Management Service (KMS):** Để quản lý các khóa mã hóa được sử dụng để bảo mật dữ liệu nhạy cảm được lưu trữ trong S3, DynamoDB và nhật ký.
- **Amazon ECR:** Để lưu trữ các tài sản mô hình container hóa và phụ thuộc ứng dụng trong kho lưu trữ an toàn và có kiểm soát phiên bản.
- **Amazon Bedrock / Large Language Model (LLM):** Để cung cấp các khả năng AI cho trò chuyện, trích xuất dữ liệu, tóm tắt và quy trình làm việc HR thông minh.
- **Amazon Simple Email Service (SES):** Để gửi thông báo email tự động như cảnh báo onboarding và giao tiếp HR.
- **Amazon Simple Notification Service (SNS):** Để xuất bản thông báo và kích hoạt các quy trình hạ lưu; tích hợp với email, SMS và microservices.
- **Amazon CloudWatch & CloudWatch Logs:** Để giám sát hiệu suất, ghi nhật ký, theo dõi và khắc phục sự cố hoạt động trên Lambda, API Gateway và các thành phần AI.

### 2.2 Technical Plan {#technical-plan}

Đối tác sẽ phát triển các tập lệnh triển khai tự động bằng AWS CloudFormation và các quy trình IaC (Infrastructure as Code).

Điều này sẽ cho phép triển khai nhanh chóng và có thể lặp lại vào các tài khoản AWS. Một số cấu hình bổ sung như quy tắc WAF trên CloudFront để tăng cường bảo mật có thể yêu cầu phê duyệt và sẽ tuân theo các quy trình quản lý thay đổi DevOps tiêu chuẩn.

**Application Feature Implementation:**

**1. Authentication & Security Module**

- **User Management:** Cognito quản lý vòng đời người dùng Đăng ký, đăng nhập, quy trình đặt lại mật khẩu
- **Access Control:** IAM và RBAC thực thi các quyền dựa trên vai trò Admin/HR, Manager, Employee access levels
- **API Security:** API Gateway triển khai các endpoint được bảo vệ JWT Xác thực mã thông báo trước khi xử lý Lambda

**2. Administration Module (HR Panel)**

- **KPI Management:** HR tạo, chỉnh sửa và xóa các số liệu tùy chỉnh Ví dụ: Công việc đã hoàn thành, Chất lượng mã, Sự hài lòng của khách hàng Các định nghĩa được lưu trữ trong DynamoDB
- **Auto scoring by employee's technical score for each team with ML model.**

**3. Core User Functions**

- **Data Upload & Mapping:** Tải lên các tệp dữ liệu hiệu suất (CSV) vào DynamoDB
- **Scoring Engine:** Lambda được kích hoạt khi tải lên Lấy công thức hoạt động từ DynamoDB Tính điểm nhân viên Lưu trữ kết quả trong DynamoDB Flow: Tải lên → Xác thực → Ánh xạ → Tính toán → Lưu trữ
- **Dashboard:** Hình dung hiệu suất cá nhân và bộ phận Biểu đồ dòng, biểu đồ thanh, phân tích xu hướng
- **AI Chatbot:** Tích hợp Bedrock (LLM) Truy vấn ngôn ngữ tự nhiên (ví dụ: "Tóm tắt hiệu suất Q4 của Nhóm A") Truy vấn và tóm tắt dữ liệu DynamoDB
- **Notifications:** SES gửi cảnh báo tự động Các mốc hiệu suất, nhắc nhở xem xét, các kích hoạt tùy chỉnh

### 2.3 Project Plan {#project-plan}

Đối tác sẽ áp dụng framework Agile Scrum trong 12 sprint một tuần tạo thành lịch trình cung cấp 12 tuần.

**1. Team Responsibilities**

- **Product Owner:** Ưu tiên backlog (KPIs, công thức, phân tích) Thẩm quyền cuối cùng về chấp nhận tính năng
- **Development Team:** Triển khai xác thực Cognito Xây dựng cổng thông tin quản trị và trình xây dựng công thức Phát triển engine tính điểm và bảng điều khiển Tích hợp chatbot Bedrock và SNS với thông báo SES qua Email.
- **QA Personnel:** Tiến hành kiểm tra chức năng, hiệu suất và bảo mật Hỗ trợ UAT Đảm bảo tuân thủ và tiêu chuẩn chất lượng

**2. Communication Cadences**

- **Daily Standups (30 phút - 1 giờ):** Xem xét tiến độ và xác định rào cản
- **Retrospectives (Hàng tuần, 1 giờ):** Cải thiện quy trình và tối ưu hóa cung cấp
- **Executive Updates (Hàng tuần):** Báo cáo bằng văn bản về tiến độ, rủi ro, KPIs, lộ trình Các quyết định lãnh đạo được yêu cầu

**3. Knowledge Transfer**

- Các phiên do nhóm phát triển thực hiện bao gồm kiến thức cơ bản về serverless AWS Cấu hình KPI và công thức Quy trình dữ liệu và ánh xạ cột Điều hướng bảng điều khiển và phân tích Giám sát hệ thống (CloudWatch, Cognito, DynamoDB)

### 2.4 Security Considerations {#security-considerations}

Đối tác sẽ triển khai các phương pháp bảo mật AWS tốt nhất dựa trên Well-Architected Framework, ưu tiên bảo vệ dữ liệu HR nhạy cảm trong khi đảm bảo tính khả dụng hoạt động cao. Triển khai bảo mật bao gồm năm danh mục chính:

**1. Access Control**

- Cognito quản lý nhận dạng người dùng Thực thi các chính sách mật khẩu mạnh và hỗ trợ MFA
- IAM triển khai RBAC Admin/HR access Admin Panel và cấu hình KPI/Công thức Nhân viên chỉ xem dữ liệu hiệu suất của riêng họ
- API Gateway xác thực các mã thông báo JWT Các mã thông báo do Cognito cấp được xác minh trước khi xử lý Lambda

**2. Infrastructure Security**

- Kiến trúc serverless giảm bề mặt tấn công Không cần vá OS hoặc máy chủ
- Các hàm Lambda giao tiếp thông qua các mạng AWS riêng tư Chỉ các endpoint cần thiết được tiếp xúc thông qua API Gateway

**3. Data Protection**

- KMS mã hóa dữ liệu khi chưa hoạt động DynamoDB và S3 được mã hóa Dữ liệu không thể sử dụng được mà không có các khóa giải mã
- TLS/SSL (HTTPS) mã hóa dữ liệu khi đang truyền Tất cả giao tiếp frontend-backend được bảo mật

**4. Detection & Monitoring**

- CloudWatch Logs ghi lại các chi tiết thực thi Hoạt động Lambda và API Gateway được ghi lại Giám sát thời gian thực và phát hiện bất thường được bật
- AWS Config theo dõi các thay đổi cấu hình Đảm bảo tuân thủ tài nguyên với các mục tiêu bảo mật

**5. Incident Management**

- CloudWatch Alarms kích hoạt cảnh báo tự động thông qua SES Lỗi vượt ngưỡng đăng nhập Bất thường tài nguyên Lambda
- Security Hub cung cấp chế độ xem bảo mật tập trung Các phát hiện tuân thủ thống nhất trên môi trường AWS Đơn giản hóa xác định sự cố và phản ứng

AWS CloudTrail và AWS Config sẽ được định cấu hình để giám sát liên tục các hoạt động và trạng thái tuân thủ của các tài nguyên. Khách hàng sẽ chia sẻ các yêu cầu xác nhận kiểm soát quy định cụ thể của họ làm đầu vào để đối tác đảm bảo tất cả các mục tiêu bảo mật được đáp ứng.

---

## ACTIVITIES AND DELIVERABLES {#activities-and-deliverables}

### 3.1 Activities and Deliverables {#activities-and-deliverables-detail}

**NOTE: Some Project Phases overlap each other.**

| Project Phase                            | Timeline  | Activities                                                                                                                         | Deliverables/Milestones                                                                                                                                                                                               | Total man-day |
| ---------------------------------------- | --------- | ---------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------- |
| Phase 1: Foundation & Scoring Model      | Week 1-8  | • Nghiên cứu kiến trúc cơ sở hạ tầng cá nhân • Tạo dữ liệu cho đào tạo mô hình cục bộ • Xây dựng mô hình tính điểm                 | • Sơ đồ kiến trúc cá nhân hoàn thiện • Bộ dữ liệu sẵn sàng cho đào tạo Mô hình cục bộ • Scoring Model MVP (Minimum Viable Product)                                                                                    | 80            |
| Phase 2: Project Setup & Dashboard       | Week 9-10 | • Thiết lập dự án với các chức năng cơ bản: IAM Role, CRUD function, Static web • Web UI Demo • Triển khai Dashboard • Sửa mô hình | • Cấu hình IAM Roles cơ bản • Các hàm CRUD hoạt động • Trang web tĩnh được triển khai (S3/CloudFront) • Web UI Demo hoàn tất • Dashboard hiển thị dữ liệu được triển khai                                             | 40            |
| Phase 3: AI Agent & Absence Mgmt         | Week 11   | • Xây dựng Bedrock Agent • Triển khai quản lý Absence                                                                              | • Bedrock Agent được xây dựng • Quy trình theo dõi Absence hoạt động được triển khai                                                                                                                                  | 15            |
| Phase 4: Integration, Testing & Handover | Week 12   | • Triển khai Chatbot vào Ứng dụng • Kiểm tra và thiết lập Giám sát                                                                 | • Chatbot được tích hợp vào ứng dụng • Kiểm tra chức năng, hiệu suất và bảo mật hoàn tất • Giám sát (CloudWatch) được cấu hình và hoạt động • Báo cáo Hoàn thành Dự án & Kế hoạch hỗ trợ sau triển khai được cung cấp | 15            |

### 3.2 Out Of Scope {#out-of-scope}

**1. AI Enhancements**

**AI-Powered Insights:**

- Khi có đủ dữ liệu, phát triển các mô hình AI có khả năng:
  - Chatbot truy cập cơ sở dữ liệu trực tiếp và truy xuất cửa sổ nhắc nhở -> Giá rất nhiều mã thông báo và khóa cao, trong tương lai có thể được tối ưu hóa bằng các cách khác
  - Xác định các mẫu hiệu suất trên các nhóm và bộ phận
  - Dự đoán rủi ro HR (ví dụ: khả năng rời khỏi, chỉ số kiệt sức)
  - Đề xuất các kế hoạch phát triển được cá nhân hóa
  - Phát hiện bất thường trong dữ liệu hiệu suất
  - Đề xuất thành phần nhóm tối ưu

**Machine Learning Features:**

- Phân tích dự đoán cho kế hoạch lực lượng lao động
- Phân tích cảm tính từ phản hồi của nhân viên
- Phân tích khoảng cách kỹ năng tự động
- Dự báo xu hướng hiệu suất

**2. Public API Development**

**API Ecosystem:**

- Xây dựng một bộ API toàn diện cho phép các hệ thống kinh doanh nội bộ khác tự động đẩy dữ liệu hiệu suất vào InsightHR.

**Integration Targets:**

- Công cụ quản lý dự án (Jira, Asana, Monday.com)
- Hệ thống CRM (Salesforce, HubSpot)
- Phần mềm theo dõi thời gian (Toggl, Harvest)
- Nền tảng giao tiếp (Slack, Microsoft Teams)
- Kho lưu trữ mã (GitHub, GitLab, Bitbucket)

**Benefits:**

- Biến InsightHR thành trung tâm xử lý dữ liệu HR tập trung
- Tạo hệ sinh thái quản lý đồng bộ và toàn diện
- Loại bỏ nhập dữ liệu thủ công
- Theo dõi hiệu suất theo thời gian thực

**3. Advanced Features**

**Mobile Applications:**

- Ứng dụng iOS và Android gốc
- Thông báo đẩy
- Khả năng ngoại tuyến
- Bảo điểm điều khiển được tối ưu hóa cho di động
- Sao lưu DynamoDB

**Advanced Analytics:**

- Mô hình dự đoán
- Đánh giá kỹ năng so sánh trên toàn ngành
- Trình xây dựng báo cáo tùy chỉnh
- Xuất dữ liệu và API cho công cụ của bên thứ ba

**Collaboration Features:**

- Hệ thống đánh giá ngang hàng
- Phản hồi 360 độ
- Đặt mục tiêu và theo dõi
- Kế hoạch cải thiện hiệu suất

**Compliance & Governance:**

- Đường dõi kiểm toán
- Báo cáo tuân thủ
- Chính sách giữ lại dữ liệu
- Kiểm soát truy cập nâng cao

### 3.3 Path To Production {#path-to-production}

Tài liệu này mô tả kiến trúc sản xuất hiện tại và trạng thái hoạt động của việc triển khai nền tảng InsightHR. Nền tảng này đang hoạt động hoàn toàn ở vùng ap-southeast-1 (Singapore).

**1. Platform Architecture and Access**

- **Public URL:** https://d7gdgmhloq3vn.cloudfront.net
- **AWS Region:** ap-southeast-1 (Singapore)
- **Frontend:** Ứng dụng React được lưu trữ trên S3 (insighthr-web-app-sg) với phân phối HTTPS CloudFront.
- **Backend:** 8 nhóm hàm Lambda được truy cập thông qua API Gateway REST API.
- **Database:** DynamoDB tables được cấu hình với dung lượng On-Demand.
  - 6 bảng cho mỗi nhóm
  - Bảng thông tin nhân viên
  - Bảng điểm lịch sử
  - Bảng Absent
  - Bảng quản lý tài khoản
- **Authentication:** Cognito User Pool.
- **AI/Chatbot:** Amazon Bedrock (Claude 3 Haiku) tích hợp cho lịch sử cuộc trò chuyện và cơ sở kiến thức để nâng cao mô hình.

**2. Live Production Features**

Các tính năng chính sau đây đã được triển khai thành công và đang hoạt động:

- **Authentication:** Hỗ trợ đầy đủ cho đăng nhập email/mật khẩu, quy trình đặt lại mật khẩu.
- **User Management:** Chức năng CRUD đầy đủ, bao gồm nhập hàng loạt và truy cập dựa trên vai trò.
- **Employee Management:** Hỗ trợ đầy đủ cho 300+ nhân viên và hoạt động hàng loạt.
- **Performance Score Management:** Quản lý 900+ điểm số theo quý và xem dựa trên lịch.
- **Attendance Management:** Xử lý 9,300+ bản ghi, bao gồm chức năng kiosk check-in/check-out và đánh dấu absence tự động.
- **Performance Dashboard:** Biểu đồ trực tiếp, phân tích xu hướng, đồng hồ trực tiếp và khả năng xuất CSV.
- **AI Chatbot:** Tích hợp Bedrock với lịch sử cuộc trò chuyện được bật.

**3. Deployment and Verification Process**

Quy trình triển khai tiêu chuẩn và có thể lặp lại đảm bảo cập nhật nhanh chóng và có thể xác minh được:

- **Build:** `npm run build` tạo bộ tài sản sản xuất được tối ưu hóa.
- **Test:** `npm run preview` xác thực bộ được xây dựng cục bộ trước khi triển khai.
- **Deploy:** `aws s3 sync dist/ s3://insighthr-web-app-sg --region ap-southeast-1` đẩy tài sản vào nhóm S3.
- **Invalidate:** `aws cloudfront create-invalidation --distribution-id E3MHW5VALWTOCI --paths "/*"` xóa bộ đệm CDN CloudFront.
- **Verify:** Kiểm tra tính năng đầy đủ được thực hiện trên URL công khai trực tiếp.

**4. Remaining Production Enhancements**

Nền tảng này ở giai đoạn cuối cùng của việc nâng cao trước khi ổn định hoàn toàn, với các mục chính được lên kế hoạch hoặc đang tiến hành:

**Page Integration (In Progress)**

- Hợp nhất tất cả điều hướng trang quản trị.
- Xác minh tất cả các tính năng đều có thể truy cập từ menu chính.
- Kiểm tra định tuyến dựa trên vai trò trên tất cả các trang.
- Sửa các lỗi tích hợp.

**Polish and Final Deployment (Planned)**

- Triển khai xử lý lỗi toàn diện và xác thực đầu vào.
- Tinh chỉnh thiết kế responsive để tương thích đầy đủ với di động.
- Tiến hành kiểm tra bảo mật chuyên dụng (thử nghiệm xâm nhập, quét lỗ hổng).
- Thực thi kiểm tra tải để xác thực khả năng mở rộng.
- Phát triển tài liệu người dùng và tài liệu đào tạo.
- Thực hiện các thủ tục tăng cường sản xuất cuối cùng.

**Monitoring and Scalability Strategy**

- **Active Monitoring:** CloudWatch Logs được bật cho tất cả các hàm Lambda và endpoint API Gateway, cùng với CloudWatch Metrics để theo dõi hiệu suất.
- **Planned Alarms:** CloudWatch Alarms và thông báo SNS được lên kế hoạch cho tỷ lệ lỗi và độ trễ críti.
- **Scalability:** Đạt được thông qua Architecture Serverless (DynamoDB On-Demand, Lambda, CloudFront CDN).
- **Disaster Recovery:** Khôi phục Điểm trong Thời gian DynamoDB và Phiên bản S3 được lên kế hoạch để được bật cho dữ liệu/tài sản quan trọng. Mã Lambda được lưu trữ trong kiểm soát phiên bản để triển khai lại nhanh chóng.

---

## EXPECTED AWS COST BREAKDOWN BY SERVICES {#cost-breakdown}

| AWS Service                       | Monthly Estimated Cost (USD) |
| --------------------------------- | ---------------------------- |
| Amazon Bedrock                    | $21.61                       |
| AWS Lambda                        | $3.75                        |
| Amazon Simple Email Service (SES) | $2.25                        |
| Amazon DynamoDB                   | $1.52                        |
| Amazon Simple Storage Service     | $0.46                        |
| Amazon CloudWatch                 | $0.80                        |
| Amazon API Gateway                | $0.06                        |
| Amazon CloudFront                 | $0.00                        |
| Amazon Cognito                    | $0.00                        |
| Amazon EventBridge                | $0.00                        |
| Amazon IAM                        | $1.60                        |
| Amazon KMS                        | $1.03                        |
| **TOTAL MONTHLY COST**            | **$33.14**                   |
| **TOTAL YEARLY COST**             | **$397.79**                  |

---

## TEAM {#team}

| Name                     | Task                                                                | Role   | Email / Contact Info             |
| ------------------------ | ------------------------------------------------------------------- | ------ | -------------------------------- |
| Bùi Tấn Phát             | Dashboard, Manage Employee, Support, Content check                  | Leader | btfat3103@gmail.com              |
| Nguyễn Ngọc Long         | CRUD, Config Network / API Gateway, Test function, Slide            | Member | nguyenngoclong216@gmail.com      |
| Đặng Nguyễn Minh Duy     | Database, CloudWatch / CloudLogs, Paper, Slide                      | Member | dangnguyenminhduy11b08@gmail.com |
| Đỗ Đăng Khoa             | Log In/ Registration / Forget Password, UI / UX - Static Web, Paper | Member | khoado7577@gmail.com             |
| Nguyễn Huỳnh Thiên Quang | Auto Scoring, AI Assistant, Slide                                   | Member | quangkootenhatvutru@gmail.com    |

---

## RESOURCES & COST ESTIMATES {#resources-and-cost-estimates}

| Resource                  | Responsibility                                                                         | Rate (USD) / Hour |
| ------------------------- | -------------------------------------------------------------------------------------- | ----------------- |
| Full-Stack Developers [2] | React frontend, Python Lambda backend, API integration                                 | $66               |
| Cloud Engineers [3]       | AWS infrastructure setup, deployment automation, monitoring                            | $66               |
| Other (Please specify)    | Estimated platform consumption (Lambda, DynamoDB, Bedrock). Paper and present material | $0.01             |

**NOTE: Project Phase durations overlap each other.**

| Project Phase                            | Duration     | Man-Days         | Other (Please specify) | Estimated Cost            |
| ---------------------------------------- | ------------ | ---------------- | ---------------------- | ------------------------- |
| Phase 1: Foundation & Scoring Model      | 8 Weeks      | 80               | -                      | $42,246.40 (80 x $528.08) |
| Phase 2: Project Setup & Dashboard       | 2 Weeks      | 40               | -                      | $21,123.20 (40 x $528.08) |
| Phase 3: AI Agent & Absence Mgmt         | 1 Week       | 15               | -                      | $7,921.20 (15 x $528.08)  |
| Phase 4: Integration, Testing & Handover | 1 Week       | 15               | -                      | $7,921.20 (15 x $528.08)  |
| **Total Hours**                          | **12 Weeks** | **150 Man-Days** |                        | **$79,212.00**            |

**Cost Contribution distribution between Partner, Customer, AWS.**

| Party    | Contribution (USD) | % Contribution of Total |
| -------- | ------------------ | ----------------------- |
| Customer | 0                  | 0                       |
| Partner  | 0                  | 0                       |
| AWS      | 200                | 100                     |

---

## ACCEPTANCE {#acceptance}

**1. Project Acceptance Criteria**

Nền tảng InsightHR sẽ được coi là hoàn chỉnh và được chấp nhận khi các tiêu chí sau đây được đáp ứng.

**2. Completed Deliverables**

- Tất cả các tính năng chính được triển khai và triển khai sản xuất
- Quản lý người dùng và nhân viên với hoạt động hàng loạt
- Quản lý điểm hiệu suất với xem dựa trên lịch
- Hệ thống Attendance với đánh dấu absence tự động
- Bảng điều khiển tương tác với đồng hồ trực tiếp
- Chatbot AI với tích hợp Bedrock

**3. Key Metrics Achieved**

- 300+ tài khoản người dùng
- 300 bản ghi nhân viên trên 5 bộ phận
- 900+ điểm hiệu suất được theo dõi
- 9,300+ bản ghi tham dự
- Chi phí AWS hàng tháng: ~$33.14
- Thời gian hoạt động hệ thống: 99.9%+
- Zero critical security vulnerabilities

**4. Acceptance Status**

- Current Status: Application deployed in cloudfront Production URL: https://d2z6tht6rq32uy.cloudfront.net

**5. Next Steps**

- Sửa lỗi nhỏ và cập nhật tính năng
- Tiến hành kiểm tra chấp nhận của người dùng
- Cung cấp chuyển giao kiến thức và đào tạo
