pipeline {
  agent any
  stages {
    stage('Preparation') {
      steps {
        git 'https://github.com/James1218/simple-maven-project-with-tests.git'
        sh '${mvnHome} = tool \'M3\''
      }
    }
  }
  environment {
    mvnHome = ''
  }
}