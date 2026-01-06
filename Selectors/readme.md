Selectors are queries used to filter or match k8s objects based on their labels.
* K8s uses selectors to decide which resources a service, deployment or replicaset should manage.

Types : 
1. Equality-Based Selector :
    selector:
        matchLabels:
            app: frontend
            env: production
2. Set-Based Selector: 
    selector:
        matchExpressions:
        - key: app
          operator: In
          values:
          - frontend
          - backend
        - key: env
          operator: NotIn
          values:
          - dev