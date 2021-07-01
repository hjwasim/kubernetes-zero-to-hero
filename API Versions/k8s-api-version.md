# Kubernetes
## API Versions

In kubernetes, there is a lot of api resources and version and it supports multiple versions of same resource type.
Each one has a different API path, such as
- /api/v1
- /apis/ 
- extensions/v1beta1

###### The different API versions are below:
- alpha [when the resource type which are in developing mode or partially complete & not for production grade]
- beta [when the resource type which are in testing mode or fully complete, is mainly         for testing. not for production grade]
- stable [when the resource type is fully supports and it is good to use in the production grade.]

#### For example.
Autoscaling have multiple versions which are v1beta1, v1beta2, and v1.
Each version have different purposes.

To get all API Resources,
```sh
kubectl api-resources
```

To get API Resources with respect to the API Groups,
```sh
kubectl api-resources --api-group= <name of an api group>
```