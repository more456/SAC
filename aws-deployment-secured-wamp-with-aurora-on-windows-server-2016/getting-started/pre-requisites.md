# Pre-Requisites

**Pre-Requisites:**

Basic knowledge of below AWS components if required:

1. [AWS account](https://aws.amazon.com/account/)
2. [Cloud Formation Template](https://aws.amazon.com/cloudformation/resources/templates/)
3. [EC2](https://aws.amazon.com/ec2/?ec2-whats-new.sort-by=item.additionalFields.postDateTime\&ec2-whats-new.sort-order=desc) - Windows Operating System
4. [RDS](https://aws.amazon.com/rds/) - Aurora MySQL

**IAM Roles:**

Below IAM Roles will be created by the Cloud Formation Template:

1. IAMForEC2 : This role is required for creation of EC2 Instance and Network elements - Principal of ec2.amazonaws.com
2. IAMRoleForStackCreation: This role is required for creation of Cloud Formation components&#x20;

These IAM roles are required for creation of resources mentioned in this [link](../introduction/resources.md)

