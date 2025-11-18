* Kind is a tool for running local k8s cluster using Docker images ("nodes").
* Kind was primarily designed for testing k8s itself, but can be also used for local dev or cli.

* kind create cluster --image <image_name> --name <cluster_name>
* kind delete cluster <cluster_name>
* kubectl config get-contexts
* kubectl cluster-info --context <context_name>
* kubectl version --client
* kubect get nodes
* kubectl config use-context <context_name>
* kind create cluster --image <image_name> --name <cluster_name> --config config.yaml