# Kubernetes
## Services

##### ClusterIP

###### Apply the configurations
```sh
kubectl apply -f nginx-deployment.yaml
kubectl apply -f nginx-service-clusterip.yaml
```
###### Output
```sh
deployment.apps/nginx-deployment created
service/nginx-service-clusterip created
```
###### Check it is correctly applied.
```sh
kubectl get deploy nginx-deployment
kubectl get svc nginx-service-clusterip
```
###### Note the ClusterIp addess of the nginx-service-clusterip service. To make sure it is working or not.
```sh
minikube ssh
```
```sh
curl <IP of nginx-service-clusterip svc>
```
###### Output
```html
<!DOCTYPE html>
<html>
<head>
<title>Welcome to nginx!</title>
<style>
    body {
        width: 35em;
        margin: 0 auto;
        font-family: Tahoma, Verdana, Arial, sans-serif;
    }
</style>
</head>
<body>
<h1>Welcome to nginx!</h1>
<p>If you see this page, the nginx web server is successfully installed and
working. Further configuration is required.</p>

<p>For online documentation and support please refer to
<a href="http://nginx.org/">nginx.org</a>.<br/>
Commercial support is available at
<a href="http://nginx.com/">nginx.com</a>.</p>

<p><em>Thank you for using nginx.</em></p>
</body>
</html>
```
##### ================================================================





