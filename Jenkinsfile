pipeline {
  agent any
  stages {
    stage('Preparation') {
      steps {
        bat 'set tool=M3'
        git 'https://github.com/DannySe/simple-maven-project-with-tests.git'
        tool 'M3'
      }
    }
    stage('Build') {
      steps {
        bat 'echo %tool%'
        bat(script: 'set mvnhome=%MVN_HOME%', encoding: 'UTF-8')
      }
    }
    stage('Results') {
      steps {
        bat 'echo Done'
      }
    }
  }
}