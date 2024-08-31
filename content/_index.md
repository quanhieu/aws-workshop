+++
title = "Host Static Website on S3 and CloudFront"
date = 2024
weight = 1
chapter = false
+++

# Host Static Website on S3 and CloudFront

## Why Deploy a Static Website Using Amazon S3 and CloudFront?

### High Performance and Page Load Speed:

- **S3** stores static files (HTML, CSS, JS) on the cloud platform with automatic scaling and quick access.
- **CloudFront** is a Content Delivery Network (CDN) that helps distribute content to users from the nearest servers, reducing latency and increasing page load speed.

### Cost Savings:

- Deploying a static website on **S3** is cost-effective, charging only based on storage and bandwidth usage, with no complex server management required.
- **CloudFront** optimizes bandwidth by caching content close to users, reducing direct access to S3 and thereby cutting costs.

### Superior Scalability:

- **S3** and **CloudFront** automatically handle high traffic without complex configurations, suitable for websites with rapid growth needs.
- No worries about server overload when many users access the site simultaneously.

### Enhanced Security:

- **CloudFront** allows HTTPS setup, protecting data during transmission.
- Use **Origin Access Control (OAC)** to ensure only CloudFront has access to S3, protecting data from unauthorized access.
- AWS provides advanced security options like **AWS WAF (Web Application Firewall)** and **Shield** to protect websites from DDoS attacks.

### Easy Management and Automation:

- Configuring, deploying, and managing a static website is straightforward via AWS Console or by using **Infrastructure as Code** with AWS CloudFormation or Terraform.
- AWS offers automatic backup and recovery features, ensuring service continuity.

### Integration with Other AWS Services:

- Easily integrate with **AWS Lambda**, **API Gateway**, or **AWS Amplify** to create more complex web applications from a static base.
- **AWS IAM** can be used to manage access permissions, providing additional security control.

## Benefits of Using S3 and CloudFront:

- **Faster Response Time**: Content is distributed from the nearest edge locations to users through CloudFront, reducing page load time.
- **Data Security and Access Control**: Security settings help better control who can access your content.
- **High Reliability**: AWS services have a high SLA, ensuring website availability.
- **SEO Optimization and User Experience**: Fast page load speeds improve SEO rankings and overall user experience.
- **No Complex Maintenance Required**: No worries about server maintenance or regular software updates, reducing workload for the development team.

Deploying a static website using S3 and CloudFront is simple, cost-effective, and provides a fast, secure, and stable web experience for users!

#### Main Content

1. [Create and Configure the S3 Bucket](1-Create-s3-bucket-upload-file/)
2. [Config permission S3 bucket](2-Config-permission-s3-bucket/)
3. [Create CloudFront Distribution](3-Create-cloudFront-distribution/)

<!-- need to remove parenthesis for path in Hugo 0.88.1 for Windows-->
