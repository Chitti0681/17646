pipeline {
  agent any
  stages {
    stage('Build Jar') {
      agent any
      steps {
        sh '''mvn package
java -jar target/*.jar'''
      }
    }

  }
}