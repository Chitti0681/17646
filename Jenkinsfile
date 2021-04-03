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
        stash(name: 'save Target', includes: '**/targettarget/*.jar')
      }
    }

    stage('Execute Jar') {
      steps {
        sh 'java -jar target/*.jar'
      }
    }

  }
}