pipeline {
  agent any
  stages {  
    stage('Build') {
      steps {
          sh "./gradlew clean build"
      }
    }
    
    stage ('Sonarqube Analysis') {
      steps {
        withSonarQubeEnv('java-gradle') {
          sh "./gradlew sonarqube"
        }
      }
    }
  }
}
