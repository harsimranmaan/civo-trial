# civo-trial
Experiments with the Civo k3s cloud

## Setup

Create a medium 3-node k3s cluster

```bash
export KUBECONFIG=kubeconfigfile
kubectl get nodes
```


## Install cert-manager

Follow https://github.com/civo/kubernetes-marketplace/blob/6ec81e0d2693957a5ccecfc4238ad6d088c77eca/cert-manager/install.sh

```bash
kubectl create namespace cert-manager

#helm3 
helm install \
  cert-manager jetstack/cert-manager \
  --namespace cert-manager \
  --version v1.0.4 \
  --set installCRDs=true
  
```

 Verify
 ```bash
 kubectl get pods --namespace cert-manager
 ```

