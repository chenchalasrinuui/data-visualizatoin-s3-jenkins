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
  }
}