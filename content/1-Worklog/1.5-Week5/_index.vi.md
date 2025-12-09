---
title: "Worklog tuần 5"
date: "2025-10-06"
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

**Thời gian: 6 tháng 10 – 12 tháng 10, 2025**

### Mục tiêu Tuần 5:

- Kiểm tra các mô hình ML để xác định kiến trúc phù hợp nhất với bộ dữ liệu (XGBoost vs Neural Network)  
- Hiểu lý do vì sao XGBoost luôn vượt trội trên dữ liệu dạng bảng (tabular)  
- Học kiến thức nền tảng về NoSQL và DynamoDB, và cách chúng hỗ trợ các ứng dụng có khả năng mở rộng  
- Xây dựng mô hình XGBoost baseline cho project cuối  

### Các nhiệm vụ thực hiện trong tuần:

| Ngày               | Nhiệm vụ                                                                                                                                                                                                                   | Ngày Bắt Đầu | Ngày Hoàn Thành | Tài Liệu Tham Khảo                                         |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|------------------|-------------------------------------------------------------|
| Thứ Hai           | - **Kiểm thử kiến trúc mô hình:** <br>&emsp; + So sánh XGBoost và Neural Network <br>&emsp; + Đánh giá thời gian train, mức độ overfitting và performance khi validation                                                   | 06/10/2025   | 06/10/2025       | ML Model Comparison Notes                                   |
| Thứ Ba            | - **Lý do XGBoost vượt trội:** <br>&emsp; + Nghiên cứu ưu điểm của mô hình cây quyết định <br>&emsp; + Đọc nghiên cứu so sánh XGBoost và deep learning trên dữ liệu tabular                                              | 07/10/2025   | 07/10/2025       | https://arxiv.org/pdf/2207.08815                            |
| Thứ Tư - Thứ Năm  | - **Khám phá DynamoDB & NoSQL:** <br>&emsp; + Học nền tảng NoSQL <br>&emsp; + Hiểu mô hình mở rộng (scalability) của DynamoDB <br>&emsp; + Học về partition key, sort key, RCU/WCU và chiến lược autoscaling           | 08/10/2025   | 09/10/2025       | https://www.youtube.com/watch?v=0buKQHokLK8                 |
| Thứ Sáu           | - **Mô hình XGBoost baseline:** <br>&emsp; + Xây dựng mô hình baseline <br>&emsp; + Tuning hyperparameter <br>&emsp; + Ghi nhận các metrics để so sánh mô hình sau này                                                    | 10/10/2025   | 10/10/2025       | XGBoost Documentation                                       |

### Thành tựu Tuần 5:

- **Hoàn thành so sánh mô hình:**
  - Đã kiểm thử hiệu năng giữa XGBoost và Neural Network  
  - Xác định kiến trúc phù hợp nhất dựa trên độ chính xác, sự ổn định và tốc độ huấn luyện  

- **Hiểu rõ sức mạnh của XGBoost:**
  - Học được lý do mô hình cây vượt trội hơn deep learning trên dữ liệu tabular  
  - Hiểu cách XGBoost xử lý tương tác đặc trưng, dữ liệu không đồng nhất và lợi thế của boosting  

- **Kiến thức NoSQL & DynamoDB:**
  - Nắm được nguyên lý NoSQL và khả năng mở rộng  
  - Học các khái niệm cốt lõi của DynamoDB: partitioning, RCU/WCU, chế độ on-demand, global tables  
  - Biết khi nào nên dùng NoSQL thay vì cơ sở dữ liệu quan hệ  

- **Hoàn thành mô hình XGBoost baseline:**
  - Xây dựng và kiểm thử mô hình baseline  
  - Tuning hyperparameters và ghi lại metrics  
  - Tạo nền tảng vững chắc cho việc training và tối ưu mô hình sau này  

- **Năng lực kỹ thuật đạt được:**
  - So sánh và lựa chọn mô hình  
  - Hiểu lý thuyết mô hình cây  
  - Thiết kế cơ sở dữ liệu NoSQL  
  - Làm việc thực tế với DynamoDB  
  - Quy trình phát triển mô hình ML baseline  
