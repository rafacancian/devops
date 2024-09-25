## DEVOPS Projects

### Minikube commands

Installation: https://minikube.sigs.k8s.io/docs/start/

```
minikube config set driver docker
minikube start // stop
minikube status
minikube dashboard --url
minikube service <applicaiton-service-name>
```

### Kubectl Installation/Configuration

Installation: https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/

```
curl -LO "https://dl.k8s.io/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl.sha256"
sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl


cat ~/.kube/config  // kubectl config view
alias k='kubectl'
```

### Kubectl commands

```
kubectl get namespace
kubectl get deployment
kubectl get replicasetP
kubectl get configmap
kubectl get nodes
kubectl describe nodes
kubectl get events
minikube service mywebapp
```

### Cluster Management

```
kubectl cluster-info
kubectl get nodes
kubectl describe node minikube
kubectl cordon minikube
kubectl drain minikube --ignore-daemonsets=true --force
kubectl uncordon minikube
```

### Namespaces

```
kubectl get namespace
kubectl create namespace dev
kubectl create namespace test
kubectl delete namespace test
k create -f namespaces/namespace-prod.yaml
k describe namespace prod

# OPTIONAL
kubectl config set-context --current --namespace=<NAMESPACE NAME>
```
