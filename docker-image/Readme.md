# docker-image role

This role has task to build docker image and add to minikube registry from the provided Dockerfile.
- Set variables in roles.yml file:  
  image_name: Name of the docker image.  
  (By default it is set as '${ORGANIZATION_NAME}-${SERVICE_NAME}:${BUILD_ID}')
