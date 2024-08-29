## Terraform introduction:
 Terraform is an infrastructure as a code {Iac} tool, it is cloud-agnostic and allows a single configuration. it also used to manage multiple providers and handle cross-cloud dependencies.

### Terraform files uses the extension .tf

## Terraform Commands:
  1. terraform init: initializes a terraform dir and download providers plugins
  2. terraform validate: To make sure that terraform scripts are correct
  3. terraform plan: It gives a detailed execution plan by terraform
  4. terraform apply --auto-approve:  (creates the infrastructure with non-interactive session)
  5. terraform destroy --auto-approve: (To destroy the infrastructure with non-interactive session)
  6. terraform fmt: to check the format of terraform file written.
  7. terraform import:  to import a resources not created by terraform into terraform to manage it, Which would be found in the terraform state file
  8. terraform.tfstate: It records all infrastructure created in the console
  9. terraform show: to display all the resources under the mgt of terraform and many more.

## Terraform Installation:
### Note: ON UBUNTU SERVER

a. Install Terraform CLI
b. Install AWS CLI
c. Install VS Code Editor - recommended for this course
d. Install HashiCorp Terraform plugin for VS Code - recommended  

```
sudo adduser terraform
sudo echo "terraform  ALL=(ALL) NOPASSWD:ALL" | sudo tee /etc/sudoers.d/terraform
sudo su - terraform
```

1. Update apt repo
```
sudo apt-get update -y
```

3. Amazon CLI Installation:
```
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install
```

4. Terraform CLI Installation:
```
wget -O- https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update && sudo apt install terraform
```

5. Add a role to the server you are using to access EKS worker nodes. (Administrative Access)
   - And configure access & secret access keys for the server to ensure interaction with AWS API

### For Window Server: 10
1. install aws cli using AWS Docs
2. Configure aws cli using (aws configure)
3. Install terraform for windows from terraform docs


