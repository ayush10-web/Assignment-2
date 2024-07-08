Docker:
Created the docker file exposing the application to the 3030 port.

To initialize the docker:
1. docker build -t app.py . 
2. docker tag app.py username/app.py:latest  
3. docker push username/app.py:latest 

After this docker image is created and pushed into the docker hub.

Kubernetes:

Deployment and Service yaml files are made in order to contanarized the application and host it in kubernetes.

To deploy kubernetes:
1. kubectl apply -f deployment.yaml
2. kubectl apply -f service.yaml
3. minikube service apppy-service 