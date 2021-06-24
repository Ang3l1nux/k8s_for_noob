# k8s_for_noob
Dedicated repo for my study
! 

# UP minikube 

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
# Lab-002:

1-Create the manifest for Pod:     
kuard-pod.yaml
```
apiVersion: v1
kind: Pod
metadata:
  name: kuard
spec:
  containers:
    - image: gcr.io/kuar-demo/kuard-amd64:blue 
      name: kuard
      ports:
        - containerPort: 8080
          name: http
          protocol: TCP
```
2- UP Pod with manisfest:
```
kubectl apply -f kuard-pod.yaml
```
3-List Pods:
```
kubectl get pods
```
4-Detail about Pods:
```
kubectl describe pods kuard
```
5-Delete Pod:
```
kubectl delete pods/kuard
ou
kubectl delete -f kuard-pod.yaml
```
