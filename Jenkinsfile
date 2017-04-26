pipeline {
  agent any
  stages {
    stage('Preparation') {
      steps {
        bat 'echo Hello start'
        tool 'M3'
      }
    }
    stage('Build') {
      steps {
        bat 'echo middle'
      }
    }
    stage('Results') {
      steps {
        bat 'echo Done'
      }
    }
  }
}