# 🚀 Kubernetes

## 📖 What is Kubernetes?

**Kubernetes (K8s)** is an open-source container orchestration platform. It helps you run, manage, scale, and automate containerized applications — most commonly Docker containers — across a cluster of machines. <br>
Is like an operating system for your containers. <br>
Instead of running one app on one server, Kubernetes lets you run many containers across many servers, and it manages all the complexity for you.

![k8s](https://github.com/user-attachments/assets/213c52b2-50d6-4cbd-b1d1-d2e7a1c0261d)

---

# Key features:
Restarts crashed containers, replaces failed pods <br>
Lets containers find each other without hardcoding IPs <br>
Deploys app updates with zero downtime <br>
Automatically scale apps up/down based on demand <br>
Distributes traffic across services automatically <br>
Store passwords, tokens, configs securely <br>

# Components:
kube-apiserver: API you talk to via kubectl <br>
etcd: stores the state of the cluster <br>
kubelet: runs on each node, manages containers <br>
kube-proxy: handles networking between pods and services <br>

# Why Learn Kubernetes:
It’s the industry standard for deploying apps at scale. <br>
Used by big companies like Netflix, Google <br>
Cloud-native jobs increasingly require it. <br>

Cluster info commands:
```
kubectl cluster-info - Shows cluster details
kubectl get nodes - Lists all nodes in the cluster
kubectl get pods - Lists pods in the current namespace
kubectl get all	- Lists all resources (pods, svc, etc.)
kubectl get namespaces	- Lists all namespaces
kubectl config current-context	- Shows the current context (cluster config)
kubectl proxy - expose Dashboard - for local access
```
Managing Workloads commands:
```
kubectl create deployment nginx --image=nginx	- Creates a deployment running NGINX
kubectl get deployments	- Lists all deployments
kubectl delete deployment nginx	- Deletes the nginx deployment
kubectl scale deployment nginx --replicas=3	- Scales nginx deployment to 3 pods
kubectl rollout restart deployment nginx	- Restarts the deployment (pods refresh)
```
Services & Networking commands:
```
kubectl expose deployment nginx --port=80 --type=NodePort	- Creates a service to expose the app
kubectl get svc	- Lists all services
kubectl describe svc nginx	- Detailed info about the service
```
YAML Files commands:
```
kubectl apply -f app.yaml -	Applies config from a YAML file
kubectl delete -f app.yaml -	Deletes resources defined in the YAML file
kubectl edit deployment nginx	- Opens live YAML editor in terminal
kubectl get deployment nginx -o yaml -	Shows full YAML config
```
