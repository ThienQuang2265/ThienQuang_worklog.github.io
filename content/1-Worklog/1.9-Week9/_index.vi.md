---
title: "Worklog tuần 9"
date: "2025-11-03"
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

**Khoảng thời gian tuần: 3 – 9 tháng 11, 2025**

### Mục tiêu tuần 9:

- Triển khai mô hình auto_scoring vào môi trường AWS.
- Học cách Lambda Layer hoạt động và cách đóng gói dependencies.
- Thực hành build Docker image và đẩy lên Amazon ECR.
- Triển khai mô hình thành công bằng Lambda sử dụng ECR container.

### Các nhiệm vụ thực hiện trong tuần:

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | -------- | ------------- | ---------------- | ------------------ |
| Thứ Hai | - Triển khai mô hình auto_scoring lên môi trường AWS <br> &emsp;+ Kiểm tra inference cơ bản | 03/11/2025 | 03/11/2025 | Project Docs |
| Thứ Ba–Thứ Tư | - Học quản lý dependencies cho Lambda <br> &emsp;+ Tạo Lambda layers <br> &emsp;+ Kiểm tra giới hạn kích thước <br> &emsp;+ Tìm hiểu các phương pháp triển khai thay thế | 04/11/2025 | 05/11/2025 | AWS Lambda Docs |
| Thứ Năm | - Build Docker image cho mô hình <br> - Đẩy image lên Amazon ECR <br> - Cấu hình IAM permissions | 06/11/2025 | 06/11/2025 | AWS ECR Docs |
| Thứ Sáu | - Deploy Lambda bằng container từ ECR <br> - Chạy kiểm thử inference của mô hình | 07/11/2025 | 07/11/2025 | AWS Lambda + ECR Docs |

### Kết quả đạt được tuần 9:

- Hiểu giới hạn kích thước của Lambda Layers.
- Đóng gói mô hình ML thành công bằng Docker image.
- Đẩy image lên Amazon ECR và triển khai lên Lambda.
- Triển khai hoàn chỉnh mô hình auto_scoring trong AWS bằng container.
- Hiểu vai trò quan trọng của ECR đối với các mô hình ML lớn có nhiều dependencies.
