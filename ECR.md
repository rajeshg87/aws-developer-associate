**ECR**

    * ECR is Private Docker Image Repository

    * AWS CLI v1 login cmd
        $(aws ecr get-login --no-include-email --region eu-west-1)

    * AWS CLI v2 login cmd
        aws ecr get-login-password --region eu-west-1 
        | docker login --username AWS --password-stdin
        | 1234567890.dkr.ecr.eu-west-1.amazonaws.com
