pipeline {
  agent any
  stages {
    stage('Preparation') {
      steps {
        git 'https://github.com/DannySe/simple-maven-project-with-tests.git'
      }
    }
    stage('Build') {
      steps {
        bat 'mvn -Dmaven.test.failure.ignore clean package'
      }
    }
    stage('Results') {
      steps {
        bat 'echo Done'
      }
    }
  }
}