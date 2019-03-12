

```
apiVersion: v1
kind: Node
metadata:
  name: webapp1-svc
  labels:
    app: webapp1
```
`kubectl create -f node.yaml`{{execute}}

`kubectl get nodes`{{execute}}
