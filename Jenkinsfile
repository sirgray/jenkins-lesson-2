pipeline {
    agent none // Do not assign a global machine yet

    stages {
        stage('Test Node.js App') {
            agent {
                docker { image 'node:18-alpine' }
            }
            steps {
                echo '=== Running inside Node.js Container ==='
                sh 'node --version'
                sh 'npm --version'
            }
        }

        stage('Test Python App') {
            agent {
                docker { image 'python:3.11-slim' }
            }
            steps {
                echo '=== Running inside Python Container ==='
                sh 'python --version'
                sh 'pip --version'
            }
        }
    }
}
