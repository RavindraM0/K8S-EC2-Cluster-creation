# Kubernetes Cluster on AWS EC2 (kubeadm)

Two-node cluster (1 master + 1 worker) on Ubuntu EC2, containerd runtime, Calico CNI (pod CIDR 192.168.0.0/16).

## Deploy the app

    kubectl create namespace ravindra
    kubectl apply -f k8s/manifest.yaml -n ravindra
    kubectl get pods -n ravindra -o wide
    kubectl get svc -n ravindra
## nginx
    /nginx.png

## Access

The nginx app is exposed through a NodePort service: `http://<worker-public-ip>:30080`

## Contents

- `k8s/manifest.yaml`: Deployment (10 nginx replicas) and NodePort Service (30080)
