# purplenow
Terraform1
Create an ubuntu empty server
	Install terraform
	Install AWS CLI
Terraform install --> https://askubuntu.com/questions/983351/how-to-install-terraform-in-ubuntu
AWS CLI install-->  https://dev.to/abstractmusa/install-aws-cli-command-line-interface-on-ubuntu-1b50
aws configure
Need to provide AWS access key ID & Secret key 
Create main.tf file
 #List of active iam users.
data "aws_iam_users" "all" {}
output "total_iam_users" {
  value = "data.aws_iam_users.all.users_length" # Will show the number of IAM users
}
 After creating the main.tf file we need to use the commands below
terraform init
terraform plan
terraform apply
After using apply command we can see the IAM users list
If we need to delete the infrastructure, we can use destroy command
Terraform destroy
 
![image](https://github.com/user-attachments/assets/153f3cd1-c7cd-40e9-bf7c-ceb979814d9b)
