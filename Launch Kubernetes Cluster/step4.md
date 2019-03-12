

```
apiVersion: v1
kind: Pod
metadata:
  name: webapp1-node
spec:
  containers:
  - name: webapp1
	image: katacoda/docker-http-server:latest
    resources:
      limits:
        memory: "200Mi"
      requests:
        memory: "100Mi"
    command: ["stress"]
    args: ["--vm", "1", "--vm-bytes", "150M", "--vm-hang", "1"]
```
`kubectl create -f node.yaml`{{execute}}
`kubectl get nodes`{{exec}}
