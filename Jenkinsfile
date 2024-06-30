pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/9-anonymous/Pipeline.git'
            }
        }

        stage('Build') {
            steps {
                sh 'ls -a'
                sh 'cd Pipeline'
                sh 'cp index.html /var/www/html/'  // Adjust path as per your server configuration
            }
        }
    }

    post {
        success {
            echo 'Build successful! Deployed index.html.'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}

