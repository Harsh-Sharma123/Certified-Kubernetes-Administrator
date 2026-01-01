Namespaces are ways to organise and isolate resources within a cluster.
They act like virtual cluster inside a single physical cluster.
Namespaces provides :
    * Logical isolation of resources
    * Scoping of names of objects
    * Resources quota boundaries
    * RBAC Separation (permissions per namespace)
To access services from one namespace to another, we use : 
    FQDN (Fully Qualified Domain Name)
    curl <service-name>.<namespace>.svc.cluster.local