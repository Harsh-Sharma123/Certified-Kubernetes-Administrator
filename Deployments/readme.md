Deployments are high-level k8s controllers that manages ReplicaSets (and therefore Pods) in a declarative way.

It ensures your application is running in a desired state - correct number of pods, correct version of containers and smooth updates and rollbacks.

A Deployment:
    - can create and manage ReplicaSets automatically.
    - ensures number of pods are always running.
    - supports rolling updates, rollback and scaling.
    - makes application management reliable and unpredictable.

Key Features:
* Declarative Updates : You specify desired state (image, replicas, etc) & k8s handles changes automatically.
* Rolling Updates : Deploy new versions without downtime.
* Rollbacks : Easily revert to previous working version easiy.
* Scaling : Change replicas to scale pods up or down.
* Self-Healing : Automatically replace failed pods.

-- To set image version in Deployment : 
kubectl set image deploy/<deployment-name> <container-name>=<new-image-name>:<new-image-version>
ex., kubectl set image deploy/nginx-deploy nginx-container=nginx:1.9.1

-- To check rollback history :
kubectl rollout history deploy/<deployment-name>

-- To check rollback status :
kubectl rollout status deploy/<deployment-name>

-- To roolback recent changes : 
kubectl rollout undo deploy/<deployment-name>