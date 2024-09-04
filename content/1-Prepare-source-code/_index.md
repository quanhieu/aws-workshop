+++
title = "Prepare source code"
date = 2024-08-14T00:38:32+07:00
weight = 1
chapter = false
pre = "<b>1. </b>"
+++

## Deploying a Static Website Using Amazon S3 and CloudFront

Deploying a static website using Amazon S3 and CloudFront is a popular, quick, and cost-effective solution. Follow the steps below to get started:

### Step 1: Prepare source code

1.  **Init source code**

    ```

    npx create-next-app

    ```

    ![Step 1](./images/1-prepare-nextjs/1.step.png)

2.  **Test source**

    ```
     pnpm dev
     or
     yarn dev
    ```

    ![Step 2](./images/1-prepare-nextjs/2.step.png)

- Check `https://localhost:3000`

  ![Step 3](./images/1-prepare-nextjs/3.step.png)

3. **Build source**

   ```
    pnpm build
    or
    yarn build
   ```

   ![Step 4](./images/1-prepare-nextjs/4.step.png)
