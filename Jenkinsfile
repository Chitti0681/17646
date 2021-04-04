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

    stage('Execute jar') {
      steps {
        unstash 'Target'
        sh 'java -jar target/*.jar'
      }
    }

  }
}