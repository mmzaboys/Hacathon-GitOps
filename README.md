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