## Basic Kubernetes commands

To look at the Operating System.
```
kubectl get nodes -o wide
```
to create a new pod with the nginx image.
```
kubectl run nginx --image=nginx
```
to look at the pods in detail
```
kubectl describe pod <podid>
```
To create a pod defination YAML file or create a mainfest file:-  
```
kubectl run redis --image=redis123 --dry-run=client -o yaml > redis-definition.yaml
```
to create a resource from the manifest file  
```
kubectl create -f redis-definition.yaml
```
to scale replicaset using command
```
kubectl scale rs new-replica-set --replicas=2
```
 to get all the information of all the pods or replicaset
 ```
 kubectl get all
 ```

 

