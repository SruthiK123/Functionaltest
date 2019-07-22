pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat(script: 'gradle clean build', returnStatus: true)
      }
    }
    stage('Testing') {
      steps {
        bat(script: 'gradle test', returnStatus: true)
      }
    }
  }
}