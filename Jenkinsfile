pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'make'
        echo 'Build Successful'
      }
    }
    stage('Test') {
      steps {
        sh '/var/jenkins_home/workspace/PES2UG20CS068-1/main/hello_exec'
      }
    }
    stage('Deploy') {
      steps {
        sh 'make deploy'
        echo 'Deployed Successfully!'
      }
    }
  }
  post {
    failure {
      echo 'Task Failed'
    }
  }
}
