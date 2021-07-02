# create-deploymentfile role

This role has task to create a deployment.yml file for cluster deployment from the generic_template.   
- Set variables in roles.yml file:  
   kube_config: path to cluster config path.  
   context: context to use while accessing the cluster.  
   image_name: Name of the image used for deployment.  
   replicas: no. of replicas/copy of your pod.  
   port: port no. for the service within the cluster.  
   NodePort: NodePort no. for the service to expose outside the cluster.  
   label: label for objects to create.  
   namespace: Namespace in which to deploy in cluster.  
   deployment_name:  Deployment name.  
   container_name:  Container name.  
   service_name: Service name.  
   ingress_name: ingress name.  
   host_name: Host name by which you can access the service from browser.  


Note: For the ingress service, the host_name should be present in C:\Windows\System32\drivers\etc\hosts file with the cluster ip address.
