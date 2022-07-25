pipeline {
  agent any
  stages {  
    stage('Build') {
      steps {
        withSonarQubeEnv('java-gradle') {
          sh "./gradlew sonarqube"
          }
        }
      }
    }
  }
