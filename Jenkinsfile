pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat(script: 'gradle clean build', returnStatus: true)
      }
    }
    stage('msg') {
      steps {
        catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE') {
          sh 'exit 0'
        }

      }
    }
    stage('test') {
      steps {
        bat(script: 'gradle test', returnStatus: true)
      }
    }
  }
}