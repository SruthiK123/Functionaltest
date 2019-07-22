pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat(script: 'gradle build', returnStatus: true)
      }
    }
    stage('test') {
      steps {
        catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE') {
          bat(script: 'gradle test', returnStatus: true)
        }

      }
    }
    stage('message') {
      steps {
        sh 'exit 0'
      }
    }
  }
}