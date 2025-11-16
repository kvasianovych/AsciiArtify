## Install and Setup ArgoCD

### Prerequisites
- Docker
- Minikube OR Kind OR K3D
- kubectl

### Installation
1. Create cluster
`k3d cluster create $CLUSTER_NAME`

2. Create a separate namespace for ArgoCD
`kubectl create namespace $ARGOCD_NAMESPACE_NAME`

3. Install ArgoCD
`kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml`

4. Get automatically generated password for `admin` user.
`ARGO_ADMIN_PASS=$(kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d) && echo $ARGO_ADMIN_PASS`

5. Use K8S port forwarding to provide acess.
`kubectl port-forward svc/argocd-server -n argocd 8080:443`

6. Open `127.0.0.1:8080` in you web browser.

7. Cleanup if needed.
