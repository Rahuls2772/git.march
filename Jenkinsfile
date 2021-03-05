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
stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
                    steps {
                        sh './jenkins/scripts/test.sh'
                    }
                }
                stage('Deliver') {
                            steps {
                                sh './jenkins/scripts/deliver.sh'
                                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                                sh './jenkins/scripts/kill.sh'
                            }
                        }

    }
}
