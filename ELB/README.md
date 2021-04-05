**ELB Types**

    1) Classic Load Balancer
        1) Supports TCP(Layer 4), Http & Https (Layer 7)
        2) Health checks are TCP or Http based
        3) Fixed Hostname
    2) Application Load Balancer
        1) Load Balancing to multiple HTTP applications across machines (target groups)
        2) Load Balancing to multiple application on the same machine (ex Containers)
        3) Suppoprt for HTTP and Socket
        4) Support redirect from Http to Https
        5) Routing tables based on different categories
            1) Path (example.com/product & example.com/user
            2) URL (first.com & second.com)
            3) Query Parameter (example.com/product?id=1)
        6) True IP of the client inserted in the Header X-Forwarded-For
        6) Port (X-Forwarded-Port) and Proto (X-Forwarded-Proto)
   
    3) Network Load Balancer
        1) Forward TCP & UDP traffic to your instances
        2) Handle millions of requests per seconds
        3) Less Latency ~ 100ms (vs 400ms for ALB)
        4) Has one static IP per AZ, supports assigning Elastic IP (Helpful for whitelisting specific IP)
        5) Extreme Performance 
        
**Server Name Indication (SNI)**   
     
    1) Supports multiple listeners with multiple SSL
    2) ALB & NLP Supports SNI