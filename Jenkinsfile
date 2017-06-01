pipeline {
  def mvnHome
  agent any
  stages {
    stage('Preparation') {
      steps {
        git 'https://github.com/James1218/simple-maven-project-with-tests.git'
        mvnHome = tool 'M3'
      }
    }
    stage('Build') {
      steps {
        if (isUnix()) {
          sh "'${mvnHome}/bin/mvn' -Dmaven.test.failure.ignore clean package"
        } else {
         bat(/"${mvnHome}\bin\mvn" -Dmaven.test.failure.ignore clean package/)
        }
      }
    }
    stage('Results') {
      steps {
        junit '**/target/surefire-reports/TEST-*.xml'
        archiveArtifacts 'target/*.jar'
      }
    }
  }
}
