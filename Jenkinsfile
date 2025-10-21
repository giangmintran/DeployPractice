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
                echo "🔧 Building project..."
                sh 'dotnet build'
            }
        }

        stage('Test') {
            steps {
                echo '🧪 Running tests...'
                sh 'dotnet test MyApp.sln'
            }
        }

        stage('Docker Build') {
            steps {
                echo '🐳 Building Docker image...'
                sh 'docker build -t myapp:latest .'
            }
        }
    }
}
