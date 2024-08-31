+++
title = "Create and Configure the S3 Bucket"
date = 2024-08-14T00:38:32+07:00
weight = 1
chapter = false
pre = "<b>1. </b>"
+++

**Content:**

## Deploying a Static Website Using Amazon S3 and CloudFront

Deploying a static website using Amazon S3 and CloudFront is a popular, quick, and cost-effective solution. Follow the steps below to get started:

## Step 1: Create and Configure the S3 Bucket

1. **Create an S3 Bucket**

   - Go to the AWS Management Console and select S3.
   - Click “Create bucket.”
   - Name your bucket (e.g., `your-bucket-name`) and choose the appropriate region.
   - Disable the “Block all public access” option to allow public access to the bucket (or use CloudFront to restrict access).

2. **Upload Website Files**

   - After creating the bucket, go into the bucket and upload your HTML, CSS, JavaScript, images, etc.

3. **Configure the Bucket as a Static Website**
   - In the bucket, go to “Properties.”
   - Find the “Static website hosting” section and enable it.
   - Choose “Use this bucket to host a website” and specify the index document (e.g., `index.html`) and error document (e.g., `404.html`).
