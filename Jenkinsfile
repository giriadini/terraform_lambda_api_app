pipeline {
    agent any
    stages {
        stage ('Push_to_S3') {
            steps {
                withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: 'awsCredentials', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']]) {
                sh '''
                         sh ./compression.sh 
                         aws s3 cp ./lambda_function.zip s3://gar-hw-aws2/v1.0.0/lambda_function.zip
                 '''
                }
            }
        }
        stage ('Invoke_terraform_pipeline') {
            steps {
                    build job: 'terraform-pipeline'
                 }
        }    
        
    }

}