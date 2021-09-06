# AWS Virtual Private Cloud (VPC) & CIDR Blocks

![iamge](./img/AWS_deployment_networking_security.PNG)

---
#### What is a VPC?
AWS isolated virtual network - It allows us to control virtual network environment including selection of your own IPs address range, we can create multiple subnets within one VPC with specific network configuration. We can use both IPv4 & IPv6 for most resources, it provdes security for your services or instances.

## Internet Gateway
#### What is an Internet Gateway?
An Internet Gateway can transfer communications between an enterprise network and the internet. It allows internet access into the VPC.

**Write own defintition here**

## Subnets
#### What is a Subnet?
A Subnet is a segmented piece of a larger network - the goal of the subnet is to split a large network into a group of smaller, inter-connected networks to help minimise traffic - or navigate traffic securely.

**Write own defintition here**

## Route Tables
#### What is a Route Table (RT)?
RT contains a set of rules, called routes, that are used to determine where the network traffic from your subnet or gateway is directed.

**Write own defintition here**

## Network Access Control List (NACL)
#### What is a Network Access Control List (NACL)?
NACL's are stateless - we have to explicility allow inbound **AND** outbound rules. They are an added layer of security at the subnet level.

**Write own defintition here**

## Security Groups

---

## Networking Task
*4.3 Billion IP addresses in the world (approx.)*
- Step 1: create a VPC with IPV *valid* CIDR block
    
    `10.0.0.0/16`  ->  `10.101.0.0/16`  ->  `10.102.0.0/16`

- Step 2: Create internet gateway (IG)

    Step 2.1: Attach the IG to your VPC

- Step 3: Create route tables

    Step 3.1: Edit route and insert your IG in `target`

- Step 4: Create public subnet

    `10.0.1.0/24` *(Choose according to your VPC IP range)*

    Step 4.1: Associate public subnet with our RT

- Step 5: Create public NACLs

    Set inbound and outbound rules for this

- Step 6: Create a Security Group for our app
