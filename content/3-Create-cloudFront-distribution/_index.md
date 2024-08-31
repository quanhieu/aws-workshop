+++
title = "Set Up CloudFront to Speed Up Content Delivery"
date = 2024-05-14T00:38:32+07:00
weight = 3
chapter = false
pre = "<b>3. </b>"
+++

**Content:**

## Step 3: Set Up CloudFront to Speed Up Content Delivery

1. **Create a CloudFront Distribution**

   - Go to CloudFront in the AWS Management Console, select “Create Distribution.”
   - In the “Origin” section, select the S3 bucket created earlier as the origin source.
   - In “Origin access,” select "Origin Access Control (OAC)" to protect the S3 bucket, allowing access only from CloudFront.
   - Set other parameters such as Cache Policy and Viewer Protocol Policy (HTTP and HTTPS).

2. **Configure Other Settings**
   - **Default Root Object**: Set to `index.html` or your default file.
   - **Custom Domain** (if applicable): Set up a custom domain by using AWS Certificate Manager (ACM) to issue a free SSL certificate.

## Step 4: Update DNS with Route 53 (If Using a Custom Domain)

1. **Configure Record Sets in Route 53**
   - Point your domain to CloudFront by adding a Record Set with type CNAME or A (Alias).

## Step 5: Test and Finalize

1. Access the CloudFront URL to ensure the website is working properly.
2. Check page load speed and ensure all files are being distributed through CloudFront.
