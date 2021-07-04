# cluster-deployment role

This role has task to deploy on cluster reading deployment.yml file from the src provided. 

- Set variables in roles.yml file:  
   kube_config: path to cluster config path.  
   context: context to use while accessing the cluster. 
   
Note: For the ingress service, the host_name should be present in C:\Windows\System32\drivers\etc\hosts file with the cluster ip address.
