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
                sh 'cp ~/Documents/My-Pipeline/Pipeline/index.html /var/www/html/' // Use $WORKSPACE to refer to Jenkins workspace
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

