**CloudFront Origins**

    * S3 Bucket
        . For distributing files and chaching them at edge
        . Enhanced security with CloudFront Origin Access Identity (OAI)
        . CloudFront can be used as an ingress (to upload files to S3)

    * Custom Origin (Http)
        . Application Load Balancer
        . EC2 Instance
        . S3 Website 
        . Any Http Backend you want

**CloudFront vs S3 Cross Region Replication**

    * CloudFront - Great for static content that must be available everywhere
    * S3 CRR - Great for Dynamic Content that needs to be available at Low Latency in few region

**CloudFront Geo Restriction**

    * Whitelist
    * Blacklist

**CloudFront and Https**

    *Viewer Protocol Policy
        . Redirect Http to Https
        . Or Use Https Only
    
    * Origin Protocol Policy(Http or S3)
        . Https Only
        . Match Viewer (http => http, https=>https)

**S3 Bucket Website don't support HTTPS**