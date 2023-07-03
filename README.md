# rabbitmq-cluster-k8s

## Instructions:
```
$ kubectl create ns rabbits
$ kubectl get storageclass
```

## Deployment 
```
$ kubectl apply -n rabbits -f .\kubernetes\rabbit-rbac.yaml
$ kubectl apply -n rabbits -f .\kubernetes\rabbit-configmap.yaml
$ kubectl apply -n rabbits -f .\kubernetes\rabbit-secret.yaml
$ kubectl apply -n rabbits -f .\kubernetes\rabbit-statefulset.yaml
```

## Access 
```
$ kubectl -n rabbits port-forward rabbitmq-0 8080:15672
or 
$ kubectl -n rabbits .\kubernetes\service-client.yaml

Go to htttp://localhost:8080 or htttp://localhost:15672
Username: guest
Password: guest
```

## Useful links
https://blog.rabbitmq.com/posts/2020/08/deploying-rabbitmq-to-kubernetes-whats-involved/
