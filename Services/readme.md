In K8s, Service is an abstraction that defines a stable, reliable network endpoint for accessing one or more pods.
Since pods are ephemeral and can be recreated, their IPs can change frequently.
A service provides consistent way to reach them.

# Types of Services : 

1. NodePort
* Expose the service on a static port on each node
* External Traffic -> <Node-IP>:<NodePort> -> Service -> Pod
* Typically used for simple external access or dev/test.
* Port between 30000 to 32767

2. ClusterIP
* Internal-use only, access within the cluster
* use when :
    - microservices talks to each other
    - Internal APIs
    - Database inside cluster
* By default, Services are ClusterIP only.

3. LoadBalancer
* Automatically creates a cloud provider load balancer.
* use when :
    - you want a public endpoint
    - you're running on managed k8s (AWS/GCP)

4. ExternalName
* maps a service to an external DNS name
* use when :
    - Accessing external service through k8s DNS