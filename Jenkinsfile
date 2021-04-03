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
        stash(name: 'Target', includes: '**/target/*.jar')
      }
    }

    stage('Execute Jar') {
      steps {
        unstash 'Target'
        sh '''ls
java -jar target/*.jar'''
      }
    }

  }
}