**RDS**

        Database Managed by AWS
            1) Postgres
            2) MySQL
            3) MariaDB
            4) Oracle
            5) Microsoft SQL Server
            6) Aurora (AWS Proprietary Database)

        Advantages
            1) Automated Provisioning, OS Patching
            2) Continous Backups & Point in Time Restore
            3) Monitoring Dashboards
            4) Read Replicas for imporved read performance
            5) Multi AZ setup for DR
            6) Maintance windows for upgrades
            7) Scaling Capabilities (Horizontal & Vertical)
            8) Storage backed by EBS (gp2 & iol)
        Can't SSH into Instance
        RDS Storage Autoscaling
            1) Free storage is less than 10% of allocated storage
            2) Low storage lasts atleast 5 mins
            3) 6 hours have passed since last modification

**RDS Security & Access Management**
        
    Security
        1) RDS usually deployed with in Private subnet
        2) RDS Security works by leveraging security groups

    Access Management
        1) IAM Policies 
        2) Traditional Username & Password
        3) IAM Based Authentication (Only for MySQL & Postgres)

**Aurora**

    * Performance 5x -> MySQL & 3x -> Postgres
    * Storage increments of 10GB, upto 64TB
    * Can have 15 replicas while MySQL has 5
    * COsts 20% more

    * 6 Copies of data across 3 AZs
        . 4 Copies for writes
        . 3 Copies for reads

    * Writer Endpoint (master) 
    * Reader Endpoint (replicas)

**Elastic Cache**

    REDIS
        1) Multi AZ with Auto Failover
        2) Read Replicas to scale reads
        3) Backup & Restore features

    MEMCACHED
        1) Multi Node for Partitioning of data (sharding)
        2) No High Availability
        3) Non Persistent
        4) No Backup and restore
        5) Multi Threaded architecture