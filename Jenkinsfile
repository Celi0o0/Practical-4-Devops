pipeline {
    agent any // Runs the pipeline on any available Jenkins agent

    stages {
        stage('Checkout') {
            steps {
                // Pulls code from your Git repository
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application...'
                // Example for Node.js: sh 'npm install'
                // Example for Maven: sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                echo 'Running unit tests...'
                // Example: sh 'npm test' or sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application to production...'
                // Example: sh './deploy.sh' or Docker commands
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished. Cleaning up workspace...'
        }
        success {
            echo 'Pipeline succeeded! 🎉'
        }
        failure {
            echo 'Pipeline failed. ❌'
        }
    }
}
