**SQS**

    * Default retention of messages 4 days, max of 14 days
    * 256 KB per message
    * Low Latency < 10ms
    * ChangeMessageVisibility to avoid read Queue message twice
    * Long Polling decrease the number of API calls made to SQS
      while increasing the efficiency and latency of application
    * Deduplication methods
        1) Content Based - SHA-256 
        2) Explicitly provide a Message Deduplication Id