# Kubernetes
## Services

##### ClusterIP
ClusterIP is used to expose the Service on a certain IP address inside the 
cluster. This is the default type of Service. It is a good type of Service to use for communication between different types of Pods inside the k8s cluster.

###### Syntax - configiuration
```yaml
kind: Service
........
spec:
 type: ClusterIP
 ports:
   - targetPort: 80
     port: 80
```

We can also specify the custom IP address for clusterIP service, but it has one constraint. we cannot arbitarily set random IP address. 
Before assigning IP address make sure that the IP address ranges from
#####            	10.96.0.0 to 10.111.255.255

##### ================================================================





