# Snippets

Random Snippets of code and configuration for various tasks, projects, and testing.


## CloudCustodian
* EC2 Tagging Compliance - Contains various policies for the following tasks
  * Tag instaces with key:value that denotes it's managed by CloudCustodian I.E. Custodian:true (Set to RunInstance)
  * Check for compliance on specific tag(s) - If not compliant mark for op - I.E. Stop after 3 days (Set to state:running)
  * Check for remediation of tag(s) - See if tag(s) exist yet - If they do, untag mark (Set to 30 minutes rate)
  * Check marked op tag (default maid_status) - If gte current date, perform op. I.E. Stop. (Set to 1 hour rate)
  * Check EBS Snapshots and propogate tags from parent EBS volume
  * Contains .json policy document to perform the above actions


## TerraForm



## AWS



## Kubernetes
### A dump of random things that will get converting into snippet files later
### Login commands:
#### Google Cloud:
gcloud container clusters get-credentials ${cluster}
#### Microsoft Azure:
az aks get-credentials --resource-group ${RS} --name ${cluster}
#### AWS:
aws eks --region ${region} update-kubeconfig --name ${cluster}

### Starting Nodes on AWS
https://docs.aws.amazon.com/eks/latest/userguide/launch-workers.html

### Useful commands
kubectl get nodes --> Shows nodes, check if nodes are up and registered to the cluster
kubectl get pods (-o wide) --> shows pods, checks status of the pods on the node(s)
kubectl apply -f "service.yml" - Deploy a service to nodes, as pods
kubectl get deploy  - Show the deployment
