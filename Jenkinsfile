pipeline {
  agent any
  stages {
    stage('Stage 1: Integrate Web and DB') {
      steps {
        echo '1.1 Getting application web files'
        echo '1.2 Getting database files'
        echo '1.3 Combining web and db files'
      }
    }
  }
}
pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000'
        }
    }
     
        
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
    }
}
