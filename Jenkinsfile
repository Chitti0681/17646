pipeline {
  agent any
  stages {
    stage('Build jar') {
      steps {
        sh '''cd spring-petclinic-main
mvn package
'''
        stash 'Target'
      }
    }

    stage('Execute jar') {
      steps {
        unstash 'Target'
        sh '''cd spring-petclinic-main
java -jar target/*.jar
'''
      }
    }

  }
}