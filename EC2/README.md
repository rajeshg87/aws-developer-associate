**COMMAND**

ssh -i xxx.pem ec2-user@13.234.240.10

chmod 0400

**Apache Installation Steps**

"#!/bin/bash"

yum update -y

yum install -y https.x86_64

systemctl start httpd.service

systemctl enable httpd.service

echo "Hello World from $(hostname -f)" > /var/www/html/index.html

**EC2 Launch Types**

1) On Demand - Short Workload
2) Reserved - Minimum 1 Year (DB)
    1) Reserved
    2) Convertible 
    3) Scheduled
3) Dedicated  Instance: No Customers will share Hardware
4) Dedicated Host: Book an entire Physical server, control instance placement

**ENI - Elastic Network Interface**

1) Logical component in a VPC that represents Virtual Network Card
2) ENI Attributes
    1) Primary Private IPv4, One or More secondary IPv4
    2) One Elastic IP (IPv4) per private IPv4
    3) One Public IPv4
    4) One or More security groups
    5) MAC Address
3) Bound to specific AZ