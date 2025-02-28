<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Build a Virtual Private Cloud

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-vpc)

**Author:** Justin Williams  
**Email:** eiujustin4@gmail.com

---

## Build a Virtual Private Cloud (VPC)

![Image](http://learn.nextwork.org/lighthearted_beige_zany_bison/uploads/aws-networks-vpc_2facf927)

---

## Introducing Today's Project!

### What is Amazon VPC?

Amazon VPC stands for Amazon Virtal Private Cloud, this is very useful for giving resources access to the internet.

### How I used Amazon VPC in this project

We used VPC in this project to create subnets, internet gateways, and utilized it in AWS CloudShell

### One thing I didn't expect in this project was...

-----

### This project took me...

-------

---

## Virtual Private Clouds (VPCs)

VPC stand for Virtual Private Cloud. This is used to create subnets, traffic rules, and security measures to control how resources, like EC2 instances and databases, connect and work together.

There was already a default VPN in my account ever since my AWS account was created. This is because EC2 instances and Databases require an VPC in order to be setup. The reasoning behind this is because certain services need a secure, isolated network to connect with each other and run securely.

To set up my VPC, I had to define an IPv4 CIDR block, which is a way to assign a whole block of IP addresses.

![Image](http://learn.nextwork.org/lighthearted_beige_zany_bison/uploads/aws-networks-vpc_2facf927)

---

## Subnets

Subnets are used to group resources with similar access rules and restrictions. There are already subnets existing in my account, one for every availablity zone.

Once I Created my subnet I enabled auto-assign public IPv4 Address. This setting makes sure that internal communication within my VPC is allowed. So that It can access the internet.

The difference between public and private subnets are that public subnets are connected to the internet and private subnets are not. In order for a subnet to be considered public it has to have a valid connection to the internet gateway.

![Image](http://learn.nextwork.org/lighthearted_beige_zany_bison/uploads/aws-networks-vpc_157c4219)

---

## Internet gateways

Internet gateways are key to making applications available on the internet. This allows things to be accessible to external users.

Attaching an internet gateway to a VPC means that I am giving access to the resources in my VPC to the internet now. If I missed this step then I would have no internet connection.

![Image](http://learn.nextwork.org/lighthearted_beige_zany_bison/uploads/aws-networks-vpc_4ae90410)

---

## Using the AWS CLI

VPC resources can also be created with Cloud shell which is AWS CLI. CLI stands for command line interface, it is where engineers use the terminal to automate tasks using scripts, making the CLI essential for managing your cloud environment in an efficient way. 

To set up a VPC or a subnet u can used the command aws ec2 create-subnet --vpc-id [ID] but make sure to avoid errors by include the cidr block

Compared to using the AWS Console, an advantage of using commands is speed, an advantage of using the console is presicion and visually seeing what your doing. Overall I prefer to use the console due to my heavy Linux background and how quick it is to set up.

![Image](http://learn.nextwork.org/lighthearted_beige_zany_bison/uploads/aws-networks-vpc_9b2465411)

---

---
