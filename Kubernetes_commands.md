# Common kubernetes Commands

Deploying Nginx container on Kubernetes
-----------------------------------------
1.Deploying Nginx Container

  -> kubectl run sample-nginx --image=nginx --replicas=2 --port=80
  -> kubectl get pods
  -> kubectl get deployments
  
2.Expose the deployment as service. This will create an ELB in front of those 2 containers and allow us to publicly access them:

 -> kubectl expose deployment sample-nginx --port=80 --type=LoadBalancer
 -> kubectl get services -o wide
 
3.To delete cluster

 -> kops delete cluster dev.k8s.valaxy.in --yes
 
 
 
 
Deploying Nginx container on Kubernetes
Deploying Nginx Container

  kubectl run sample-nginx --image=nginx --replicas=2 --port=80
  kubectl get pods
  kubectl get deployments
Expose the deployment as service. This will create an ELB in front of those 2 containers and allow us to publicly access them:

 kubectl expose deployment sample-nginx --port=80 --type=LoadBalancer
 kubectl get services -o wide
To delete cluster

 kops delete cluster dev.k8s.valaxy.in --yes



   
