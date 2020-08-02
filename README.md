# terraform_lambda_api_app

Deploying a Serverless application on AWS using Terraform and Jenkins and exposing via API gateway endpoint.
============================================================================================================

Prerequisites:
=============


1.  Steps to install AWS Client on linux

      1. curl "https://s3.amazonaws.com/aws-cli/awscli-bundle.zip" -o "awscli-bundle.zip"

      2. unzip awscli-bundle.zip

      3. sudo ./awscli-bundle/install -i /usr/local/aws -b /usr/local/bin/aws


2.  Install terrform on linux

      1. Downloand and move the terraform binary to /usr/local/bin.

      2. Verify terraform by  "terraform --help" on commandline to confirm terraform is available.


3.  Install Plugins in Jenkins

      1. CloudBees AWS Credentials Plugin
      2. Pipeline
      3. Terraform Plugin
      4. AnsiColor
      
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

This application execution is build on jenkins pipeline and executes two stages.
 Stage 1 : 
        
