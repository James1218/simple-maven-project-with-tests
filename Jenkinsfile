pipeline {
  agent any
  stages {
    stage('Preparation') {
      steps {
        git 'https://github.com/jglick/simple-maven-project-with-tests.git'
      }
    }
  }
  environment {
    mvnHome = 'tool \'M3\''
  }
}