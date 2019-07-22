pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'exit 1'
        bat(script: 'gradle build', returnStatus: true)
      }
    }
    stage('Testing') {
      steps {
        bat(script: 'gradle test', returnStatus: true)
      }
    }
  }
}