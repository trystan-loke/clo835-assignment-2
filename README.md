# This project demonstrate the deployment of an API service by leveraging Docker and Kubernetes

# Steps
## 1. Build docker image
```docker build -t clo835-assignment-2:latest .```

## 2. Run docker container
```docker run --name clo835-assignment-2 -p 3030:3030 -d clo835-assignment-2:latest```

## 3. Tag and Push docker image to docker hub
```docker tag clo835-assignment-2:latest trystan00000/clo835-assignment-2:latest```
```docker push trystan00000/clo835-assignment-2:latest```

## 4. Install minikube for local k8s cluster
### url: https://minikube.sigs.k8s.io/docs/start/?arch=%2Fmacos%2Fx86-64%2Fstable%2Fbinary+download

## 5. Start minikube
```minikube start```

## 6. Create k8s deployment
```kubectl apply -f deployment.yml```

## 7. Create k8s service
```kubectl apply -f service.yml```

## 8. Use minikube to open the service
```minikube service clo835-assignment-2-service```

## 9. Access the url mentioned in minikube console
