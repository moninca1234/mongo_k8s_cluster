
# Deploying MongoDB and Mongo-express in Kubernetes
This project demonstrates how to deploy MongoDB and Mongo-express in Kubernetes using YAML files.


## Prerequisite

-  Minikube cluster running


## Steps to deploy MongoDB and Mongo Express using Kubernetes:

- Created ConfigMap for DB Server URL
- Create a Secret to store the credentials of the mongodb 
- Create a Deployment to run the MongoDB pods
- Create a ClusterIP Service to expose MongoDB within the cluster
- Create a Deployment to run the Mongo Express pods
- Created MongoExpress External Service




## How to Deploy

##### Apply the ConfigMap and Secrets


```http
  kubectl apply -f mongo-configmap.yml
  kubectl apply -f mongo-secrets.yml

```
##### Apply the MongoDB resources:

```http
  kubectl apply -f mongodb-deployment.yml

```
##### Apply the MongoExpress resources:

```http
  kubectl apply -f mongodb-express.yml

```
##### give a URL to external service in minikube
```http
  minikube service mongo-express-service

```



