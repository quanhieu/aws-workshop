+++
title = "Chuẩn bị source code"
date = 2024-08-14T00:38:32+07:00
weight = 1
chapter = false
pre = "<b>1. </b>"
+++

## Triển khai Website Tĩnh bằng Amazon S3 và CloudFront

Triển khai một website tĩnh bằng Amazon S3 và CloudFront là một giải pháp phổ biến, nhanh chóng và tiết kiệm chi phí. Hãy làm theo các bước dưới đây để bắt đầu:

### Bước 1: Chuẩn bị source code

1. **Init source code**

   ```
     npx create-next-app
   ```

   ![Step 1](../../images/1-prepare-nextjs/1.step.png)

2. **Test source**

   ```
     pnpm dev
     or
     yarn dev
   ```

   ![Step 2](../../images/1-prepare-nextjs/2.step.png)

- Kiểm tra `https://localhost:3000`

  ![Step 3](../../images/1-prepare-nextjs/3.step.png)

3. **Build source**

   ```
     pnpm build
     or
     yarn build
   ```

   ![Step 4](../../images/1-prepare-nextjs/4.step.png)
