Pod : smallest deployable unit in k8s

Two ways to create a pod in k8s : 
    * imperative (using commands)
        kubectl run <pod_name> --image=<image:latest>
    * declarative (using yaml file)

Some more commands : 

kubectl explain pod
kubectl get pods
kubectl describe pod <pod_name>
kubectl edit pod <pod_name>
kubectl exec -it <pod_name> -- sh
kubectl run <pod_name> --image=<image:latest> --dry-run=client -o yaml > <file_name>.yaml
kubectl run <pod_name> --image=<image:latest> --dry-run=client -o json > <file_name>.json
kubectl get pods <pod_name> --show-labels
kubectl get pods -o wide
kubectl get nodes -o wide