+++
title = "Triển khai Static Website trên S3 và CloudFront"
date = 2024
weight = 1
chapter = false
+++

# Triển khai Static Website trên S3 và CloudFront

## Tại sao cần triển khai Website Tĩnh bằng Amazon S3 và CloudFront?

### Hiệu suất và Tốc độ Tải Trang Cao:

- **S3** lưu trữ tệp tĩnh (HTML, CSS, JS) trên nền tảng đám mây với khả năng mở rộng tự động và truy cập nhanh chóng.
- **CloudFront** là một Content Delivery Network (CDN) giúp phân phối nội dung tới người dùng từ các máy chủ gần nhất, giảm độ trễ và tăng tốc độ tải trang.

### Tiết Kiệm Chi Phí:

- Triển khai website tĩnh trên **S3** có chi phí thấp, chỉ tính phí dựa trên dung lượng lưu trữ và băng thông sử dụng, không yêu cầu quản lý máy chủ phức tạp.
- **CloudFront** giúp tối ưu hóa băng thông bằng cách lưu trữ nội dung cache gần người dùng, giảm số lần truy cập trực tiếp vào S3, từ đó giảm chi phí.

### Khả Năng Mở Rộng Vượt Trội:

- **S3** và **CloudFront** tự động xử lý lưu lượng truy cập lớn mà không cần cấu hình phức tạp, phù hợp với các website có nhu cầu tăng trưởng nhanh.
- Không cần lo lắng về việc quá tải máy chủ khi có nhiều người truy cập cùng lúc.

### Bảo Mật Nâng Cao:

- **CloudFront** cho phép thiết lập HTTPS, bảo vệ dữ liệu khi truyền qua mạng.
- Sử dụng **Origin Access Control (OAC)** để đảm bảo chỉ CloudFront mới có quyền truy cập vào S3, giúp bảo vệ dữ liệu khỏi truy cập trái phép.
- AWS cung cấp các tùy chọn bảo mật nâng cao như **AWS WAF (Web Application Firewall)** và **Shield** để bảo vệ website khỏi các tấn công DDoS.

### Dễ Dàng Quản Lý và Tự Động Hóa:

- Cấu hình, triển khai, và quản lý website tĩnh rất đơn giản qua AWS Console hoặc bằng cách sử dụng **Infrastructure as Code** với AWS CloudFormation hoặc Terraform.
- AWS cung cấp tính năng tự động sao lưu và phục hồi, giúp đảm bảo tính liên tục của dịch vụ.

### Khả Năng Kết Hợp với Các Dịch Vụ AWS Khác:

- Dễ dàng tích hợp với **AWS Lambda**, **API Gateway**, hoặc **AWS Amplify** để tạo nên ứng dụng web phức tạp hơn từ nền tảng tĩnh.
- Có thể sử dụng **AWS IAM** để quản lý quyền truy cập, cung cấp thêm mức độ kiểm soát bảo mật.

## Lợi ích của việc sử dụng S3 và CloudFront:

- **Tốc Độ Phản Hồi Nhanh Hơn**: Nội dung được phân phối từ các edge location gần người dùng nhất thông qua CloudFront, giảm thời gian tải trang.
- **Bảo Mật Dữ Liệu và Quyền Truy Cập**: Các thiết lập bảo mật giúp kiểm soát tốt hơn ai có thể truy cập vào nội dung.
- **Độ Tin Cậy Cao**: Dịch vụ của AWS có SLA cao, đảm bảo tính sẵn sàng của website.
- **Tối Ưu SEO và Trải Nghiệm Người Dùng**: Tốc độ tải trang nhanh giúp cải thiện xếp hạng SEO và trải nghiệm tổng thể cho người dùng.
- **Không Cần Bảo Trì Phức Tạp**: Không phải lo lắng về việc bảo trì máy chủ hay cập nhật phần mềm định kỳ, giảm tải công việc cho đội ngũ phát triển.

Việc triển khai website tĩnh bằng S3 và CloudFront không chỉ đơn giản, tiết kiệm mà còn mang lại một trải nghiệm web nhanh, bảo mật và ổn định cho người dùng!

#### Main Content

1. [Chuẩn bị source code](1-Prepare-source-code/)
2. [Tạo và Cấu Hình S3 Bucket](2-Create-s3-bucket-upload-file/)
3. [Thiết Lập Quyền Truy Cập](3-Config-permission-s3-bucket/)
4. [Thiết Lập CloudFront Để Tăng Tốc Độ Phân Phối Nội Dung](4-Create-cloudFront-distribution/)
<!-- need to remove parenthesis for path in Hugo 0.88.1 for Windows-->
