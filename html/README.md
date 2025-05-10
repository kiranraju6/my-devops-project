# Steps to Deploy Your Application on Kubernetes from Docker Hub
---
## Build and Push Docker Images to Docker Hub
- To get started, you'll need to build Docker images for each project (Node.js, HTML, and Python), tag them, and then push them to your Docker Hub repository. Use the following commands for each project:

Example Commands:
```
docker build -t <your-dockerhub-username>/<your project>:<tag> .
docker push <your-dockerhub-username>/<your project>:<tag>
```

Replace <your-dockerhub-username> with your Docker Hub username and <tag> with the appropriate tag (e.g., latest).

---

## Create Kubernetes Deployment and Service Manifest Files
- Next, you’ll need to create Kubernetes manifest files to define the deployment and expose the services. These files will pull the images you’ve just pushed to Docker Hub.

---

## Deploy the Application to Kubernetes
- Once the manifest files are ready, apply them to your Kubernetes cluster to create the deployments and services:

### To apply
```
kubectl apply -f <....-deployment>.yaml
kubectl apply -f <....-service>.yaml
```

### To delete
```
kubectl delete -f <....-deployment>.yaml
kubectl delete -f <....-service>.yaml
```

### To replace
```
kubectl replace -f <....-deployment>.yaml
kubectl replace -f <....-service>.yaml
```
---

## Verify the Deployment and Access the Application
- After applying the manifest files, check the status of the deployments and services:

### Check Pods:
```
kubectl get pods
```

### Check Services (to get the external IPs if using LoadBalancer):
```
kubectl get services
```

The output should display the external IP address assigned to the service (if using LoadBalancer). You can access the deployed applications using these external IP addresses in your browser.

---

## Summary of Steps
- Build and Push Docker images to Docker Hub for each project.

- Create Kubernetes Deployment and Service Manifest Files to define your application and services.

- Apply the Kubernetes Files using kubectl apply to deploy the application to your cluster.

- Expose the Application through a service (LoadBalancer or NodePort) to make it accessible.

- Verify Deployment by checking the status of your pods and services using kubectl get pods and kubectl get services.

- Once the deployment is successful, you can access your application via the external IP of the LoadBalancer service.
