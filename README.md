# CSYE6225-Cloud Computing Assignment 3 </br>

<h2>AWS Infrastructure Setup using Terraform</h2>
Prerequisites
Before you can create the infrastructure using Terraform, you need to have the following:

An AWS account with administrative privileges
Terraform installed on your local machine
AWS CLI installed on your local machine 
AWS IAM user with necessary permissions and access keys

Steps to Setup Infrastructure
1. Clone the repository to your local machine
git clone git@github.com:Trisha-s-CloudOrganization/aws-infra.git

2. Navigate to the cloned directory
cd terraform/environment/dev or cd terraform/environment/demo

3. Format and Initialize Terraform
terraform fmt && terraform init

Note: rename *.tfvars.* to *.tfvars as required

4. Create a terraform.tfvars file with your AWS access and secret keys if aws user credentials are not saved:
access_key = "your_aws_access_key"
secret_key = "your_aws_secret_key"

5. Plan the infrastructure to see what changes Terraform will make:
terraform plan

6. Apply the infrastructure to create the resources:
terraform apply

7. Verify that the infrastructure was created successfully e.g. if ec2 created:
aws ec2 describe-instances

This command should return information about the EC2 instance that Terraform created.

8. Destroy the infrastructure when it is no longer needed:
terraform destroy

cmd to execute in Mac M1 processor (before terraform init):
git clone https://github.com/hashicorp/terraform-provider-template
cd terraform-provider-template
go build
mkdir -p ~/.terraform.d/plugins/registry.terraform.io/hashicorp/template/2.2.0/darwin_arm64
mv terraform-provider-template ~/.terraform.d/plugins/registry.terraform.io/hashicorp/template/2.2.0/darwin_arm64/terraform-provider-template_v2.2.0_x5
chmod +x ~/.terraform.d/plugins/registry.terraform.io/hashicorp/template/2.2.0/darwin_arm64/terraform-provider-template_v2.2.0_x5


Useful Links: </br>
AWS CLI install and configuration: https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html </br>
Terraform: https://www.terraform.io/ </br>
Guideline to build terraform infrastructure: https://developer.hashicorp.com/terraform/tutorials/aws-get-started/aws-build </br></br>
Usefull cmd:</br>
terraform init</br>
terraform fmt</br>
terraform plan</br>
terraform apply</br>
terraform destroy</br>
