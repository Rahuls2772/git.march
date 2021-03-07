pipeline {
  agent any
    
  tools {nodejs "node"}
    
  stages {
        
    stage('Git') {
      steps {
        git 'https://github.com/Rahuls2772/git.march.git'
      }
    }
     
    stage('Build') {
      steps {
        sh 'npm install'
       }
    }  
    
            
    stage('Test') {
      steps {
        sh 'node test'
      }
    }
  }
    }
    stage('Deliver') {
            steps {
                sh './jenkins/scripts/deliver.sh'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                sh './jenkins/scripts/kill.sh'
            }
    }
