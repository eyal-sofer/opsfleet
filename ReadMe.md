read me file for first task - automate eks cluster creation with terrafrom

There is one tf file in the repo - eks.tf
Run this file to create an eks cluster in your aws account (which associated with your terrafrom).
You can customize the resources (number of nodes, type of ec2, eks cluster name) in the eks.tf file.

After craeting the cluster, you can configure access for kubectl using the AWS CLI :

aws eks update-kubeconfig --name my-eks-cluster

# Make sure you switch to the new context:
kubectl config use-context 

# Test it out, this should show the nodes we configured:
kubectl get nodes

running a pod in the cluster:
after you set up an access with kubctl, you can deploy pods in the cluster by creating and running a yaml file of the 
resource you would like (pod/deployment/RS/DS and etc')
