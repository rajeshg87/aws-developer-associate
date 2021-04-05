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
