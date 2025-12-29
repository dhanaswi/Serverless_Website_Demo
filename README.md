# Serverless Website Using AWS Lambda and API Gateway

This project demonstrates how to build and deploy a serverless website using AWS Lambda, API Gateway, and Amazon S3.
It shows how backend logic can be executed without managing servers while S3 hosts the static frontend efficiently.


## Prerequisites

- An AWS account
- Basic knowledge of AWS Console
- Static website files (index.html, error.html, Lambda Python code)
- Internet access


## Step 1: Create an AWS Lambda Function

1. Sign in to the **AWS Management Console**
2. Search for **Lambda** and open the service
<p align="center">
<img src="images/1.png" width="500">
</p>
<br>

3. Click **Create function**
4. Select **Author from scratch**
5. Enter a function name (example: Serverless-function)
6. Choose **Python** (latest version) as runtime
7. Select **x86_64** architecture
<br>
<p align="center">
<img src="images/2.png" width="500">
</p>
<br>

8. Select **Create a new role with basic Lambda permissions** in Execution role
9. Click **Create function**
<br>
<p align="center">
<img src="images/3.png" width="500">
</p>
<br>

## Step 2: Add Code to the Lambda Function

1. Scroll to the **Code source** section
<br>
<p align="center">
<img src="images/4.png" width="500">
</p>
<br>

2. Remove the default sample code
3. Paste the provided Python code
4. Click **Deploy** to save changes
<br>
<p align="center">
<img src="images/5.png" width="500">
</p>
<br>

## Step 3: Add API Gateway as a Trigger

1. In the Lambda function page, click Add trigger
2. Select **API Gateway**
3. Choose **Create a new API**
4. API type: **HTTP API**
5. Security: **Open**
6. Enable **CORS**
7. Click **Add**
