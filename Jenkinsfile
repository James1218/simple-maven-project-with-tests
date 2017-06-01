pipeline {
  agent any
  stages {
    stage('Preparation') {
      steps {
        parallel(
          "Preparation": {
            git 'https://github.com/jglick/simple-maven-project-with-tests.git'
            
          },
          "Define mvnHome": {
            tool 'M3'
            
          }
        )
      }
    }
  }
}