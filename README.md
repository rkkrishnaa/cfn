# cfn
This repo contains cloudformation template to deploy a single node or multinode openstack(ocata release) setup on AWS infrastructure.


I haved added some templates to automate cloudformation and terraform deployments using  AWS CI/CD pipeline tools such as code commit, code build, code deploy and code pipeline.


Apart from that, You can find a nested template to deploy a three tier web application using RDS as a data tier, ec2 instances managed by elastic beanstack as app tier and s3 bucket for storing the build artifacts, we can reuse the above CI/CD template for setting a CI/CD pipe line for managing your project builds.This template follows the standard approach for deploying an application on AWS infrastructure. You should execute the template in order. Orelse you can create one more stack which wraps all the nested stacks in a single template which creates an infrastructure. This template is intended for testing the stack components individually, So that I have not included a dedicated parent template to invoke the other nested templates in a specific order.
