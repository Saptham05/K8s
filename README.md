# K8s
What is Kubernetes (K8S)?

K8S is a system for deploying, scaling and managing containerized applications across a cluster of nodes.

The K8S cluster has 2 main components:

Master Node (Control Plane)
Worker Node (Minions)

K8S Architecture Diagram
Now Let’s dive into each of these components.

Master Components
It manages the K8S cluster and performs all administrative tasks.

API Server
It is the front-end of the K8S control plane where all other components interact, to talk with the K8S cluster. It validates and processes the REST requests.

Controller Manager
It continuously watches the shared state of the cluster and makes corrective changes to bring the current state to the desired state.

Examples of controllers:

Replication controller
Namespace controller
Endpoint controller
Service account controller
Scheduler
It is responsible for distributing the workload to available nodes across the cluster, based on resource utilization.

etcd
It is a simple, distributed and consistent key-value store. It stores all the relevant data to manage the cluster.

Few examples of data stored are:

State and details of pods, services.
Data on scheduled, created and deployed jobs.
Details about subnets, configmaps, and secrets.
Worker Components
Physical server or VM that runs applications using pods.

Kubelet
It monitors the API server for pods that are scheduled to the node and start the pod’s container by instructing the container runtime engine, then reports the status of the running containers back to the API server.

Kube Proxy
It makes services available to the external hosts, manages network rules and port forwarding. It also serves as a Network proxy and Load balancer and handles the network routing for TCP and UDP packets.

Container Runtime
It is the underlying software that runs the containers and handles the container’s lifecycle in an isolated but lightweight environment.

Platforms that use containers as a container runtime are:

Docker
Containerd
Cri-o
rktlet
Kubectl
It is the command-line tool to communicate with the API server and send commands to the master node.

Examples of few frequently used commands are:

kubectl apply -f file.yaml   #Create a resource from file
kubectl get pods             #List all pods in the default namespace
kubectl describe svc my_svc  #Describes about the specified service
sqa_619064b7d681b6dc9ed95e055383bd8c4a18f16e

...
squ_b989930248a75606a5c58e6de53e66080f5cadc7
