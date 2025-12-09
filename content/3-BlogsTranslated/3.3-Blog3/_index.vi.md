---

title: "MasterClass nâng cao chất lượng video và giảm chi phí với AWS Media Services"
date: "2025-03-25"
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
----------------------

# MasterClass nâng cao chất lượng video và giảm chi phí với các Dịch vụ AWS Media

**Tác giả:** Dan Gehred và Matt Carter
**Ngày:** 25 tháng 3, 2025
**Chuyên mục:** Amazon CloudFront, AWS Elemental MediaConvert, Direct-to-Consumer & Streaming, Media & Entertainment, Media Services, Content Delivery & Networking

---

## Giới thiệu

Đối với nhiều người, nấu ăn cùng Gordon Ramsay hay viết lách với Shonda Rhimes có vẻ như chỉ là giấc mơ. Tuy nhiên, MasterClass đã biến điều đó thành hiện thực với hơn 200 lớp học được giảng dạy bởi những người giỏi nhất thế giới. Với video là trọng tâm trải nghiệm, MasterClass đã sử dụng các dịch vụ Media của AWS để hỗ trợ sự tăng trưởng nhanh chóng của họ.

Công ty hiện sử dụng **AWS Elemental MediaConvert** và **Amazon CloudFront**, với Nomad Media làm lớp điều phối, giúp tối ưu chuyển mã và phân phối nội dung video. Sau khi di chuyển hạ tầng video sang AWS, MasterClass ghi nhận **chất lượng video cải thiện đáng kể**, đồng thời **giảm hơn một nửa chi phí video**.

![Masterclass](/images/Blog/blog_3.jpg)

## Cải thiện hiệu quả chuyển mã với AWS Elemental MediaConvert

Khi ra mắt năm 2015, MasterClass chọn giải pháp video turnkey. Tuy nhiên, khi thư viện nội dung mở rộng, công ty cần một hệ thống linh hoạt và có khả năng mở rộng tốt hơn.

MediaConvert — đặc biệt là tính năng **Quality-Defined Variable Bitrate (QVBR)** — trở thành lựa chọn tối ưu. QVBR tự động phân bổ bitrate để tối ưu chất lượng hình ảnh trên mọi loại thiết bị. Trước đây, MasterClass phải dùng FFmpeg trước khi chuyển mã, gây ra quá trình nén hai lần và giảm chất lượng. Với MediaConvert, họ gửi file gốc trực tiếp, giúp:

* Tăng chất lượng video
* Giảm lỗi hình ảnh (artifacts)
* Đưa nội dung đến người xem nhanh hơn

---

## Di chuyển liền mạch và tối ưu phân phối nội dung

Nomad Media hỗ trợ lớp điều phối giúp song song hóa các workflow, đảm bảo di chuyển mượt mà.

"Chúng tôi đã chuyển mã lại toàn bộ thư viện để nâng cấp nội dung cũ với QVBR," Phipps chia sẻ. Nhờ hạ tầng không máy chủ của AWS, họ hoàn thành việc chuyển mã khối lượng lớn chỉ **trong vài ngày**.

Về phân phối, MasterClass thử nhiều CDN khác nhau và nhận thấy:

* CloudFront hoạt động tốt nhất hoặc tương đương lựa chọn khác
* Tích hợp dễ dàng vì đã sử dụng AWS
* Không có chi phí tiêu thụ từ lưu trữ — giúp tối ưu chi phí

Kết hợp CloudFront với **Lambda@Edge**, MasterClass tối ưu hệ thống xác thực token, giữ nguyên đường dẫn nội dung, tăng tính ổn định cache.

---

## Hướng tới tương lai với AWS

Giờ đây làm chủ hoàn toàn ngăn xếp video của mình, MasterClass có thể:

* Tuỳ chỉnh workflow media
* Tích hợp phân tích video dựa trên AI
* Mở rộng sang livestream tương tác thời gian thực

AWS cung cấp nền tảng linh hoạt và mạnh mẽ để hỗ trợ mọi đổi mới trong tương lai.

"AWS mang lại sự linh hoạt cần thiết để chúng tôi xây dựng giải pháp bền vững, hỗ trợ sự phát triển không ngừng," Phipps chia sẻ.

---

**Tìm hiểu thêm:** Khám phá các giải pháp tối ưu hoá workflow video hoặc liên hệ đại diện ngành Truyền thông & Giải trí của AWS để được tư vấn.
