# ansible-common-roles
This repository houses ansible common roles:
- set-port: To set the port for application.
- copy-jar: To copy jar file of the application to artifactory folder.
- docker-image: To build docker image and add to minikube registry.
- cluster-deployment: To create a deployment and service for the image.
- pod-status: Check pod are running or not.


1. Add the kube-config file and certificates in kube_config directory.
2. Add your repo name in the Jenkinsfile.
3. In the artifactory directory jar files are copied through copy-jar role.
4. In the common_templates directory yaml files are created from the templates.

