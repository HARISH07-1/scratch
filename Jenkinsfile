pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Code checked out from GitHub'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh '''
                docker build -t scratch-app .
                '''
            }
        }

        stage('Run Docker Container') {
            steps {
                sh '''
                docker rm -f scratch-container || true
                docker run -d -p 80:80 --name scratch-container scratch-app
                '''
            }
        }
    }

    post {
        success {
            echo 'Application deployed successfully on port 80'
        }
    }
}
        }

        stage('Build Docker Image') {
            steps {
                sh '''
                docker build -t scratch-app .
                '''
            }
        }

        stage('Run Docker Container') {
            steps {
                sh '''
                docker rm -f scratch-container || true
                docker run -d -p 80:80 --name scratch-container scratch-app
                '''
            }
        }
    }

    post {
        success {
            echo 'Application deployed successfully on port 80'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Code checked out successfully'
            }
        }

        stage('Build') {
            steps {
                echo 'Build stage running'
            }
        }

        stage('Test') {
            steps {
                echo 'Test stage running'
            }
        }
    }
}
