pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'gradle clean build'
      }
    }
    stage('Testing') {
      steps {
        bat(script: 'gradle test', returnStatus: true)
      }
    }
  }
}
