pipeline {
    agent any

    environment {
        IMAGE_NAME = "abd1rehman/flask-k8s-app"
        IMAGE_TAG = "latest"
        KUBE_NAMESPACE = "default"
    }

    stages {

        stage('Build Docker Image') {
            steps {
                bat """
                docker build -t %IMAGE_NAME%:%IMAGE_TAG% .
                docker images
                """
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                bat """
                kubectl apply -f kubernetes/deployment.yaml
                kubectl apply -f kubernetes/service.yaml
                """
            }
        }

        stage('Verify Deployment') {
            steps {
                bat """
                kubectl rollout status deployment/flask-deployment
                kubectl get pods
                kubectl get svc
                """
            }
        }
    }
}
