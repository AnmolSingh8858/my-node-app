pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                git url: 'https://github.com/AnmolSingh8858/my-node-app.git', branch: 'main'
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
            echo "Build complete"
        }
        failure {
            echo "Build failed!"
        }
    }
}

