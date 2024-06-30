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
                sh 'make build' // Replace with your build command
            }
        }
        stage('Test') {
            steps {
                sh 'make test' // Replace with your test command
            }
        }
    }
}
