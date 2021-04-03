pipeline {
  agent any
  stages {
    stage('Build Jar') {
      agent any
      steps {
        sh '''cd spring-petclinic-main
mvn -version
#chmod u+x mvnw
#./mvnw package '''
      }
    }

  }
}