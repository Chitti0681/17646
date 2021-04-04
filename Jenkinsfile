pipeline {
  agent docker
  stages {
    stage('Build Jar') {
      agent docker
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
        sh '''cd spring-petclinic-main
ls
java -jar target/*.jar'''
      }
    }

  }
}
