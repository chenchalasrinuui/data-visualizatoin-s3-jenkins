pipeline {
  agent any

  stages {
    stage('Install Dependencies') {
      steps {
        script {
          bat 'npm install'
        }
      }
    }

    stage('Build') {
      steps {
        script {
          bat 'npm run build'
        }
      }
    }
    stage('deploy') {
            steps {
              bat "aws configure set aws_access_key_id $AWS_ACCESS_KEY_ID"  
              bat "aws configure set aws_secret_access_key $AWS_SECRET_ACCESS_KEY"
              bat 'aws s3 sync dist/ s3://my-react-bucket-2 --region us-east-1'
            }
        }
  }
}
