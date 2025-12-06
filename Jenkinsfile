pipeline {
    agent any

    environment {
        APP_ENV = "production"
        VERSION = "1.0.0"
    }

    stages {
        stage('Checkout') {
            steps {
                echo "Checking out source code..."
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                echo "Installing dependencies..."
               
            }
        }

        stage('Build') {
            steps {
                echo "Building project..."
                sh 'python3 test.py'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."

            }
        }
    }

    post {
        success {
            echo "Pipeline finished successfully!"
        }
        failure {
            echo "Pipeline failed!"
        }
    }
}
