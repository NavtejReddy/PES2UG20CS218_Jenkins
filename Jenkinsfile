 pipeline {
  agent any
  
  stages {
    stage('Build') {
      steps {
        sh 'g++ -o PES2UG20CS218 PES2UG20CS218.cpp'
        echo 'Build stage successful'
     
    stage('Test') {
      steps {
        sh './PES2UG20CS218'
        echo 'Test stage successful'
      }
    }
    stage('Deploy') {

        sh 'echo "Deploying..."'
        echo 'Deployment successful'
      }
    }
  }
  
  post {
    failure {
      echo 'pipeline failed'
    }
  }
}
