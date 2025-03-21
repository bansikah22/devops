The Nautilus DevOps teams is planning to set up a Grafana tool to collect and analyze analytics from some applications. They are planning to deploy it on Kubernetes cluster. Below you can find more details.


1.) Create a deployment named `grafana-deployment-datacenter` using any grafana image for Grafana app. Set other parameters as per your choice.

2.) Create `NodePort` type service with nodePort `32000` to expose the app.

`You need not to make any configuration changes inside the Grafana app once deployed, just make sure you are able to access the Grafana login page.`


`Note`: The `kubectl` on `jump_host` has been configured to work with kubernetes

## Solution
```bash
## apply files
kubectl apply -f grafana-deployment.yaml
kubectl apply -f grafana-service.yaml

## verify
# Check the deployment
kubectl get deployments

# Check the pods
kubectl get pods

# Check the service
kubectl get svc

# Access application
kubectl get nodes -o wide

## defaults
password: admin
username: admin
```