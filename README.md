# bespin-debug
Helm chart that creates a service for debugging a bespin job
Deploys a pod that mounts existing persistent volume claims from a bespin job. 

__Creates__
- Deployment to run jupyter lab
- Service/Ingress to allow a user to access the pod created by the deployment

## Required values:
- job_id - id of bespin job we are debugging
- ingress.host - host to use for access to the jupyter lab instance
- volumes.output_data_pvc_name - name of the PVC that contains output data
- volumes.job_data_pvc_name - name of the PVC that contains job input data
- volumes.system_data_pvc_name - name of the PVC that contains system data

## Optional values:
- notebook_token - token used to secure notebook
- notebook_password - password used to secure notebook
