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
git clone https://github.com/your-username/aws-terraform-infrastructure.git

2. Navigate to the cloned directory
cd aws-terraform-infrastructure

3. Initialize Terraform
terraform init

4. Create a terraform.tfvars file with your AWS access and secret keys:
access_key = "your_aws_access_key"
secret_key = "your_aws_secret_key"

5. Plan the infrastructure to see what changes Terraform will make:
terraform plan

6. Apply the infrastructure to create the resources:
terraform apply

7. Verify that the infrastructure was created successfully:
aws ec2 describe-instances

This command should return information about the EC2 instance that Terraform created.

8. Destroy the infrastructure when it is no longer needed:
terraform destroy

Useful Links: </br>
AWS CLI install and configuration: https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html </br>
Terraform: https://www.terraform.io/ </br>
Guideline to build terraform infrastructure: https://developer.hashicorp.com/terraform/tutorials/aws-get-started/aws-build </br>
