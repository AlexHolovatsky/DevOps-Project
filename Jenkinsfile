pipeline {
    agent any
    
    environment {
        AWS_ACCESS_KEY_ID     = credentials('AWS_ACCESS_KEY_ID1')
        AWS_SECRET_ACCESS_KEY = credentials('AWS_SECRET_ACCESS_KEY1')
        AWS_REGION = 'eu-west-2'
        AWS_DEFAULT_REGION = 'eu-west-2'
    }
    
    stages {
         stage('Checkout') {
            steps {
            echo 'test'        

          }
        }
        
        
        stage('Init') {
            steps {
                sh 'terraform init'
            }
        }
        
        stage('Plan') {
            steps {
                sh 'terraform plan'
            }
        }

        
        stage ("Deploy") {
            steps {
                sh 'terraform apply --auto-approve'
        }
    }
    }
   
}
