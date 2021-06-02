**AWS Directory Services**

    AWS Managed Microsoft AD
        * Create own AD in AWS, manage users locally, Supports MFA
        * Establish 'trust' connection to on-premise AD
    
    AD Connector
        * Directory Gateway (proxy) to redirect to on-permise AD
        * Users are managed on the on-permise AD

    Simple AD
        * AD-Compatability managed directory on AWS
        * Cannot be joined with 0n-permise AD