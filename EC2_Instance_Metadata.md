**AWS EC2 Instance Metadata**

    URL : http://169.254.169.254/latest/meta-data

    * Can retrieve the IAM Role name from metadata, but you cannot retrieve IAM policy
    * Metadata -> Info about the EC2 Instance
    * Userdata -> Launch Script of the EC2 Instance

**MFA with CLI**

    * To use MFA with CLI, you must create a temporary session.
    * STS GetSessionToken API call

**Exponential Backoff**

    * If you get ThrottlingException intermittenly, use Exponential Backoff
    * Retry mechanism already included in AWS SDK API calls
    * Must implement ourself if using AWS API 
        . Implement of server error 5xx, not on client error 4xx