# Terraform1
How to launch an EC2 instance using Terraform With Terraform, developers can lean on familiar coding practices to provision the underlying resources for their applications. Follow these steps to use the IaC tool to create an Amazon EC2 instance.


To launch an EC2 instance using Terraform, follow these steps:

1-Install Terraform on your local machine and configure the AWS CLI to use your AWS credentials.

2-Create a Terraform configuration file, usually with a ".tf" extension, to define the resources you want to create.

3-In the Terraform configuration file, specify the AWS provider and the desired region to use.

4-Define the EC2 instance resource in Terraform, including the instance type, AMI ID, security group, and key pair.

5-Use Terraform's "apply" command to launch the EC2 instance in AWS. Terraform will communicate with the AWS API to provision the specified resources.

6-After the EC2 instance is launched, you can use Terraform to manage changes to the instance and its associated resources.

**Here is a sample Terraform configuration to launch an EC2 instance:

provider "aws" {
  region = "us-west-2"
}

resource "aws_instance" "example" {
  ami           = "ami-0c55b159cbfafe1f0"
  instance_type = "t2.micro"

  tags = {
    Name = "example-instance"
  }
}



--------------


This is a basic example, and you can add additional resources or configuration options as needed.
