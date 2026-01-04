DaemonSet is a K8s controller that makes sure a copy of a specific pod is running on all nodes or some nodes (based on node selectors, taint/tolerations, affinity).

Ideal for node-level services :
-> Log Collector
-> Monitoring Agents (prometheus, grafana)
-> Storage Daemon
-> Network Plugin
-> Security Agents