**AWS Credentials Provider Chain**

    1) Command Line Options - --region, --output, --profile
    2) Environment Variables - AWS_ACCESS_KEY, AWS_SECRET_ACCESS_KEY, AWS_SESSION_TOKEN
    3) CLI Credentials file - aws configure ~/.aws/credentials
    4) CLI Config file - aws configure ~/.aws/config
    5) Container Credentials - for ECS tasks
    6) Instance Profile Credentials - For EC2 Instance profile