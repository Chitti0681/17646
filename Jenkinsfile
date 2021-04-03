pipeline {
  agent any
  stages {
    stage('Build Jar') {
      agent any
      steps {
        sh '''cd spring-petclinic-main
./mvnw package '''
      }
    }

  }
}