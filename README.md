# aws_sqs_feedback_system_project
Automated feedback collection and processing system built using Amazon SQS and AWS Lambda.

# What this project does
Collects user feedback and processes it 
automatically using AWS SQS and Lambda
and store it into AWS DYNAMO DB.

# AWS Services Used
- Amazon SQS
- AWS Lambda
- AWS DYNAMO DB
- AWS CLOUDWATCH
- AWS IAM ROLE
- AWS API GATEWAY
- AWS SNS

# Steps I followed
- Created an IAM Role with required permissions for Lambda to access SQS, DynamoDB and SNS
- Set up an SQS Queue to act as the message buffer between producer and consumer
- Built a Producer Lambda function to receive feedback from API Gateway and push it to SQS
- Created a REST API using API Gateway and linked it to the Producer Lambda
- Built a Consumer Lambda function triggered automatically by SQS to process incoming messages
- Configured DynamoDB table to store the feedback data received from Consumer Lambda
- Set up an SNS Topic to send notification once feedback is successfully stored
- Enabled CloudWatch logging on both Lambda functions to monitor execution and debug errors- 
- Tested the complete flow end-to-end using Postman by sending POST requests with feedback data





