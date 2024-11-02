# Kubernetes Operator

## Build
```
docker build -t staticpage-controller .
# the following commands can be replaced with (if your docker build is compatible with minikube): minikube image load staticpage-controller
docker image save -o staticpage-controller.tar staticpage-controller
minikube image load staticpage-controller.tar
rm staticpage-controller.tar 
```

## Deploy

```
kubectl apply -f example/crd.yaml # CRDs
kubectl apply -f example/deploy-controller.yaml # deploy the staticpage-controller (and roles)
kubectl apply -f example/mydep.yaml # staticpage example

```