Kubernetes resource that ensures that a specified number of identical pods are running at any given time - it's next generation replacement of older ReplicationController.

Selector-based Management : Manages pods based on label selectors.

This is internally used by Deployments.

* To update the count of replicas:
1. One way is to update rc.yaml/rs.yaml, save it and re-apply it using kubectl apply -f <file-name>
2. Second way is to :
    kubectl edit rs/<replica-set-name>
3. Third way is to use commands to scale replicas:
    kubectl scale --replicas=10 rs/<replica-set-name>