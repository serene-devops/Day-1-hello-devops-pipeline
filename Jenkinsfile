pipeline {
    agent any

    environment {
        IMAGE_NAME = "hello-devops-app"
        CONTAINER_NAME = "hello-devops-app"
        APP_PORT = "5000"
    }

    stages {

        stage('Checkout Code') {
            steps {
                // Pull latest code from GitHub
                git branch: 'main', url: 'https://github.com/serene-devops/hello-devops.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    sh "docker build -t ${IMAGE_NAME} ."
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                script {
                    // Stop & remove old container if exists
                    sh "docker rm -f ${CONTAINER_NAME} || true"

                    // Run the new container
                    sh "docker run -d -p ${APP_PORT}:${APP_PORT} --name ${CONTAINER_NAME} ${IMAGE_NAME}"
                }
            }
        }

        stage('Post-Build Cleanup (Optional)') {
            steps {
                script {
                    // Remove dangling images to save space
                    sh "docker image prune -f || true"
                }
            }
        }
    }

    post {
        success {
            echo "✅ Pipeline completed successfully! App is running on port ${APP_PORT}"
        }
        failure {
            echo "❌ Pipeline failed. Check logs."
        }
    }
}

