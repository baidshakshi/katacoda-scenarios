Kubernetes has powerful networking capabilities that control how applications communicate. These networking configurations can also be controlled via YAML.

#### Task
Copy the Service definition to the editor. The Service selects all applications with the label webapp1. As multiple replicas, or instances, are deployed, they will be automatically load balanced based on this common label. The Service makes the application available via a NodePort.

```
apiVersion: v1
kind: Service
metadata:
  name: webapp1-svc
  labels:
    app: webapp1
spec:
  type: NodePort
  ports:
  - port: 80
    nodePort: 30080
  selector:
    app: webapp1
```
All Kubernetes objects are deployed in a consistent way using kubectl.

Deploy the Service with `kubectl create -f service.yaml`{{execute}}

As before, details of all the Service objects deployed with kubectl get svc. By describing the object it's possible to discover more details about the configuration 
`kubectl describe svc webapp1-svc`{{execute}}

`curl master:30080`{{execute}}

