## ArgoCD Project

---

### Install Argo-cd into your Cluster

https://argo-cd.readthedocs.io/en/stable
https://argo-cd.readthedocs.io/en/stable/operator-manual/installation/
https://github.com/argoproj/argo-cd/tree/master/manifests/install.yaml

```
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
kubectl get pods -n argocd
```

### Port forward

```
kubectl port-forward svc/argocd-server -n argocd 8080:443
```

### Get Access

User: admin \
Password:

```
argocd admin initial-password -n argocd
```

### Reference

https://argo-cd.readthedocs.io/en/stable/getting_started/
