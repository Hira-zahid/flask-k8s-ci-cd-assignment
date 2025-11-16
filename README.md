3. Visit `http://localhost:5000` in your browser.

## Deployment via Jenkins
1. Ensure Jenkins is configured with Kubernetes access.
2. Pipeline stages:
- Build Docker image
- Deploy to Kubernetes (`kubectl apply`)
- Verify rollout and pods
3. Run the pipeline → app is deployed to Kubernetes.

## Automated Rollouts, Scaling, Load Balancing
- **Rollouts:** `kubectl rollout status deployment/flask-deployment` ensures smooth updates.  
- **Scaling:** `kubectl scale deployment flask-deployment --replicas=3` increases pods.  
- **Load Balancing:** NodePort service exposes app to multiple pods for traffic distribution.
