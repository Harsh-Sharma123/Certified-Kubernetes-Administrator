Manual Scheduling means assigning a pod to a specific node without using k8s scheduler.
This is done by setting 'nodeName' in the pod spec so that kubectl on that node picks it directly.