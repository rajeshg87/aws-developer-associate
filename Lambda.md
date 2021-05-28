**Lambda**

    * Lambda S3 notification needs Bucket Versioning
    * Resource Based Policy helps other resource to invoke Lambda Function
    * AWS Lambda Aliases cannot refer another Alias
    * SNS does not require Event Source Mapping

**Environment Variable**

    Environment variables to communicate with X-Ray
        1) _X_AMZN_TRACE_ID : Contains the tracing header
        2) AWS_XRAY_CONTEXT_MISSING: by Default, LOG_ERROR
        3) AWS_XRAY_DAEMON_ADDRESS: X-Ray Deamon IP_ADDRESS:PORT

**Performance**

    * The more RAM you add, the more vCPU credits we get
    * Lambda good for 3 secs to 900 secs (15 mins)