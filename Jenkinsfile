pipeline {
  agent any
  stages {
    stage('Build Jar') {
      agent any
      steps {
        sh '''./mvnw package
java -jar target/*.jar'''
      }
    }

  }
}