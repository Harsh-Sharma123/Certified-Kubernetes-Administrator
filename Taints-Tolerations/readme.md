Taints and Tolerations work together to control which pods are allowed to be scheduled on which nodes.

Taints = applied on nodes -> repel pods
Tolerations = applied on pods -> allow pods to "tolerate" there taints

Taint Effects : 
1. NoSchedule : Pod will not be scheduled on this node unless it has a toleration.
2. PreferNotSchedule: Try to avoid scheduling here, but no guarantee.
3. NotExecute : Existing pods without tolerations are evicted.


To add Taint to a node : 
kubectl taint node <node-name> gpu=true:NoSchedule

To remove Taint from a node :
kubectl taint node <node-name> gpu=true:NoSchedule-