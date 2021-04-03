pipeline {
  agent any
  stages {
    stage('Build Jar') {
      agent any
      steps {
        sh '''cd spring-petclinic-main
mvn -version
chmod u+x mvnw
mvn package '''
      }
    }

    stage('Execute Jar') {
      steps {
        sh 'java -jar target/*.jar'
      }
    }

  }
}