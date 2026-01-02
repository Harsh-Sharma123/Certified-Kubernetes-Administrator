Pods in K8s that runs more than one container inside the same pod environment.
All containers in that pod share: 
- network namespace
- lifecycle (scheduled and started together)
- storage volume

We generally use this when two or more containers works closely together.

* Common Scenarios : 
- Sidecar Pattern : A helper container runs alongside main application container.
    ex., logs collector, etc.
- Ambassador Pattern : A helper container acts as proxy to external services.
    ex., a proxy container that routes traffic from main app to an external db or api.
- Adapter Pattern : A container converts or normalises o/p from main app.
    ex., format converter, etc.