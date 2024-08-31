+++
title = "Set Up Permissions"
date = 2024-05-14T00:38:32+07:00
weight = 2
chapter = false
pre = "<b>2. </b>"
+++

**Content:**

## Step 2: Set Up Permissions

1. **Configure the Bucket Policy to Allow Public Access**

   - Go to the “Permissions” tab > “Bucket Policy” and add the following policy to allow public access:

     ```json
     {
       "Version": "2012-10-17",
       "Statement": [
         {
           "Sid": "PublicReadGetObject",
           "Effect": "Allow",
           "Principal": "*",
           "Action": "s3:GetObject",
           "Resource": "arn:aws:s3:::your-bucket-name/*"
         }
       ]
     }
     ```

2. **Verify Permissions**
   - Ensure the files in the bucket can be accessed publicly via direct URLs.
