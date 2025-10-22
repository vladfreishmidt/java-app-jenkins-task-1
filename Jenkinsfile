pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M3"
    }
    environment {
        APP_PORT = '9090'
    }

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                // Run Maven on a Unix agent.
                sh "mvn -Dmaven.test.failure.ignore=true clean package"

                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }
        }
        stage('Unit Tests') {
            steps {
                sh 'mvn test' // Execute the Maven test phase to run unit tests
            }
        }
    }
}

