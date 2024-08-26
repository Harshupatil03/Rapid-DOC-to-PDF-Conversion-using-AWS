# Rapid DOC to PDF Conversion Project

## Overview
This project provides a solution for converting Microsoft Word documents (.docx) to PDF format using AWS services. The solution is designed to be scalable, efficient, and fully automated, leveraging Amazon S3, AWS Lambda, Amazon SQS, and IAM for secure access management.

## Features
- **Automated Conversion:** Automatically converts DOCX files uploaded to an S3 bucket into PDFs.
- **Scalable Architecture:** Uses AWS Lambda to handle the conversion process, ensuring scalability and efficiency.
- **Secure Processing:** Utilizes IAM roles and policies to manage secure access to AWS resources.
- **Queue Management:** Implements Amazon SQS to manage file conversion requests in a queue, ensuring reliable processing.

## AWS Services Used
- **Amazon S3:** For storing the input DOCX files and output PDF files.
- **AWS Lambda:** To execute the conversion process upon detecting new uploads.
- **Amazon SQS:** To queue the file conversion requests.
- **AWS IAM:** To manage permissions and access control for the AWS services used.

## Setup Instructions
1. **Create S3 Buckets:**
   - Set up two S3 buckets: one for DOCX file uploads and another for storing the converted PDF files.

2. **Set Up IAM Roles:**
   - Create IAM roles with permissions to access S3, SQS, and Lambda. Attach the necessary policies to these roles.

3. **Deploy Lambda Function:**
   - Write a Lambda function to handle the conversion process. Use Python or Node.js with a relevant library (e.g., `pypandoc` or `docxtopdf`).
   - Configure the Lambda function to trigger on new DOCX file uploads in the S3 bucket.

4. **Configure SQS Queue:**
   - Set up an SQS queue to handle conversion requests. Ensure the Lambda function processes messages from this queue.

5. **Test the Workflow:**
   - Upload a DOCX file to the designated S3 bucket and verify that it is automatically converted to PDF and saved in the output bucket.

## How It Works
1. A DOCX file is uploaded to the input S3 bucket.
2. The S3 event triggers the Lambda function, which retrieves the file and processes the conversion.
3. The converted PDF is stored in the output S3 bucket.
4. If SQS is used, the Lambda function reads the conversion request from the SQS queue and processes it.

## Prerequisites
- AWS Account with access to S3, Lambda, SQS, and IAM.
- Basic knowledge of AWS services and Python/Node.js for Lambda scripting.

## Contributing
Contributions to the project are welcome. Please fork the repository and submit a pull request with your changes.


## Document 
i have uploaded a word file in which all the steps are there for the configuration of the project.



