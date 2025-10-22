pipeline {
    // Use any agent
  agent any
    // Set the environment variable APP_PORT=9090
  tools {
    maven 'apache-maven-3.0.1' 
  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn -B -DskipTests clean package'
      }
    }
    stage('Unit Test') {
      steps {
        sh 'mvn test'
      }
      post {
        always {
          junit 'target/surefire-reports/*.xml'
        }
      }
    }
  }
}
