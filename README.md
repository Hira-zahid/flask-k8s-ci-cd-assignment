# Flask Kubernetes CI/CD Assignment

## Project Description
This project demonstrates a **CI/CD pipeline for a Flask application using Jenkins and Kubernetes**.  
The application is containerized using Docker and deployed to a local Kubernetes cluster (Minikube).  
The pipeline automates building the Docker image, deploying to Kubernetes, and verifying the deployment.

### Kubernetes Features Used
- **Deployment:** Manages pods and application updates.
- **Service (NodePort):** Exposes the app outside the cluster.
- **Automated Rollouts:** Ensures smooth updates without downtime.
- **Scaling:** Easily increase or decrease the number of pods.
- **Load Balancing:** Distributes traffic across multiple pods for reliability.

## Running the Application Locally with Docker
1. Clone the repository:
   ```bash
   git clone https://github.com/Hira-zahid/flask-k8s-ci-cd-assignment.git
   cd flask-k8s-ci-cd-assignment

Build the Docker image:

docker build -t flask-k8s-app:latest .


Run the Docker container:

docker run -p 5000:5000 flask-k8s-app:latest


Visit http://localhost:5000
 in your browser.

Deployment via Jenkins

Ensure Jenkins is configured with Kubernetes access.

Pipeline stages:

Build Docker image

Deploy to Kubernetes using kubectl apply

Verify rollout and pods

Run the Jenkins pipeline → the app will be deployed to Kubernetes.

Automated Rollouts, Scaling, Load Balancing

Rollouts:

kubectl rollout status deployment/flask-deployment


Ensures smooth updates without downtime.

Scaling:

kubectl scale deployment flask-deployment --replicas=3


Increases the number of pods to handle more traffic.

Load Balancing:
NodePort service exposes the app to multiple pods for traffic distribution.


This is **100% proper Markdown syntax**:  
- Headings with `#`  
- Lists with `-`  
- Code blocks with triple backticks  
- Links formatted properly  

I can also make a **more detailed version with badges, images, and screenshots sections** so it looks submission-ready for your assignment.  

Do you want me to do that next?


Here’s a fully polished README.md in proper Markdown syntax, ready to paste and submit:

# Flask Kubernetes CI/CD Assignment

## Project Description
This project demonstrates a **CI/CD pipeline for a Flask application using Jenkins and Kubernetes**.  
The application is containerized using Docker and deployed to a local Kubernetes cluster (Minikube).  
The pipeline automates building the Docker image, deploying to Kubernetes, and verifying the deployment.

### Kubernetes Features Used
- **Deployment:** Manages pods and application updates.
- **Service (NodePort):** Exposes the app outside the cluster.
- **Automated Rollouts:** Ensures smooth updates without downtime.
- **Scaling:** Easily increase or decrease the number of pods.
- **Load Balancing:** Distributes traffic across multiple pods for reliability.

## Running the Application Locally with Docker
1. Clone the repository:
   ```bash
   git clone https://github.com/Hira-zahid/flask-k8s-ci-cd-assignment.git
   cd flask-k8s-ci-cd-assignment


Build the Docker image:

docker build -t flask-k8s-app:latest .


Run the Docker container:

docker run -p 5000:5000 flask-k8s-app:latest


Open your browser and visit http://localhost:5000
.

Deployment via Jenkins

Ensure Jenkins is configured with Kubernetes access.

Pipeline stages:

Build Docker image

Deploy to Kubernetes using kubectl apply

Verify rollout and pods

Run the Jenkins pipeline → the app will be deployed to Kubernetes.

Automated Rollouts, Scaling, Load Balancing

Rollouts:

kubectl rollout status deployment/flask-deployment


Ensures smooth updates without downtime.

Scaling:

kubectl scale deployment flask-deployment --replicas=3


Increases the number of pods to handle more traffic.

Load Balancing:
NodePort service exposes the app to multiple pods, distributing traffic for reliability.
