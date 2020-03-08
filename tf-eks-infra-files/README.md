# Setting up AWS EKS infra using Terraform

# Commands to run 

## Terraform apply
$> terraform init
$> terraform apply


## Configure kubectl
$> terraform output kubeconfig # save output in ~/.kube/config


## Configure config-map-auth-aws

$> terraform output config-map-aws-auth # save output in config-map-aws-auth.yaml
$> kubectl apply -f config-map-aws-auth.yaml


## See nodes coming up

$> kubectl get nodes


## Destroy
#Make sure all the resources created by Kubernetes are removed (LoadBalancers, Security groups)

$> terraform destroy

