# terraform_lambda_api_app

Deploying a Serverless application on AWS using Terraform and Jenkins and exposing via API gateway endpoint.
                               

Prerequisites:
=============


1.  Steps to install AWS Client on linux

      1. curl "https://s3.amazonaws.com/aws-cli/awscli-bundle.zip" -o "awscli-bundle.zip"

      2. unzip awscli-bundle.zip

      3. sudo ./awscli-bundle/install -i /usr/local/aws -b /usr/local/bin/aws..


2.  Install terrform on linux

      1. Downloand and move the terraform binary to /usr/local/bin.

      2. Verify terraform by  "terraform --help" on commandline to confirm terraform is available.


3.  Install Plugins in Jenkins

      1. CloudBees AWS Credentials Plugin
      2. Pipeline
      3. Terraform Plugin
      4. AnsiColor
      
 4. AWS account.
 
 5. S3 bucket with name - gar-hw-aws2 
      
 Resources used:
 =============
 
        1. Node Js Application.
        2. AWS Lambda.
        3. API Gateway.
        4. IAM
        5. Terraform
        6. Jenkins - pipeline.
        
    
Application:
===========
 This application contains below :

      1. index.js is the sample helloworld program.
      2. compression.sh is the script to zip the file.
      3. Jenkinsfile contains two stages
            1. Stage push_to_S3:
                  1. In this stage index.js script is bundled using compression.sh and zip file is created and pushed to s3 bucket.

            2. Stage invoke_terraform_pipeline:
                  1. In this stage terraform pipeline is triggered.
                 ( https://github.com/giriadini/terraform-jenkins-pipeline/find/master )
        
