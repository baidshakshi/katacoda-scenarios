

```
apiVersion: v1
kind: Pod
metadata: 
  labels: 
    app: webapp1
  name: nginx
spec: 
  containers: 
    - 
      image: "katacoda/docker-http-server:latest"
      name: webapp1
      ports: 
        - 
          containerPort: 80
```
`kubectl create -f node.yaml`{{execute}}

`kubectl get nodes`{{execute}}
