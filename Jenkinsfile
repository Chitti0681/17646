pipeline {
  agent any
  stages {
    stage('Build jar') {
      steps {
        sh '''cd spring-petclinic-main
mvn sonar:sonar \\
  -Dsonar.projectKey=petclinic-analysis \\
  -Dsonar.host.url=http://192.168.33.20:9000 \\
  -Dsonar.login=a334579e75b11973b86cb546c0e17ea8d9edd778'''
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