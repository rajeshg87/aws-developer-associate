**EBS Volume Type**

    1) GP2 (SSD) - General Purpose volume that balance Price and performance
        . Cheap
        . 3 IOPS / GiB, minimum 100 IOPS, burst to 3000 IOPS, max 16000 IOPS
    2) IOI (SSD) - Highest Performance voulme for mission critical low latency and highest through put
        . Expensive
        . More than 16,000 IOPS per volume
        . 4 GiB - 16 TiB
    3) ST1 (HDD) - Low cost HDD volume designed for frequenctly accessed, throughput instensive workloads
        . 500 GiB - 16 TiB
    4) SC1 (Cold HDD) - Lowest cost HDD volume designed for less frequently accessed workloads
        .  Cannot be Boot Volume
    
**COMMAND**

    ldblk - To list EC2 volume attached
    
**Instance Store**

    Pros
        * Better I/O performance
        * Good for Buffer / cache / temporary content
        * Data survives reboot
    Cons
        * On Stop or Termination data lost
        * Can't resize
        * Backups by user
       
**EFS - Elastic File System **

    * Managed NFS (Network File System) can be mounted on any EC2
    * EFS works with EC2 instances in multi-AZ
    * Highly available, Scalable, Expensive, Pay per use
    * Compatible with Linux not Windows