# Ansible Playbook to Create an EC2 Instance and Open Ports 22 and HTTP

This Ansible playbook can be used to create an EC2 instance of type t2.micro in the us-east-1 region, open ports 22 and HTTP, install Apache2, and start the service.
Prerequisites

Before running this playbook, you will need:

    An AWS account
    AWS credentials with the necessary permissions to launch an EC2 instance, create a security group, and modify security group rules
    Python 2.6 or later or Python 3.5 or later installed on the local machine
    The boto and boto3 Python packages installed on the local machine

 ## Usage

To use this playbook:

    Clone the repository to your local machine.
    Edit the vars section of the playbook with your desired values for the following variables:
        region: The AWS region where the instance will be launched.
        image: The ID of the Amazon Machine Image (AMI) to use for the instance.
        instance_type: The type of instance to launch (e.g., t2.micro).
        security_group: The name of the security group to create and use for the instance.
    Ensure that you have an SSH key pair named my-key in the AWS region where you will be launching the instance. You can create a new key pair in the AWS Console if necessary.
    Run the playbook with the following command:


ansible-playbook create-ec2-instance.yml

This will create a new EC2 instance, install Apache2, and start the service. Note that the playbook will prompt you for your AWS access key and secret key when it runs.
### License

This playbook is released under the MIT License. See the LICENSE file for more information.
