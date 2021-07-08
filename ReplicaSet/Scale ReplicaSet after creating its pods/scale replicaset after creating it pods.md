# Kubernetes
## Controllers

##### Scale ReplicaSet after creating its pods.

###### CLI Syntax
```bash
kubectl scale rs <name of the replicaset> --replicas=<your desired replicas pod count>
```

###### Example
```bash
kubectl scale rs replicaset-nginx --replicas=4
```

replicaset = rs <short hand syntax>
From the above command, 
the scale option from above command for scaling and rs means repicaset.And --replicas
is very important thing. here i mentioned its 4. so it will creating 2 new pods as i already have 2 pods existing in this replicaset, so it will create a 2 new pods

###### Why we need Replicas?
For example, think we have a web applications, if the traffic of the applications goes high, pod which are serving this, may be die or something make the pod to die or damage. so, if we want run our pod concurrently to achieve  high availablity, what we have to do? ReplicaSet is the answer.

##### Example
```yaml
kubectl get pods
```
Output would be.
```
NAME                     READY   STATUS              RESTARTS   AGE
replicaset-nginx-622qh   1/1     Running             0          114s
replicaset-nginx-9nfcj   0/1     ContainerCreating   0          4s
replicaset-nginx-bqwpb   0/1     ContainerCreating   0          4s
replicaset-nginx-xrt2n   1/1     Running             0          114s
```

##### ================================================================





