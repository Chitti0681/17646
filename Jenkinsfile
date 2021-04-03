pipeline {
  agent any
  stages {
    stage('Build Jar') {
      agent any
      steps {
        sh '''cd spring-petclinic-main
sudo ./mvnw package
java -jar target/*.jar'''
      }
    }

  }
}