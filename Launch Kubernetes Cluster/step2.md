The cluster can be interacted with using the kubectl CLI. This is the main approach used for managing Kubernetes and the applications running on top of the cluster.

Details of the cluster and its health status can be discovered via 
`kubectl cluster-info`{{execute}}

#### Task
Copy the following definition to the editor. The definition defines how to launch an application called webapp1 using the Docker Image katacoda/docker-http-server that runs on Port 80.

`apiVersion: extensions/v1beta1
kind: Deployment
metadata:
  name: webapp1
spec:
  replicas: 1
  template:
    metadata:
      labels:
        app: webapp1
    spec:
      containers:
      - name: webapp1
        image: katacoda/docker-http-server:latest
        ports:
        - containerPort: 80`

This is deployed to the cluster with the command
`kubectl create -f deployment.yaml`{{execute}}

As it's a Deployment object, a list of all the deployed objects can be obtained via-
`kubectl get deployment`{{execute}}

Details of individual deployments can be outputted with-
`kubectl describe deployment webapp1`{{execute}}

