pipeline {
    // Use any agent
    agent any
    // Set the environment variable APP_PORT=9090
    stages {
        stage('Build') {
            steps {
                // Use the maven package phase to build the project
                sh 'mvn -B -DskipTests clean package'
            }
        }
        stage('Unit Test') {
            steps {
                 // Use the maven test phase to run unit tests
            }
        }
    }
}
