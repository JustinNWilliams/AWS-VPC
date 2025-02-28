# Building a Virtual Private Cloud (VPC) with AWS
---
## Overview
This guide will walk you through creating an Amazon Virtual Private Cloud (VPC) in AWS, a foundational step in building secure, isolated cloud environments for your applications. We'll cover subnets, internet gateways, and using the AWS CLI for automation.

![image](https://github.com/user-attachments/assets/32d9151a-e5ba-41b0-9856-76fb3db923b7)

---

## In This Project, We Will Be Using:

- **AWS Management Console**: For creating and managing VPCs, subnets, and internet gateways.  
- **AWS CLI (Command Line Interface)**: To automate the provisioning of VPC resources using commands.  
- **Key AWS Services**:
  - **Amazon VPC**: For creating a secure and isolated network.
  - **Subnets**: To divide the VPC into smaller segments.
  - **Internet Gateway**: To allow public access to resources.
- **A Basic Understanding of Networking**: Knowledge of CIDR blocks, IP ranges, and public vs private subnets.

---

## What is Amazon VPC?

**Amazon VPC (Virtual Private Cloud)** is a service that enables you to create isolated networks for your AWS resources, such as EC2 instances and databases. These networks provide granular control over traffic, security, and connectivity.

---

## Setting Up Your VPC

1. **Define an IPv4 CIDR Block**  
   A CIDR block assigns a range of IP addresses to your VPC. For example, `10.0.0.0/16` gives a range of 65,536 addresses.

   - Navigate to the AWS Management Console.  
   - Go to **VPC Dashboard** > **Create VPC**.  
   - Enter your desired CIDR block.  

![Screenshot 2025-02-27 231915](https://github.com/user-attachments/assets/95d1606b-d535-4f72-9d17-b6afe3fd23fd)

2. **Default VPC**  
   AWS accounts come with a default VPC. This ensures services like EC2 and databases have a network to connect with.

---

## Creating Subnets

Subnets divide your VPC into smaller, more manageable segments. These can be public (connected to the internet) or private (internal-only).

1. **Steps to Create a Subnet**
   - Go to **VPC Dashboard** > **Subnets** > **Create Subnet**.  
   - Assign a name and choose an availability zone.  
   - Enable **Auto-assign public IPv4 addresses** to allow internet access.  

![Screenshot 2025-02-27 232333](https://github.com/user-attachments/assets/93379694-24d3-4d3a-af2b-f0977cc44b13)

2. **Public vs. Private Subnets**  
   - **Public Subnet**: Must have a connection to the Internet Gateway.  
   - **Private Subnet**: No internet connection, used for internal communication.  

![Screenshot 2025-02-27 232522](https://github.com/user-attachments/assets/6072fa84-0abc-4c09-8a63-25ffe8b83bbd)

---

## Attaching an Internet Gateway

An **Internet Gateway** connects your VPC to the internet, allowing external access to resources.

1. **Steps to Attach an Internet Gateway**
   - Go to **VPC Dashboard** > **Internet Gateways** > **Create Internet Gateway**.  
   - Attach it to your VPC.  

![Screenshot 2025-02-27 232914](https://github.com/user-attachments/assets/216a8ffd-d877-451e-84d3-cb9efdc84bfc)

2. Without an Internet Gateway, your VPC will not have external connectivity. This step is crucial for making applications accessible to users.

---

## Using the AWS CLI for Automation

For faster and more efficient management, you can use the AWS CLI (Command Line Interface) to automate tasks.

1. **Create a Subnet**
   ```bash
   aws ec2 create-subnet --vpc-id [VPC_ID] --cidr-block [CIDR_BLOCK]
   ```

![Screenshot 2025-02-27 234307](https://github.com/user-attachments/assets/211bc2e5-87fb-454b-9c6a-aea797805ff4)

2. **Advantages of AWS CLI**
   - Faster automation for repetitive tasks.  
   - Ideal for scripting and large-scale operations.

---

## Conclusion

This project demonstrates how to create and manage a Virtual Private Cloud (VPC) in AWS, including subnets, internet gateways, and automation with AWS CLI. With these skills, you can build secure cloud infrastructures to host your applications.
