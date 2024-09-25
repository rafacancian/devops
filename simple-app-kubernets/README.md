## Kubernetes Project

### Simple App Hello World

```
kubectl get get pods
kubectl get pods -n dev 

kubectl create deployment hello-node --image=k8s.gcr.io/echoserver:1.4
kubectl create deployment hello-node --image=k8s.gcr.io/echoserver:1.4 -n dev
kubectl get deployments --all-namespaces
kubectl get events -n dev
kubectl expose deployment hello-node --type=LoadBalancer --port=8080
kubectl get services
minikube service hello-node

//On cloud providers that support load balancers, an external IP address would be provisioned to access the Service. 
//On minikube, the LoadBalancer type makes the Service accessible through the minikube service command.
```

### Deployments

```
kubectl apply -f solution/v1.yaml
```

### Service LoadBalancers

```
kubectl apply -f solution/v2.yaml
```

### Config Maps and Scaling

```
kubectl apply -f solution/v3.yaml
```

### Resource Limits

```
kubectl apply -f solution/v4.yaml
```

### Troubleshooting, Logs, Rollouts, Draining Nodes

```
kubectl describe deployment mydeployment
```

### Logs

```
kubectl logs -f -l app=mywebapp
```

### Rollouts

```
kubectl rollout
k rollout restart deployment mydeployment
kubectl drain minikube --ignore-daemonsets=true --force
```