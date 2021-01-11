# Kubernetes Components

### Master Components  
  kube-apiserver  
  kube-scheduler  
  kube-controller-manager  
  etcd  

### Node Components  
  Kubelet  
  kube-proxy  


#### Kube-apiserver: 
 It acts as frontend for Kubernetes cluster. users, management devices and command line interfaces interactive API server to talk with Kubernetes cluster. 


#### etcd 
 Etcd is a Consistent and highly-available key value store used as Kubernetes' backing store for all cluster data.  
Kubernetes stores all the date related master, nodes, pods, etc in the etcd. It is distributed across the cluster. 


#### kube-scheduler
  Kube scheduler watches for newly created Pods with no assigned node, and selects a node for them to run on.

#### kube-controller-manager
  It is responsible to identify in case of node or pod failures and replace with new container or pod

Logically, each controller is a separate process, but to reduce complexity, they are all compiled into a single binary and run in a single process.

These controllers include:

`Node controller:` Responsible for noticing and responding when nodes go down.  
`Replication controller:` Responsible for maintaining the correct number of pods for every replication controller object in the system.  
`Endpoints controller:` Populates the Endpoints object (that is, joins Services & Pods).  
`Service Account & Token controllers:` Create default accounts and API access tokens for new namespaces.  


#### Cloud-controller-manager 
  It comes into the picture incase cluster is running in the cloud environment. 


#### kubelet
  An agent that runs on each node in the cluster. It makes sure that containers are running in a Pod.

#### kube-proxy 
  kube-proxy is a network proxy that runs on each node in your cluster, implementing part of the Kubernetes Service concept.  
  kube-proxy maintains network rules on nodes. These network rules allow network communication to your Pods from network sessions inside or outside of your cluster

#### Container runtime 
  it is a underlying software which is used to run our pods 
  
#### what is Kubernetes
  Kubernetes is the Greek word for helmsman or captain of a ship.
  Kubernetes is also referred to as k8s, as there are 8 characters between k and s

  container management (orchestration) tool
  developed by Google lab (& later donated to CNCF)
  open source
  written on Golang
  also called K8s

  #### Container Management / Orchestration tool
  Container Orchestration tool or engine automates deploying, scaling and managing the containerized application on a group of servers
  e.g.
  Kubernetes
  Docker Swarm
  Apache Mesos Marathon

  Docker is a tool designed to make it easier to deploy and run applications by using containers

  Organizations have to use multiple containers to
  Ensure availability
  Load balancing
  Scale-up and down based on user load

  #### Features of Kubernetes
  Docker - creates containers
  Kubernetes - manages containers
  
  Automatic bin packing
  ----------------------
  Automatically places containers based on their resource requirements 
  like CPU & Memory (RAM), 
  while not sacrificing availability
  Saves resources

  Service discover & load balancing
  ---------------------------------
  Kubernetes gives Pods their own IP addresses and a single DNS name for a set of Pods, and can load-balance across them
  With this system, Kubernetes has control over network and communication between pods and can load load balance across them

 Storage Orchestration
 ---------------------------
 Kubernetes allows to mount the storage system of your choice
 Local
 Cloud (AWS)
 Network (NFS)

 Self-healing
 --------------
 If a container fails - restarts container
 If node dies - replaces and reschedule containers on other nodes
 If container does not respond to user defined health check - kills container
 This is taken care by Kubernetes  ReplicationController
 
 Secret & configuration management
 ---------------------------------
 Kubernetes manages secrets and configuration details for an application separately from the container image,
 Deploy and update secrets and application configuration without rebuilding your image and without exposing secrets in your stack configuration.

 Automated rollouts and rollbacks
 ---------------------------------
 Rollout: deploy changes to the application or its configuration
 Rollback: revert the changes & restore to the previous state
 Kubernetes ensures there is no downtime during this process

 Batch execution
 ----------------
 Kubernetes supports batch execution, long-running jobs, and replaces failed containers

 Horizontal scaling
 ------------------
 In Kubernetes, we can scale up or down the containers 
 - using commands
 - from the dashboard (kubernetes ui)
 - automatically based on CPU usage
  
  
  
  
  
 
