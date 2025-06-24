# Install Argo CD

### Install Argo CD using manifests
```sh
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```
### Access the Argo CD UI (Loadbalancer service)
```sh
kubectl patch svc argocd-server -n argocd -p '{"spec": {"type": "LoadBalancer"}}'
```
### Get the Loadbalancer service IP
```sh
kubectl get svc argocd-server -n argocd
```


##### Get Intial Creds of ArgoCD

###### Username
```sh
admin
```
###### Initial Password
```
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d && echo
```
