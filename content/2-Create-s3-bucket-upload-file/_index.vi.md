+++
title = "Tạo và Cấu Hình S3 Bucket"
date = 2024-08-14T00:38:32+07:00
weight = 2
chapter = false
pre = "<b>2. </b>"
+++

### Bước 2: Tạo và Cấu Hình S3 Bucket

1. **Tạo S3 Bucket**

   - Truy cập vào AWS Management Console và chọn S3.
   - Nhấp vào “Create bucket.”
   - Đặt tên cho bucket (ví dụ: `ten-bucket-cua-ban`) và chọn khu vực phù hợp.

   ![Step 1](../../images/2-s3-static/1.step.png)

   - Tắt tùy chọn “Block all public access” để cho phép truy cập công khai vào bucket (hoặc sử dụng CloudFront để giới hạn truy cập).

   ![Step 2](../../images/2-s3-static/2.step.png)

2. **Tải lên Các File Của Website**

   - Sau khi tạo bucket, vào bucket và tải lên các file HTML, CSS, JavaScript, hình ảnh, v.v.

   ![Step 3](../../images/2-s3-static/4.step.png)

3. **Cấu Hình Bucket Thành Website Tĩnh**

   - Trong bucket, vào phần “Properties.”
   - Tìm mục “Static website hosting” và bật nó lên.

   ![Step 5](../../images/2-s3-static/5.step.png)

   - Chọn “Use this bucket to host a website” và chỉ định file index (ví dụ: `index.html`) và file lỗi (ví dụ: `404.html`).

   ![Step 6](../../images/2-s3-static/6.step.png)
