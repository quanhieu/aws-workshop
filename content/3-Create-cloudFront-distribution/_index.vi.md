+++
title = "Thiết Lập CloudFront Để Tăng Tốc Độ Phân Phối Nội Dung"
date = 2024-05-14T00:38:32+07:00
weight = 3
chapter = false
pre = "<b>3. </b>"
+++

**Nội dung:**

## Bước 3: Thiết Lập CloudFront Để Tăng Tốc Độ Phân Phối Nội Dung

1. **Tạo CloudFront Distribution**

   - Truy cập CloudFront trong AWS Management Console, chọn “Create Distribution.”
   - Trong phần “Origin”, chọn bucket S3 đã tạo ở trên làm nguồn gốc.
   - Trong “Origin access,” chọn "Origin Access Control (OAC)" để bảo vệ bucket S3, chỉ cho phép truy cập từ CloudFront.
   - Thiết lập các thông số khác như Cache Policy và Viewer Protocol Policy (HTTP và HTTPS).

2. **Cấu Hình Các Thiết Lập Khác**
   - **Default Root Object**: Đặt `index.html` hoặc file mặc định của bạn.
   - **Tên Miền Tùy Chỉnh** (nếu có): Cấu hình tên miền tùy chỉnh bằng AWS Certificate Manager (ACM) để cấp chứng chỉ SSL miễn phí.

## Bước 4: Cập Nhật DNS với Route 53 (Nếu Sử Dụng Tên Miền Tùy Chỉnh)

1. **Cấu Hình Record Sets Trong Route 53**
   - Trỏ tên miền đến CloudFront bằng cách thêm Record Set với loại là CNAME hoặc A (Alias).

## Bước 5: Kiểm Tra và Hoàn Thiện

1. Truy cập vào URL của CloudFront để đảm bảo website hoạt động bình thường.
2. Kiểm tra tốc độ tải trang và đảm bảo mọi file được phân phối qua CloudFront.
