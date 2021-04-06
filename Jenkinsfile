pipeline {
  agent any
  stages {
    stage('Build jar') {
      steps {
        sh '''sonar.projectKey=Petclinic
sonar.projectName=Project1
sonar.projectVersion=1.0.0
sonar.projectDescription=Static analysis for the Petclinic
sonar.sources=spring-petclinic-main
'''
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