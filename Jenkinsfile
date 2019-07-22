pipeline {
  agent any
  node{
  def build_ok = true
  stages {
  try{
    stage('Build') {
      steps {
        sh 'gradle clean build'
		sh 'exit 1'
      }
    }
	}
	catch(e){
	build_ok = false
    echo e.toString()
	}
    stage('Testing') {
      steps {
        bat(script: 'gradle test', returnStatus: true)
      }
    }
  }
  if(build_ok) {
        currentBuild.result = "SUCCESS"
    } else {
        currentBuild.result = "FAILURE"
    }
}
}
