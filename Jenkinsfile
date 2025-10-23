pipeline {
    agent any
    tools {
        maven "3.9.11"
        jdk "jdk17"
    }
    environment {
        APP_PORT = '9090'
    }
    stages {
        stage('Build') {
            steps {
                sh "mvn -B clean package"
            }
        }
        stage('Unit Tests') {
            steps {
                sh 'mvn test'
            }
        }
    }
}

