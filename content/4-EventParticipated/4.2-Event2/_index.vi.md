---
title: "Workshop: Khoa học dữ liệu trên AWS"
weight: 3
chapter: false
pre: " <b> 4.3. </b> "
---

# **Workshop: Khoa học dữ liệu trên AWS**

**Địa điểm**: Trường Đại học FPT, cơ sở TP.HCM

**Ngày**: Thứ Năm, 16 tháng 10, 2025

### Mục tiêu sự kiện

- Khám phá toàn bộ hành trình xây dựng hệ thống Khoa học Dữ liệu hiện đại, từ lý thuyết đến thực hành
- Nắm vững **quy trình Khoa học Dữ liệu end-to-end** trên AWS, bao gồm lưu trữ, xử lý và triển khai mô hình
- Có kinh nghiệm thực tiễn với dữ liệu thực (IMDb) và mô hình áp dụng (Phân tích cảm xúc)
- Phân tích sự đánh đổi giữa **hạ tầng Cloud và On-premise** về chi phí và hiệu năng

---

### Danh sách diễn giả

- **Văn Hoàng Kha** – Kiến trúc sư giải pháp Cloud, AWS Community Builder
- **Bạch Doãn Vương** – Kỹ sư DevOps Cloud, AWS Community Builder

---

### Nội dung chính

#### 1. Vai trò của Cloud trong Khoa học Dữ liệu và Tổng quan quy trình

- **Tầm quan trọng của Cloud**: Giới thiệu cách dịch vụ Cloud như AWS giúp lập trình viên đơn giản hóa pipeline xử lý dữ liệu và đồng thời tiết kiệm chi phí
- **Quy trình Khoa học Dữ liệu trên AWS**:
  - **Lưu trữ**: Sử dụng **Amazon S3** làm nền tảng data lake trung tâm
  - **ETL/Xử lý**: Dùng **AWS Glue** cho các tác vụ tích hợp dữ liệu serverless
  - **Mô hình hóa**: Sử dụng **Amazon SageMaker** làm trung tâm xây dựng, huấn luyện và triển khai mô hình
  - Tổng quan hệ sinh thái AI/ML rộng lớn của AWS, bao gồm dịch vụ AI, dịch vụ ML, và hạ tầng

#### 2. Trình diễn thực hành

- **Demo 1: Xử lý dữ liệu với AWS Glue**:
  - **Kịch bản**: Xử lý và làm sạch dữ liệu thô từ dataset IMDb
  - **Kỹ thuật**: Trình bày cách feature engineering và chuẩn bị dữ liệu hiệu quả. Workshop nhấn mạnh nhiều phương pháp, từ low-code như **SageMaker Canvas** đến code-first sử dụng Numpy/Pandas
- **Demo 2: Phân tích cảm xúc với SageMaker**:
  - **Kịch bản**: Huấn luyện và triển khai mô hình Machine Learning để phân tích cảm xúc từ dữ liệu văn bản
  - **Quy trình**: Minh họa vòng "Train, Tune, Deploy" trong **SageMaker Studio**. Buổi học cũng giới thiệu khái niệm "Bring Your Own Model (BYOM)", cho thấy tính linh hoạt với TensorFlow và PyTorch

#### 3. Thảo luận chiến lược

- **Cloud vs On-Premise**: Thảo luận sâu về tối ưu chi phí và hiệu năng. Nội dung nhấn mạnh cloud elasticity giúp thử nghiệm khối lượng công việc lớn mà không cần đầu tư phần cứng lớn cho on-premise
- **Hướng dẫn dự án nhỏ**: Giới thiệu dự án áp dụng sau workshop để củng cố kỹ năng học được

---

### Những điều tôi học được

#### Quy trình kỹ thuật

- **Quy trình thống nhất**: Với các dịch vụ AI phong phú từ cloud, việc xây dựng ứng dụng AI trở nên đơn giản hơn, giảm độ phức tạp lý thuyết trừu tượng
- **Chọn công cụ phù hợp**: Học cách chọn công cụ thích hợp cho từng kịch bản (Amazon Transcribe, Amazon Textract) và cân nhắc chi phí để quản lý dự án

#### Ứng dụng trong ngành

- Áp dụng quy trình, dịch vụ AWS vào các dự án thực tế, tăng khả năng xử lý dữ liệu và triển khai mô hình

---

### Ứng dụng tại công việc

- **Sử dụng AWS Glue**: Đề xuất chuyển các script ETL cục bộ sang AWS Glue để tự động hóa xử lý dữ liệu serverless trên dataset lớn
- **Triển khai SageMaker**: Di chuyển mô hình thử nghiệm từ Jupyter notebooks sang **SageMaker Studio** để chuẩn hóa quy trình huấn luyện và triển khai
- **Thực hiện dự án**: Thực hiện dự án nhỏ sau workshop để củng cố hiểu biết về quy trình xử lý dữ liệu IMDb

---

### Trải nghiệm sự kiện

Workshop **"Khoa học dữ liệu trên AWS"** cho thấy Cloud đã đưa quá trình xây dựng ứng dụng AI gần hơn với cả doanh nghiệp và người dùng.

- Với sự phát triển nhanh của AI, doanh nghiệp cần thích ứng nhanh. Tuy nhiên, triển khai ứng dụng AI đòi hỏi nhiều tính toán, nhưng nhờ dịch vụ Cloud như AWS, quá trình này trở nên dễ dàng hơn.
- Các dịch vụ như Textract, Transcribe, Bedrock… giúp doanh nghiệp và người dùng cá nhân xây dựng ứng dụng AI với chi phí thấp hơn và đặc biệt giảm độ phức tạp

#### Một số hình ảnh từ sự kiện
![Ảnh 1](/images/Data_Science_1.jpg)
![Ảnh 2](/images/Data_Science_2.jpg)
![Ảnh 3](/images/Data_Science_3.jpg)
![Ảnh 4](/images/Data_Science_4.jpg)
![Ảnh 5](/images/Data_Science_5.jpg)

> Tổng quan, workshop cung cấp một framework Khoa học Dữ liệu toàn diện, nhấn mạnh tầm quan trọng của các công cụ quản lý AWS để đạt tính linh hoạt, khả năng mở rộng và tối ưu chi phí.
