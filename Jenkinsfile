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

  }
}