Architecture Diagram for deploying elasticbeanstack application
---------------
![cfn_aws_arch.png](elasticbeanstack-app/cfn_aws_arch.png?raw=true)

The above architecture diagram implements a simple three tier webapplication using elasticbeanstack for deploying application. It uses NAT Gateway for VMs hosted in the private network to access internet. Bastion host is for accessing the private servers through SSH. Multi AZ deployment in RDS improves the availability of the database server. Certificate Manager creates a SSL certificate for an application load balancer endpoints. Build artifacts are stored in S3 for deployment purposes. 

Architecture Diagram for building CI/CD pipeline to automate infrastruture provisioning and management by cloudformation
---------------
![](codepipeline-cicd/11_ci_cd_using_hashicorp_terraform_and_aws_code_pipeline.png?raw=true)

We can substitute CloudFormation/Terrform as an orchestrator in the above architecture diagram

Architecture Diagram for building CI/CD pipeline to automate infrastruture provisioning and management by terraform
---------------
![](codepipeline-cicd/8_ci_cd_using_hashicorp_terraform_and_jenkins.png?raw=true)

Replace Jenkins and its pipeline plugin with AWS CodePipeline and AWS Code Build. You can add a manual approval stage in a pipeline using SNS or lambda trigger with slack integration.
