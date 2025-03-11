pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        build 'P'
        sh 'g++ hello.cpp -o output'
      }
    }
    stage('Test') {
      steps {
        sh './output'
      }
    }
    stage('Deploy') {
      steps {
        echo 'deploy'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline failed'
    }
  }
}
