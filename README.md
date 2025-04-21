# fileprocessing-lambda

An event-driven image processing pipeline using AWS Lambda and S3. This project automatically processes images (e.g., pixelation) and stores them in a destination S3 bucket.

## Features

- Triggered by S3 events
- Processes images with Python and PIL
- Stores results in an S3 destination bucket

## AWS Services

- Amazon S3
- AWS Lambda
- IAM Roles & Policies
- CloudWatch Logs

## Setup Instructions

1. **Create S3 Buckets**: One for input and one for processed output.
2. **Lambda Execution Role**: Create a role with permissions for S3 and CloudWatch.
3. **Lambda Deployment**: Upload the Lambda function and set the environment variable for the processed bucket.
4. **S3 Trigger**: Configure the Lambda function to trigger on new object creation in the source bucket.

## Architecture

<img src="pixelator-aws-s3-lambda-events-main\maxresdefault.jpg" alt="architecture" width="500" />


## Cleanup

After testing, delete the Lambda function, IAM role, and both S3 buckets to avoid unnecessary charges.

---
This project is suitable for educational/demo purposes and uses AWS Free Tier.
