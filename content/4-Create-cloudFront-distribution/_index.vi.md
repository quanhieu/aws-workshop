+++
title = "Thiết lập CloudFront để Tăng Tốc Độ Phân Phối Nội Dung"
date = 2024-05-14T00:38:32+07:00
weight = 4
chapter = false
pre = "<b>4. </b>"
+++

<!-- **Nội dung:** -->

### Bước 3: Thiết Lập CloudFront để Tăng Tốc Độ Phân Phối Nội Dung

1. **Cập Nhật S3 Permissions**

   - Chọn "Permission" -> Edit

     ![Bước 1](../../images/3-cloudfront-static/1.step.png)

   - Kích hoạt tùy chọn “Block all public access” để cho phép quyền truy cập công khai vào bucket.

     ![Bước 2](../../images/3-cloudfront-static/2.step.png)

   - Gõ "confirm" -> Save

     ![Bước 3](../../images/3-cloudfront-static/3.step.png)

2. **Tạo CloudFront Distribution**

   - Vào CloudFront trong AWS Management Console, chọn “Create Distribution.”
   - Trong phần “Origin”, chọn bucket S3 đã tạo trước đó.

     ![Bước 4](../../images/3-cloudfront-static/4.step.png)

   - Trong “Origin access”, chọn "Origin Access Control Setting" để bảo vệ bucket S3, chỉ cho phép truy cập từ CloudFront.

     ![Bước 5](../../images/3-cloudfront-static/5.step.png)

   - Chọn một Origin access control, nếu chưa có, chọn để tạo mới OAC

     ![Bước 6](../../images/3-cloudfront-static/6.step.png)

   - Chọn Web Application Firewall (WAF)

     ![Bước 7](../../images/3-cloudfront-static/7.step.png)

   <!-- - Thiết lập các tham số khác như Cache Policy và Viewer Protocol Policy (HTTP và HTTPS). -->

3. **Cấu Hình Các Cài Đặt Khác**

   - **Default Root Object**: Đặt thành `index.html` hoặc tệp mặc định của bạn.

     ![Bước 13](../../images/3-cloudfront-static/13.step.png)

   - **Custom Domain** (nếu có): Thiết lập một tên miền tùy chỉnh bằng cách sử dụng AWS Certificate Manager (ACM) để cấp phát chứng chỉ SSL miễn phí.

## Bước 4: Cập Nhật Chính Sách Bucket S3

1. **Sao Chép Chính Sách S3**

   - Chọn "Origins" -> Chọn Origin đầu tiên và Chọn Edit

     ![Bước 8](../../images/3-cloudfront-static/8.step.png)

   - Chọn Copy Policy

     ![Bước 9](../../images/3-cloudfront-static/9.step.png)

2. **Cập Nhật S3 Policy**

   - Quay lại S3

   - Vào tab “Permissions” > “Bucket Policy”

     ![Bước 10](../../images/3-cloudfront-static/10.step.png)

   - Edit -> Ctrl + V để dán Bucket Policy mới

     ![Bước 11](../../images/3-cloudfront-static/11.step.png)

3. **Xác Minh Quyền**

   - Quay lại CloudFront
   - Truy cập URL CloudFront để đảm bảo trang web hoạt động đúng cách.

     ![Bước 12](../../images/3-cloudfront-static/12.step.png)

   - Kiểm tra tốc độ tải trang và đảm bảo tất cả các tệp đang được phân phối qua CloudFront

     ![Bước 15](../../images/3-cloudfront-static/15.step.png)
