**Elastic Beanstalk**

    * PAAS Developer centric view od deploying an application on AWS
    * Beanstalk ios Free, pay only for underlying Instance
    * Beanstalk Components
        1) Application
        2) Application Version
        3) Environment Name

**Deployment Modes**

    1) Single Instance
    2) High Availability with Load Balancer

**Deployment Options for Updates**

    1) All at Once (deploy all in one go)
    2) Rolling
    3) Rolling with Additional Batches
    4) Immutable (Using Temporary ASG ) Canary Testing

**Beanstalk Lifecycle Policy**

    Can store upto 1000 application versions

**Beanstalk Extensions**

    * In .ebextensions/ directory
    * YAML / JSON Format
    * Resource created by extensions will be deleted if env goes away

**Beanstalk Docker**

    * Dockerrun.aws.json is used to generate the ECS task definition
    * Dockerrun.aws.json needs to be in root of Source Code