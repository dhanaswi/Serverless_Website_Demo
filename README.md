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
<br>
<p align="center">
<img src="images/1.png" width="500">
</p>
</br>

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
2. Remove the default sample code
3. Paste the Python code which is in **hellocloudgurus.py** 
4. Click **Deploy** to save changes
<br>
<p align="center">
<img src="images/4.png" width="500">
<img src="images/5.png" width="500">
</p>
<br>

## Step 3: Add API Gateway as a Trigger

1. In the Lambda function page, click **Add trigger**
2. Select **API Gateway**
<br>
<p align="center">
<img src="images/6.png" width="500">
<img src="images/7.png" width="500">
</p>
<br>  

3. Choose **Create a new API**
4. API type: **HTTP API**
5. Security: **Open**
6. API Name: **Use the default name provided by API Gateway** 
7. Enable **Cross-origin resource sharing(CORS)**
8. Click **Add**
<br>
<p align="center">
<img src="images/8.png" width="500">
<img src="images/9.png" width="500">
</p>
<br>

## Step 4: Test the API Gateway Endpoint

1. Copy the **API endpoint URL**
2. Open it in a new tab
3. Verify that the Lambda response is displayed
<br>
<p align="center">
<img src="images/10.png" width="500">
<img src="images/11.png" width="500">
</p>
<br>

## Step 5: Create an Amazon S3 Bucket

1. Navigate to **Amazon S3**
2. Click **Create bucket**
3. Select bucket type as **General purpose**
4. Enter a **globally unique bucket name**
5. In Object Ownership we need to **enable ACLs**
<p align="center">
<img src="images/12.png" width="500">
<img src="images/13.png" width="500">
</p>
<br>

6. Uncheck **Block all public access**
7. Acknowledge the warning
8. In Default Encryption select encryption types as **Server-side encryption with Amazon S3 managed keys(SSE-S3)** 
9. Click **Create bucket**
<br>
<p align="center">
<img src="images/14.png" width="500">
<img src="images/15.png" width="500">
</p>
<br>

## Step 6: Upload Website Files to S3

1. Open the created bucket
2. Click **Upload**
3. Upload:
   - index.html
   - error.html
4. Click **Upload**
<br>
<p align="center">
<img src="images/16.png" width="500">
<img src="images/17.png" width="500">
<img src="images/18.png" width="500">
</p>
<br>
