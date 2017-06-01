pipeline {
  agent any
  stages {
    stage('Preparation') {
      steps {
        git 'https://github.com/James1218/simple-maven-project-with-tests.git'
        tool 'M3'
      }
    }
    stage('Build') {
      steps {
        bat 'mvn -Dmaven.test.failure.ignore clean package'
      }
    }
    stage('Test') {
      steps {
        junit '**/target/surefire-reports/TEST-*.xml'
      }
    }
  }
}