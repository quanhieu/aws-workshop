+++
title = "Set Up CloudFront to Speed Up Content Delivery"
date = 2024-05-14T00:38:32+07:00
weight = 4
chapter = false
pre = "<b>4. </b>"
+++

<!-- **Content:** -->

### Step 3: Set Up CloudFront to Speed Up Content Delivery

1. **Update S3 Permissions**

   - Choose "Permission" -> Edit

     ![Step 1](./images/3-cloudfront-static/1.step.png)

   - Enable the “Block all public access” option to allow public access to the bucket.

     ![Step 2](./images/3-cloudfront-static/2.step.png)

   - Type "confirm" -> Save

     ![Step 3](./images/3-cloudfront-static/3.step.png)

2. **Create a CloudFront Distribution**

   - Go to CloudFront in the AWS Management Console, select “Create Distribution.”
   - In the “Origin” section, select the S3 bucket created earlier as the origin source.

     ![Step 4](./images/3-cloudfront-static/4.step.png)

   - In “Origin access” select "Origin Access Control Setting" to protect the S3 bucket, allowing access only from CloudFront.

     ![Step 5](./images/3-cloudfront-static/5.step.png)

   - Select an origin access control, if have not any select, create new OAC

     ![Step 6](./images/3-cloudfront-static/6.step.png)

   - Select Web Application Firewall (WAF)

     ![Step 7](./images/3-cloudfront-static/7.step.png)

   <!-- - Set other parameters such as Cache Policy and Viewer Protocol Policy (HTTP and HTTPS). -->

3. **Configure Other Settings**

   - **Default Root Object**: Set to `index.html` or your default file.

     ![Step 13](./images/3-cloudfront-static/13.step.png)

   - **Custom Domain** (if applicable): Set up a custom domain by using AWS Certificate Manager (ACM) to issue a free SSL certificate.

## Step 4: Update S3 Bucket Policy

1. **Copy S3 policy**

   - Choose "Origin" -> Select one and Choose Edit

     ![Step 8](./images/3-cloudfront-static/8.step.png)

   - Choose Copy Policy

     ![Step 9](./images/3-cloudfront-static/9.step.png)

2. **Update 53 policy**

   - Turn back to S3

   - Go to the “Permissions” tab > “Bucket Policy”

     ![Step 10](./images/3-cloudfront-static/10.step.png)

   - Edit -> Ctrl + V to parse new bucket Policy

     ![Step 11](./images/3-cloudfront-static/11.step.png)

3. **Verify Permissions**

   - Turn back Cloudfront
   - Access the CloudFront URL to ensure the website is working properly.

     ![Step 12](./images/3-cloudfront-static/12.step.png)

   - Check page load speed and ensure all files are being distributed through CloudFront

     ![Step 15](./images/3-cloudfront-static/15.step.png)
