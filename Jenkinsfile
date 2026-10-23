pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                bat 'python --version'
                bat 'python app.py'
            }
        }

        stage('Test') {
            steps {
                echo 'Running test cases...'
                bat 'python -m unittest test_app.py'
            }
        }
    }

    post {
        success {
            echo 'Build and tests completed successfully!'
        }
        failure {
            echo 'Build or tests failed!'
        }
    }
}