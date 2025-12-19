pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('HTML Validation') {
            steps {
                sh '''
                echo "Running HTML validation..."
                tidy -errors index.html
                '''
            }
        }

        stage('Build') {
            steps {
                echo 'Static website - no build required'
            }
        }
    }

    post {
        success {
            echo 'HTML validation passed. Pipeline SUCCESS.'
        }
        failure {
            echo 'HTML validation failed. Fix HTML errors.'
        }
    }
}
