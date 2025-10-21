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
            }
        }

        stage('Test') {
            steps {
                echo '🧪 Running tests...'
            }
        }

        stage('Docker Build') {
            steps {
                echo '🐳 Building Docker image...'
            }
        }
    }
}
