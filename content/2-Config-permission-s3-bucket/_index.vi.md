+++
title = "Thiết Lập Quyền Truy Cập"
date = 2024-05-14T00:38:32+07:00
weight = 2
chapter = false
pre = "<b>2. </b>"
+++

## Bước 2: Thiết Lập Quyền Truy Cập

1. **Cấu Hình Bucket Policy Để Cho Phép Truy Cập Công Khai**

   - Vào tab “Permissions” > “Bucket Policy” và thêm chính sách sau để cho phép truy cập công khai:

     ```json
     {
       "Version": "2012-10-17",
       "Statement": [
         {
           "Sid": "PublicReadGetObject",
           "Effect": "Allow",
           "Principal": "*",
           "Action": "s3:GetObject",
           "Resource": "arn:aws:s3:::ten-bucket-cua-ban/*"
         }
       ]
     }
     ```

2. **Kiểm Tra Quyền Truy Cập**
   - Đảm bảo các file trong bucket có thể được truy cập công khai qua URL trực tiếp.
