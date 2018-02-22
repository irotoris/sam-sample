# sam-sample
## Overview
Sample serverless application by AWS Lambda, DynamoDB, API Gateway, and deploy with AWS SAM.  

API Gateway --> AWS Lambda --> DynamoDB  

## Requirements
* awscli config
* aws-sam-local

##  Build and Deployment
### Packaging
```
sam package \
    --template-file template.yaml \
    --s3-bucket <your S3 bucket name for AWS SAM> \
    --output-template-file packaged-template.yaml
```

### Deployment
```
sam deploy \
    --template-file packaged-template.yaml \
    --capabilities CAPABILITY_IAM \
    --stack-name <YOUR_STACK_NAME>
```
