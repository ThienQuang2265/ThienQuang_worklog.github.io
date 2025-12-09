---
title: "Worklog tuần 11"
date: "2025-11-17"
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

**Khoảng thời gian: 17 – 23 tháng 11, 2025**

### Mục tiêu tuần 11:

- Thử triển khai hệ thống RAG lên môi trường AWS.
- Khám phá nhiều chiến lược triển khai (Lambda layer, container ECR).
- Nghiên cứu tính năng và chi phí của Bedrock Knowledge Base.
- Đánh giá xem Bedrock Knowledge Base có phải lựa chọn tốt hơn so với tự triển khai RAG thủ công hay không.

### Các nhiệm vụ thực hiện trong tuần:

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | -------- | ------------- | ---------------- | ------------------ |
| Thứ Hai |- Tham gia sự kiện AWS Mastery 2: AWS DevOps & Modern Operations  <br> | 17/11/2025 | 17/11/2025 | Project Docs |
| Thứ Ba | - Thử triển khai hệ thống RAG lên AWS <br> &emsp;+ Thiết lập Lambda ban đầu | 18/11/2025 | 18/11/2025 | Project Docs |
| Thứ Tư-Thứ Năm | - Thử nhiều phương pháp triển khai <br> &emsp;+ Lambda layer (kiểm thử dependencies) <br> &emsp;+ Xây dựng và deploy container ECR <br> &emsp;+ Debug lỗi dependency | 19/11/2025 | 20/11/2025 | AWS Lambda + ECR Docs |
| Thứ Sáu | - Nghiên cứu Amazon Bedrock Knowledge Base <br> - Tìm hiểu pricing và kiến trúc <br> - So sánh với phương pháp RAG thủ công | 21/11/2025 | 21/11/2025 | Bedrock Docs |

### Kết quả đạt được tuần 11:

- Hiểu rõ các vấn đề triển khai do dependency nặng trong pipeline RAG.
- Nhận ra Lambda layer và container ECR gây phức tạp và có giới hạn kích thước.
- Chuyển hướng sang sử dụng Bedrock Knowledge Base thay vì triển khai RAG thủ công.
- Nắm được chi phí và cách Knowledge Base đơn giản hóa quá trình ingestion và truy xuất.
- Học các kiến thức cơ bản về DevOps và các dịch vụ AWS hỗ trợ như ECS, ECR