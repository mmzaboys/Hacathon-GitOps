## Installing NGINX Ingress

### Minikube

For local development with Minikube, enable the built-in NGINX Ingress Controller:

```bash
$ minikube addons enable ingress


In order to run this service:

1. Remove `sealed-secret.yaml`.

2. Add the `secrets.yaml` file that was sent to you privately.

3. Run the following command from the directory above the `kubernetes` directory:

$ kubectl apply -f ./kubernetes

On Aws
Cloud Provider

For a cloud Kubernetes cluster, install the NGINX Ingress Controller using Helm:

#installing helm 

curl https://baltocdn.com | gpg --dearmor | sudo tee /usr/share/keyrings/helm.gpg > /dev/null
sudo apt-get install apt-transport-https --yes
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/helm.gpg] https://baltocdn.com all main" | sudo tee /etc/apt/sources.list.d/helm-stable-debian.list
sudo apt-get update
sudo apt-get install helm


helm install ingress-nginx ingress-nginx/ingress-nginx \
  --namespace ingress-nginx \
  --create-namespace

helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
helm repo update

kubectl get pods -n ingress-nginx
kubectl get svc -n ingress-nginx