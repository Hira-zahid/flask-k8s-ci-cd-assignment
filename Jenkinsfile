pipeline {
    agent any

    environment {
        IMAGE_NAME = "flask-app:latest"
        KUBE_NAMESPACE = "default"
    }

    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build("${IMAGE_NAME}")
                }
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                script {
                    sh "kubectl apply -f kubernetes/deployment.yaml"
                    sh "kubectl apply -f kubernetes/service.yaml"
                }
            }
        }

        stage('Verify Deployment') {
            steps {
                script {
                    sh "kubectl rollout status deployment/flask-deployment"
                    sh "kubectl get pods"
                    sh "kubectl get services"
                }
            }
        }
    }
}
git add Jenkinsfile