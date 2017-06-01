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
        isUnix()
        sh 'mnv -Dmaven.test.failure.ignore clean package'
        bat 'mvn -Dmaven.test.failure.ignore clean package'
      }
    }
  }
}