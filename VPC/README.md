**VPC & Subnets Primer**

    * To define access to the internet and between subnets 
      we use route tables.
    
**Internet Gateway & NAt Gateway**

    Internet Gateway
        * Helps our VPC instances connect with the internet
        * Public subnets have a route to the internet gateway
    
    NAT Gateway
        * AWS Managed and NAT Instances (Self Managed) allows 
          your instances in Private Subnets to access the internet
          while remaining private.

**Network ACL & Security Groups**
    
    NACL
        * Firewall which controls traffic from and to subnet
        * Can hava ALLOW & DENY rules
        * Are attached at Subnet level
        * Rules only include IP Address

    Security Groups
        * Firewall that controls traffic to and from an ENI / EC2 Instance
        * Can have only ALLOW rules
        * Rules include IP address and other security group

**VPC Flow Logs**
    
    * Capture information about IP Traffic goiing into interfaces
        1) VPC Flow Logs
        2) Subnet Flow Logs
        3) Elastic Network Interface logs

    * Helps to monitor and troubleshoot connectivity issue
        1) Subnets to internet
        2) Subnets to subnets
        3) Internet to Subnets
    
    * VPC data logs can goto S3/Cloud Watch logs

**VPC Peering**
    
    * Connect two VPC, privately using AWS network
    * Must not have overlapping CIDR address range
    * VPC peering connection is not transitive.

**VPC Endpoints**
    
    * Endpoints allows to connect to AWS services using private network
      instead of the public www network
    
    VPC Endpoint Gateway - S3 & Dynamo DB
    VPC Endpoint Interface -  the rest

**Site to Site VPn & Diect Connect(DX)
    
    Site to Site VPN - Connect on-permise VPN to AWS over the public network
    Direct COnnect (DX) - Physical connection between on-permise and AWS over a private network