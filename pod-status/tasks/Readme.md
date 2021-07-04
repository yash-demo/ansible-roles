# pod-status role

This role has 3 tasks:  
1. Wait until the pods are Running.
2. Check for failed pods.
3. Print failed pod_list.
The tasks search for the pods in the mentioned namespace having given labels.  
- Set variables in roles.yml file:  
   kube_config: path to cluster config path.  
   context: context to use while accessing the cluster.  
   label: label of the object to search for.  
   namespace: Namespace in which to search for.
