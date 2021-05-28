**NO SQL**

    * Don't support JOIN
    * Scales Horizontally
    * Don't perform aggredation operation

**Write Capacity Units (WCU)**

    10 Objects Per Sec of 2 KB  -> 10*2 = 20 WCU
    6 Objects Per Sec 0f 4.5 KB -> 6*5 = 30 WCU
    120 Objects Per Minute 0f 2  KB -> (120/60)*2 = 4 WCU

**Read Capacity Units (RCU)**

    10 Strongly Consistent read per sec of 4 KB -> 10 * 4/4 = 10 RCU
    16 eventually consistent read per sec 0f 12 KB -> (16/2) * (12/4) = 24 RCU
    10 Strongly Consistent read per sec of 6 KB -> 10 * (8/4) = 20 RCU

**DynamoDB - DAX**

    * DAX - DynamoDB Accelator
    * Seamless Cache for DB 

**Transaction Capacity Computations**
    
    5KB Item Size

    Transaction Item Writes Per Sec : 3
        = [5 KB / 1 KB per WCU] * 2(cost of transaction) * 3 (# per sec)
        = 30 WCU

    Transaction Item Reads Per Sec : 5
        = [5 KB / 4 KB per RCU] * 2(cost of transaction) * 5 (# per sec)
        = 2 (high ceiling) * 2 * 5
        = 20 RCU

**DynamoDB Session State Cache**
    
    Elastic Cache is in-memory but DynamoDB is serverless

**DynamoDB Operation**

    Copying DynamoDB Table
        1) Use AWS DataPipeline (uses EMR)
        
**Security**

    * VPC Endpoints available to access DynamoDB without internet
    * Amazon DMS can be used to migrate to DynamoDB

    