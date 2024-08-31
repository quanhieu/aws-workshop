+++
title = "Tạo và Cấu Hình S3 Bucket"
date = 2024-08-14T00:38:32+07:00
weight = 1
chapter = false
pre = "<b>1. </b>"
+++

**Nội dung:**

# Triển khai Website Tĩnh bằng Amazon S3 và CloudFront

Triển khai một website tĩnh bằng Amazon S3 và CloudFront là một giải pháp phổ biến, nhanh chóng và tiết kiệm chi phí. Hãy làm theo các bước dưới đây để bắt đầu:

## Bước 1: Tạo và Cấu Hình S3 Bucket

1. **Tạo S3 Bucket**

   - Truy cập vào AWS Management Console và chọn S3.
   - Nhấp vào “Create bucket.”
   - Đặt tên cho bucket (ví dụ: `ten-bucket-cua-ban`) và chọn khu vực phù hợp.
   - Tắt tùy chọn “Block all public access” để cho phép truy cập công khai vào bucket (hoặc sử dụng CloudFront để giới hạn truy cập).

2. **Tải lên Các File Của Website**

   - Sau khi tạo bucket, vào bucket và tải lên các file HTML, CSS, JavaScript, hình ảnh, v.v.

3. **Cấu Hình Bucket Thành Website Tĩnh**
   - Trong bucket, vào phần “Properties.”
   - Tìm mục “Static website hosting” và bật nó lên.
   - Chọn “Use this bucket to host a website” và chỉ định file index (ví dụ: `index.html`) và file lỗi (ví dụ: `404.html`).
