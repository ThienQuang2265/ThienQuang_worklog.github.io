---
title: "Blog Vận hành AWS Cloud – Quản lý AWS Config Rules with Remediation"
date: "2025-05-05"
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

{{% notice warning %}}
⚠️ **Lưu ý:** Bài viết dưới đây được giữ **nguyên văn 100%** theo yêu cầu của bạn.
{{% /notice %}}

# **Quản lý AWS Config Rules with Remediation với AWS Config Conformance Pack**

**Tác giả:** Eswar Sesha Sai Kamineni, Ravindra Kori, Samrat Lamichhane, và Prathik Chintha  
**Ngày:** 05 THÁNG 5 NĂM 2025  
**Chuyên mục:** Giao diện Dòng lệnh AWS, AWS Config, Quản lý hoạt động tập trung, Cấu hình, tuân thủ và kiểm toán, Công cụ Quản lý

---

# **Giới thiệu**
Các tổ chức phải đối mặt với các yêu cầu đặc thù trên các tài nguyên và tài khoản AWS của họ. Mặc dù AWS Config cung cấp các quy tắc được quản lý, nhiều tổ chức cần các quy tắc tùy chỉnh và khả năng khắc phục tự động có thể mở rộng trên toàn bộ Tài nguyên AWS của họ. Bài viết này trình bày cách sử dụng AWS Config custom conformance pack để triển khai và quản lý các quy tắc tùy chỉnh với các hành động khắc phục trên toàn tổ chức trong khi vẫn duy trì quyền kiểm soát tập trung.

---

# **Tổng quan về Giải pháp**
Giải pháp này triển khai một khung tuân thủ tập trung sử dụng:
- Các quy tắc tùy chỉnh của AWS Config với khả năng khắc phục tự động
- Các gói tuân thủ để triển khai trên toàn bộ tài nguyên
- Các hàm AWS Lambda để đánh giá
- AWS Systems Manager để khắc phục

![ình 1: SơH đồ kiến trúc](/images/Blog/blog2_1.png)

Quy tắc tùy chỉnh của AWS Config được cấu hình trong các tài khoản thành viên, gọi hàm Lambda đánh giá nằm trong tài khoản quản trị viên được ủy quyền của AWS.

Hàm Lambda đánh giá nằm trong tài khoản quản trị viên được ủy quyền sẽ đánh giá các tài nguyên mục tiêu (ví dụ: Nhóm bảo mật AWS EC2) theo các tiêu chí tuân thủ đã xác định trước và cập nhật kết quả đánh giá là “Tuân thủ” hoặc “Không tuân thủ” trong tài khoản thành viên của AWS Config.

Khi phát hiện các tài nguyên không tuân thủ trong tài khoản thành viên, quy tắc AWS Config sẽ tự động kích hoạt một quy trình khắc phục thông qua tài liệu Tự động hóa của AWS Systems Manager.

Tài liệu Tự động hóa của AWS Systems Manager sẽ kích hoạt một hàm Lambda được duy trì trong tài khoản quản trị viên được ủy quyền, thực thi các hành động đã xác định để đưa các tài nguyên vào trạng thái tuân thủ.

---

# **Các thành phần chính**

## **Tài khoản quản trị viên được ủy quyền lưu trữ:**
- Các hàm Lambda để đánh giá quy tắc và khắc phục
- Các logic quy tắc tùy chỉnh của AWS Config
- Các runbook Tự động hóa của Systems Manager

## **Các Tài khoản Thành viên gồm:**
- AWS Config đã được kích hoạt
- Quyền truy cập liên tài khoản để quản lý tập trung

Trong bài viết này, chúng tôi sẽ minh họa giải pháp bằng cách triển khai một quy trình kiểm soát tuân thủ kiểm tra đối với inbound rules của Nhóm bảo mật AWS EC2. Quy tắc này xác định và khắc phục các nhóm bảo mật cho phép truy cập từ các khối CIDR lớn hơn /16 (ví dụ: 10.0.0.0/10 hoặc 10.0.0.0/1).

---

# **Hướng dẫn triển khai**

## **Điều kiện tiên quyết**
- Xác minh quyền truy cập trong tài khoản quản trị viên được ủy quyền và tài khoản thành viên của AWS.
- Kích hoạt AWS Config trong tài khoản quản trị viên được ủy quyền và tài khoản thành viên.
- Ghi lại ID tài khoản quản trị viên được ủy quyền của AWS.

---

## **Bước 1: Triển khai tài nguyên trong tài khoản quản trị viên được ủy quyền**
- Tải xuống mẫu CloudFormation.
- Đăng nhập AWS Console → CloudFormation → Tạo stack.
- Upload template.

Ngăn xếp CloudFormation tạo ra:
- Hai Lambda: **ConformancePackSecurityGroup**, **AutomationSecurityGroupConformance**
- Ba vai trò IAM: **ConformancePackSecurityGroupLambdaRole**, **AutomationSecurityGroupConformanceLambdaRole**, **SSMDocumentRole**
- Document: **SecurityGroupAutomation SSMDocument**

---

## **Bước 2: Triển khai vai trò IAM liên tài khoản qua StackSets**
- Tải mẫu StackSet
- Triển khai lên OU AWS
- Nhập ID tài khoản quản lý

---

## **Bước 3: Cấu hình Quyền Lambda**
```bash
aws lambda add-permission \
  --function-name "ConformancePackSecurityGroupFunction" \
  --statement-id "AllowConfigCrossAccount" \
  --action "lambda:InvokeFunction" \
  --principal "config.amazonaws.com" \
  --source-account ${MEMBER_ACCOUNT_ID}
```

---

## **Bước 4: Chia sẻ Runbook Systems Manager**
```bash
aws ssm modify-document-permission \
  --name "SecurityGroupAutomationSSMDocument" \
  --permission-type Share \
  --account-ids-to-add "111111111111" "222222222222" "333333333333"
```

---

## **Bước 5: Triển khai Conformance Pack**
```bash
aws configservice put-organization-conformance-pack \
  --organization-conformance-pack-name "SecurityGroupConformancePack" \
  --template-body file://SecurityGroupConformancePack.yaml \
  --delivery-s3-bucket YOUR-S3-BUCKET-NAME \
  --conformance-pack-input-parameters \
      ParameterName=ManagementAccountId,ParameterValue=YOUR-Management-ACCOUNT-ID
```

---

# **Kiểm thử Giải pháp**
Tạo một nhóm bảo mật không tuân thủ:
- Tạo Security Group mới
- Thêm inbound rule SSH từ **10.0.0.0/8**
- Gắn tag nhận dạng

![Hình 2: Quy tắc đến của Nhóm Bảo mật Không tuân thủ](/images/Blog/blog2_2.png)

Sau vài phút:
- AWS Config đánh giá → trạng thái đổi sang **Không tuân thủ**

![Hình 3: Gói tuân thủ xác định các tài nguyên](/images/Blog/blog2_3.png)

- Quy tắc đến không tuân thủ được tự động loại bỏ
- Kiểm tra CloudWatch Logs cho cả hai Lambda

---

# **Dọn dẹp**
- Xóa conformance pack
- Xóa CloudFormation Stack
- Xóa bucket S3 nếu không cần

---

# **Kết luận**
Giải pháp cung cấp khả năng tuân thủ tự động trên toàn tổ chức với AWS Config, Lambda, Systems Manager và AWS Organizations. Đây là khung mở rộng, tự động phát hiện và sửa các cấu hình sai Security Group trên nhiều tài khoản AWS.
