---
title: "Worklog Tuần 2"
date: "2025-09-15"
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

**Thời gian: 15/09/2025 – 21/09/2025**

### Mục tiêu Tuần 2:

* Củng cố kiến thức nền tảng về điện toán đám mây.
* Học kiến trúc và các thành phần quan trọng của Amazon VPC (Virtual Private Cloud).
* Hiểu cách luồng mạng hoạt động bên trong VPC thông qua subnets, route tables, NAT Gateway và Internet Gateway.
* Nắm kiến thức cơ bản về Amazon EC2, các tính năng của nó và cách launch EC2 vào một VPC đã cấu hình.
* Thực hành cấu hình các thành phần mạng bằng AWS Console.

---

### Nhiệm vụ cần thực hiện trong tuần:

| Ngày | Nhiệm vụ | Ngày bắt đầu | Ngày hoàn thành | Tài liệu tham khảo |
| --- | ---- | ---------- | ---------------- | ------------------ |
| Thứ Hai | - Học các khái niệm cloud computing cơ bản qua video | 09/15/2025 | 09/15/2025 | YouTube cloud basics playlist |
| Thứ Ba | - Tham gia sự kiện CloudDay | 09/16/2025 | 09/16/2025 | — |
| Thứ Tư | - Thực hành cấu hình VPC và các thành phần: subnets, route tables, IGW, NAT Gateway | 09/17/2025 | 09/17/2025 | https://000003.awsstudygroup.com/ |
| Thứ Năm | - Học kiến thức EC2 cơ bản và cách launch EC2 vào VPC | 09/18/2025 | 09/18/2025 | https://000004.awsstudygroup.com/, YouTube EC2 tutorial |
| Thứ Sáu | - Họp nhóm và thống nhất ý tưởng dự án cuối khóa | 09/19/2025 | 09/19/2025 | — |

---

### Thành tựu Tuần 2:

#### **Kiến thức về Cloud Cơ bản**

* Hiểu rõ các khái niệm then chốt trong điện toán đám mây:
  * Cloud infrastructure là gì.  
  * Vì sao elasticity & scalability giúp tránh việc ứng dụng/website bị quá tải khi nhu cầu tăng đột biến.  
  * Vì sao cloud quan trọng trong bối cảnh công nghệ hiện đại, khi nhu cầu tăng nhưng không phải tổ chức nào cũng đủ chi phí cho hạ tầng vật lý.  

---

#### **Kiến thức về VPC (Virtual Private Cloud)**

* Có kinh nghiệm thực hành xây dựng một AWS VPC hoàn chỉnh:
  * Tạo public và private subnet.  
  * Hiểu cách **CIDR blocks** xác định dải IP trong VPC.  
  * Gắn **Internet Gateway (IGW)** để cấp Internet cho public subnet.  
  * Tạo **NAT Gateway** để cho private subnet truy cập Internet an toàn.  
  * Cấu hình **route tables** để điều hướng lưu lượng mạng và tăng cường bảo mật.  

* Hiểu logic định tuyến:
  * Public subnet → route qua IGW  
  * Private subnet → route qua NAT Gateway hoặc tài nguyên nội bộ  

* Hiểu lợi ích bảo mật của việc tách workloads thành public và private subnets.

---

#### **Kiến thức về EC2 (Elastic Compute Cloud)**

* Nắm được các khái niệm EC2 cơ bản:
  * Các loại instance (general-purpose, compute-optimized, memory-optimized, …)  
  * AMI (hệ điều hành và cấu hình nền tảng)  
  * SSH key pairs và xác thực  
  * Security Groups để kiểm soát traffic  

* Thực hành launch EC2 trong:
  * Một VPC đã chọn  
  * Một subnet cụ thể  
  * Với security groups và key pairs đã cấu hình  

