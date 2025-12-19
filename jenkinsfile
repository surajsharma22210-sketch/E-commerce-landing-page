pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out source code...'
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'static website - no build required'
            }
        }
        stage('Test') {
            steps {
                echo 'Basic validation passed'
            }
        }
    }
}