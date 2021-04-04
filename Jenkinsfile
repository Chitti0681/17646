pipeline {
  agent any
  stages {
    stage('Build jar file') {
      agent any
      steps {
        sh '''cd spring-petclinic-main
mvn package'''
        stash(name: 'Target', includes: '**/target/*.jar')
      }
    }

  }
}