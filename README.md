# k8s_for_noob
Dedicated repo for my study

# Subir minikube 

```
1-Enable Hyper-v Windows 10
2-Create Virtual Switch for external network
3-minikube start --driver=hyperv --hyperv-virtual-switch="VSwitch"
4-minikube addons enable ingress
5-minikube ip
6-minikube delete
```
# Lab-001:

1-List Namespace:
```
kubectl get namespaces
```
2-Create Namespace:
```
kubectl create namespace angelinux
```
3-Set and utilize name space:
```
kubectl config set-context --current --namespace=angelinux
```
4-Execute pod nginx:
```
kubectl run nginx --image=nginx
```
5-List your pods:
```
kubectl get pods
```
6-Delete pod:
```
kubectl delete pods/nginx
```
