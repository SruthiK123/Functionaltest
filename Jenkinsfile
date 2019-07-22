pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'exit 1'
      }
    }
    stage('Testing') {
      steps {
        bat(script: 'gradle test', returnStatus: true)
      }
    }
  }
}