
pipeline {
    agent any

    environment {
        PYTHON = 'C:\\Users\\sahan\\AppData\\Local\\Programs\\Python\\Python312\\python.exe'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                bat '"%PYTHON%" --version'
                bat '"%PYTHON%" app.py'
            }
        }

        stage('Test') {
            steps {
                echo 'Running test cases...'
                bat '"%PYTHON%" -m unittest test_app.py'
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
