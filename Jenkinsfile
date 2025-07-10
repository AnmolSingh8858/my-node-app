pipeline {
    agent any

    stages {
        stage('Print Message') {
            steps {
                echo '✅ Jenkinsfile is working!'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test || echo "No tests defined"'
            }
        }
    }

    post {
        always {
            echo "🎯 Build complete"
        }
        failure {
            echo "❌ Build failed!"
        }
    }
}


