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
 
 
3.To know the detail information of pods

 -> kubectl describe pod <podname>
  
4.to delete perticular pod and then it automatically created

 -> kubectl delete pod <podname>
 
 
 
 




   
