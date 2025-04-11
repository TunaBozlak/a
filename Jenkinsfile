pipeline {
    agent any

    tools {
        nodejs "NodeJS_18"
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test' // test script'in yoksa yorum satırı yapabilirsin
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
    }

    post {
        success {
            echo "✅ Pipeline başarılı"
        }
        failure {
            echo "❌ Pipeline başarısız"
        }
    }
}

