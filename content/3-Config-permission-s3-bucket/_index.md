+++
title = "Set Up Permissions"
date = 2024-05-14T00:38:32+07:00
weight = 3
chapter = false
pre = "<b>3. </b>"
+++

<!-- **Content:** -->

### Step 3: Set Up Permissions

1. **Configure the Bucket Policy to Allow Public Access**

   - Go to the “Permissions” tab > “Bucket Policy” and add the following policy to allow public access:

     ```json
     {
       "Version": "2012-10-17",
       "Statement": [
         {
           "Sid": "AddPerm",
           "Effect": "Allow",
           "Principal": "*",
           "Action": "s3:GetObject",
           "Resource": "arn:aws:s3:::YOUR_BUCKET_NAME/*"
         }
       ]
     }
     ```

     ![Step 7](../images/2-s3-static/7.step.png)

2. **Verify Permissions**

   - Ensure the files in the bucket can be accessed publicly via direct URLs.

     ![Step 8](../images/2-s3-static/8.step.png)

   - Verify Url
     ![Step 9](../images/2-s3-static/9.step.png)
