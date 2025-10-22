pipeline {
    // Use any agent
  agent any
    // Set the environment variable APP_PORT=9090
  tools {
    maven '3.9.11' 
  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean install -U'
      }
    }
    stage('Unit Test') {
      steps {
        sh 'mvn test'
      }
    }
  }
}
