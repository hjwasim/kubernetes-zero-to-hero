# Kubernetes
## Annotations and Labels

##### Lables
Labels are used to identify/select the pods which are in the kubernetes cluster. it also used to identify the pods in the K8s services.

###### Syntax
```yaml
metadata:
  labels:
     key1: value1
```
###### To list a pod using Label Selectors.


```sh
kubectl get pods -l app=nginx
```
above command gives the output of all pods which contains the label app:nginx

where -l is to represent the label selections and preceding app=nginx is the key/value which we added in the config file in the metadata.labels.

```sh
kubectl get pods -l app!=nginx
```
above command gives the output of all pods which doesnt contains the label app:nginx


##### Annotations
Annotations are used to provide information about the pods which are in the kubernetes cluster. for ex, it used to provide timestamps, information about client libraries or tools and even more.

###### Syntax
```yaml
metadata:
  annotations:
    key: value
```
##### ==============================================================================





