+++
title = "Create and Configure the S3 Bucket"
date = 2024-08-14T00:38:32+07:00
weight = 2
chapter = false
pre = "<b>2. </b>"
+++

### Step 2: Create and Configure the S3 Bucket

1. **Create an S3 Bucket**

   - Go to the AWS Management Console and select S3.
   - Click “Create bucket.”
   - Name your bucket (e.g., `your-bucket-name`) and choose the appropriate region.

   ![Step 1](./images/2-s3-static/1.step.png)

   - Disable the “Block all public access” option to allow public access to the bucket (or use CloudFront to restrict access).

   ![Step 2](./images/2-s3-static/2.step.png)

2. **Upload Website Files**

   - After creating the bucket, go into the bucket and upload your HTML, CSS, JavaScript, images, etc.

   ![Step 3](./images/2-s3-static/4.step.png)

3. **Configure the Bucket as a Static Website**

   - In the bucket, go to “Properties.”
   - Find the “Static website hosting” section and enable it.

   ![Step 5](./images/2-s3-static/5.step.png)

   - Choose “Use this bucket to host a website” and specify the index document (e.g., `index.html`) and error document (e.g., `404.html`).

   ![Step 6](./images/2-s3-static/6.step.png)
