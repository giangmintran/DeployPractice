pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo '🔧 Building project...'
                bat 'dotnet build MyApp.sln'
            }
        }

        stage('Test') {
            steps {
                echo '🧪 Running tests...'
                bat 'dotnet test MyApp.sln'
            }
        }

        stage('Docker Build') {
            steps {
                echo '🐳 Building Docker image...'
                bat 'docker build -t myapp:latest .'
            }
        }
    }
}
