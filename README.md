# Ansible
Repo for Projects on Ansible


# 1) Create_EC2_Instance

   This Ansible playbook automates the creation of an Amazon EC2 instance with a public IP address using the amazon.aws.ec2_instance module.
   It allows you to specify instance details dynamically via variables, including instance type, security group, region, and AMI ID.

   📋 Prerequisites
  
    Before running this playbook, ensure the following:

    (i) AWS Credentials
          You must have an AWS account and access keys with permissions to create EC2 instances.

    (ii) Setup EC2 Collection and Authentication
          Install boto3
              pip install boto3
          Install AWS Collection
              ansible-galaxy collection install amazon.aws
          Setup Vault
            Create a password for vault
                openssl rand -base64 2048 > vault.pass
            Add your AWS credentials using the below vault command
                ansible-vault create group_vars/all/pass.yml --vault-password-file vault.pass
