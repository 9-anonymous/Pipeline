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
                sh 'echo "Hello"'
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

