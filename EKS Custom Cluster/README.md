# Before executing
1. Customize your preferences on "terraform.tfvars & variables.tf file" for your EKS Cluster environment.
2. Set kubeconfig path in variable kubeconfig_path on "terraform.tfvars file". After this, run export "KUBE_CONFIG_PATH=" to the destination.
3. Set your AWS Keys in providers.tf file and ".aws/credentils" in your user home.

# Execution
1. Run on terminal: terraform init ; sleep 3 ; terraform plan ; terraform apply
2. The cluster will be accessible as declared in "KUBE_CONFIG_PATH" and you can run kubectl commands.
3. You can change and apply applications to this EKS Cluster.
  

# Destroy
1. Run on terminal: terraform destroy -auto-approve
##### NOTE: If you have issues on destroy the cluster, please check your custom application resources via AWS CLI and/or AWS UI. Some of this files are not managed by terraform.
