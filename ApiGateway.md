**API Gateway - EndPoints**

    1) Edge Optimized
        * Route through the CloudFront Edge location
        * API Gateway still lives in one region

    2) Regional
        * Could manually combine with CloudFront (more control over caching)

    3) Private
        * Can only accessed by VPC using an interface VPC Endpoint (ENI)

**Canary Deployment**

    Choose the % of traffic the canary channel service

**Error Code**

    429 - Too many requests
    403 - Access Denied
    400 - Bad Request

    502 - Bad Gateway
    503 - Service Unavailable
    504 - Integration Failure

**CORS**

    OPTIONS pre-flight request must contain below headers
        * Access-Control-Allow-Methods
        * Access-Control-Allow-Headers
        * Access-Control-Allow-Origin
