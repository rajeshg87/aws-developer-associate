**AWS CICD**

    * Code Commit
        . Version Control
        . Interaction done using GIT
        . Authentication - SSH Keys, HTTPS using CLI Authentication Helper or Generating HTTPS crdentials
        . Authorization - IAM Policies 
        . Encryption - KMS / Encrypted in Transit
        . Notification - SNS, AWS Lambda or AWS Cloudwtach Event Rules

    * Code Build
        . Leverage Docker for reproducible build
        . buildspec.yml
        . Output logs to AWS S3 and Cloud Watch logs
        . Use Cloudwatch alarms to detect failed builds

    * Code Pipeline
        . Visual Workflow
        . Made of Stages -  Each stage cretae Artifacts
        . Pipeline state changes happen in CloudWatch Events, create SNS notifications
        . AWS CloudTrail can be used to audit AWS API calls
        . If Pipeline can't perform action check IAM roles and permission

    * Code Deploy
        . Each EC2 instance must be running the CodeDeploy agent
        . CodeDeploy sends appspec.yml
        . Components
            1) Application
            2) Compute Platform
            3) Deployment Configuration
            4) Deployment Group
            5) Deployment Type
            6) IAM Instance Profile
            7) Application Revision
            8) Service Role
            9) Target Revision
        . AppSpec
            * Hooks - Set of instructions to deploythe new version.
            * Order
                1) ApplicationStop
                2) Download Bundle
                3) BeforeInstall
                4) AfterInstall
                5) ApplicationStart
                6) ValidateService

**Code Star**

    * Codestar is Integrated solution that regroups GitHub, Code Commit, CodeBuild, 
      CodeDeploy, CloudFormation, CodePipeline, CloudWatch
    * Issue tracking integration with JIRA / Github Issues
