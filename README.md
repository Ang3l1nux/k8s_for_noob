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
# Lab-002:
1-Criar o manifesto de Pod:     
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
2-Executar o Pod a partir do manisfesto:
```
kubectl apply -f kuard-pod.yaml
```
3-Listar os Pods:
```
kubectl get pods
```
4-Detalhes sobre os Pods:
```
kubectl describe pods kuard
```
5-Removendo um Pod:
```
kubectl delete pods/kuard
ou
kubectl delete -f kuard-pod.yaml
```
