pipeline {
  agent any
  stages {
    stage('Build Jar') {
      agent any
      steps {
        sh '''cd 17646-petclinic-pipeline_main
./mvnw package
java -jar target/*.jar'''
      }
    }

  }
}