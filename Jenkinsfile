pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Fetch source code from repository
                git branch: 'main', url: 'https://github.com/Manobhiramreddy/4-package-manager-integration.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                echo 'Installing dependencies...'
                bat 'npm install'
            }
        }

        stage('Build') {
            steps {
                echo 'Running the Node.js application...'
                bat 'node app.js'
            }
        }
    }

    post {
        success {
            echo 'Build completed successfully ✅'
        }
        failure {
            echo 'Build failed ❌'
        }
    }
}
