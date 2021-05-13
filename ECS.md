**ECS TAsk Definition**

    * Task definition are metadata in JSON form to tell ECS how to run container
    * Information in Task Definition
        . Image Name
        . Port Binding for Container Host
        . Memory and CPU required
        . Environment Variables
        . Networking Information

**Dynamic Port Forwarding**

    * Using Dynamic Port Forwarding we can deploy multiple conatiner in same instance

**ECS IAM Roles**

    * EC2 Instance Profile
        . Used by ECS Agent
        . Make API calls to ECS Service
        . Send container logs to CloudWatch Logs
        . Pull Docker Image from ECR

    * ECS Task Role
        . Allow each task to have specific role

**ECS Task Placement**

    * Task Placement Strategy & Task Placement Constrints
    * Only for ECS not for Fargate

**ECS Task Placement Strategy**

    Binpack
        * Place tasks based on least available amount of CPU or memory
        * Minimize the number of instances in use

    Random
        * Place task randomly

    Spread
        * Place task evenly based on specified value

**ECS Task Placement Constraints**

    * distinctInstance : Place each task on different container istance
    * memberOf : place task on instance that statisfy expression
                 Cluster Query Language

**ECS Auto Scaling**

    * Target Tracking : CloudWatch metric
    * Step Scaling : CloudWatch Alarms
    * Scheduled Scaling : Predictable Changes