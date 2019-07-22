pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            bat(script: 'gradle clean build', returnStatus: true)
          }
        }
        stage('Message1') {
          steps {
            catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE') {
              sh 'exit 0'
            }

          }
        }
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