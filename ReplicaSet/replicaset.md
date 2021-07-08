# Kubernetes
## Controllers

##### ReplicaSet Controller

###### ReplicaSet?
ReplicaSet is a like controller and its process to scale our pods to match our desired state or in other words its ensure the pod to run seamlessly with zero downtime. bascically it's cloning into two or more!

###### Why we need Replicas?
For example, think we have a web applications, if the traffic of the applications goes high, pod which are serving this, may be die or something make the pod to die or damage. so, if we want run our pod concurrently to achieve  high availablity, what we have to do? ReplicaSet is the answer.

##### Example
```yaml
apiVersion: apps/v1
kind: ReplicaSet
.....
spec:
  replicas: 2
  selector:
    matchLabels:
      environment: production
  template:
    metadata:
      labels:
        environment: production
    spec:
      containers:
        - name: nginx-container
          image: nginx
```


The above manifest split into apiVersion,kind,spec: replicas,template,selector.

###### apiVersion
The apiVersion of ReplicaSet is apps/v1.

###### kind
The type of Object we have to configure this time is ReplicaSet controller. so, ReplicaSet - mentioned.

###### replicas
- The replicas field under spec specifies means - How many Pods the ReplicaSet should keep running concurrently. here its : 2
- if nothing is mentioned - default as 1.

###### template
- The template field under spec specifies the template of the pod we want to run using this ReplicaSet.
- The ReplicaSet will use this Pod template to create new Pods whenever there is a need for them.
- It same as the Pod template.
-  Here we have also specify Labels and Annotations.
```yaml
   metadata:
      labels:
        environment: production
    spec:
      containers:
        - name: nginx-container
          image: nginx
```
###### selector
It is important thing. selector field under spec specify the labels of the pods, which the replicaSet want to manage. In the above example,
we mentioned -- "environment: production". Here the replicaSet will manage the pods which containing this labels.

##### ================================================================





