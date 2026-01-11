Node-Selector is the simplest way to schedule a pod onto specific nodes.
It works by matching pod requirements with node labels.

* The node must have the label.
* The pod must request the label using nodeselector.
Only then pod will be scheduled on that node.