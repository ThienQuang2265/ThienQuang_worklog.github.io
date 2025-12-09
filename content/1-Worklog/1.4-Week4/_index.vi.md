---
title: "Worklog tuần 4"
date: "2025-09-29"
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

**Thời gian: 29 tháng 9 – 5 tháng 10, 2025**

### Mục tiêu Tuần 4:

- Chuẩn bị bộ dữ liệu cuối cùng cho việc huấn luyện mô hình ML  
- Học các kiến thức cơ bản về AWS Lambda và cách Lambda giúp giảm chi phí trong kiến trúc serverless  
- Làm sạch và hoàn thiện bộ dữ liệu trước khi huấn luyện  
- Học về CloudTrail và CloudWatch, bao gồm sự khác nhau và các trường hợp sử dụng  
- Tìm hiểu cấu trúc và nguyên lý hoạt động của mô hình Transformer  

### Các nhiệm vụ thực hiện trong tuần:

| Ngày       | Nhiệm vụ                                                                                                                                                                                         | Ngày Bắt Đầu | Ngày Hoàn Thành | Tài Liệu Tham Khảo                                 |
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|------------------|----------------------------------------------------|
| Thứ Hai      | - **Khám phá AWS Lambda:** <br>&emsp; + Hiểu về Lambda và mô hình tính toán theo sự kiện <br>&emsp; + Xác định các trường hợp sử dụng Lambda để giảm chi phí cho project cuối                 | 29/09/2025 | 29/09/2025       | AWS Lambda Docs                                    |
| Thứ Ba       | - **Làm sạch dữ liệu cuối:** <br>&emsp; + Làm sạch bộ dữ liệu <br>&emsp; + Loại bỏ nhiễu/outliers <br>&emsp; + Đảm bảo tính nhất quán trước khi huấn luyện                                      | 30/09/2025 | 30/09/2025       | Project Dataset Guidelines                         |
| Thứ Tư - Thứ Năm     | - **CloudTrail & CloudWatch:** <br>&emsp; + Học tính năng audit của CloudTrail <br>&emsp; + Học CloudWatch metrics/logs/alarms <br>&emsp; + Hiểu sự khác nhau giữa hai dịch vụ | 01/10/2025 | 02/10/2025       | https://www.youtube.com/watch?v=S5X0PnBwp9I        |
| Thứ Sáu         | - **Học mô hình Transformer:** <br>&emsp; + Học kiến trúc Transformer <br>&emsp; + Nghiên cứu cơ chế Attention và pipeline Encoder–Decoder                                            | 03/10/2025 | 03/10/2025       | https://www.youtube.com/watch?v=biveB0gOlak&t=5779s |

### Thành tựu Tuần 4:

- **Chuẩn bị bộ dữ liệu cuối cùng:**
  - Tạo ra bộ dữ liệu tổng hợp chất lượng cao, sát thực tế  
  - Đảm bảo phân phối chuẩn cho các đặc trưng chính  
  - Loại bỏ các spikes bất thường và dữ liệu không nhất quán  
  - Bộ dữ liệu đã sẵn sàng để huấn luyện mô hình  

- **Kiến thức AWS Lambda:**
  - Hiểu mô hình tính toán theo sự kiện của Lambda  
  - Biết cách Lambda giúp giảm chi phí so với EC2 luôn bật  
  - Xác định được cách tích hợp Lambda vào project cuối  

- **Kiến thức về CloudTrail & CloudWatch:**
  - Hiểu CloudTrail dùng để theo dấu và audit hoạt động tài khoản  
  - Hiểu CloudWatch dùng để theo dõi metrics và logs  
  - Nắm rõ sự khác biệt và cách hai dịch vụ bổ trợ cho nhau  

- **Kiến thức cơ bản về Transformer:**
  - Học cơ chế Self-attention và Multi-head Attention  
  - Hiểu quy trình Encoder/Decoder và Positional Encoding  
  - Nhận thức được lý do Transformer vượt trội hơn RNN  
