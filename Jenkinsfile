pipeline {
  agent any
  stages {
    stage('Preparation') {
      steps {
        git 'https://github.com/James1218/simple-maven-project-with-tests.git'
        tool 'M3'
      }
    }
    stage('build') {
      steps {
        bat 'mvn Checks if running on a Unix-like node'
      }
    }
  }
}