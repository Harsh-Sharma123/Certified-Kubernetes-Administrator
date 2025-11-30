Kubernetes resource that manages lifecyle of PODs - it ensures that a number of pod instances are always up and running.
If a Pod fails or gets deleted, or become unresponsive, the RC automatically creates a new one to replace it.

# Key Features : 
* Maintain Desired State
* Self-Healing
* Scaling
* Rolling Updates

# Commands : 
* kubectl explain rc
* kubectl get rc