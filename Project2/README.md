(Part 1 - Build a VPC)
Step 1: Creating VPC

The created VPC is named BRADLEY-VPC. This VPC will create a virtual private network with 10.0.0.0/24 in CIDR block formatting,
which implements a range of IP addresses that will be used and associated with in the private network. 

(Picture shown in "Images" directory in github. Picture Name: VPC Creation) 
-----------------------------------------------------------------------------------------------------------------------------------------
Step 2: Creating Subnet

I created a subnet named BRADLEY-Subnet. I had to connect this subnet to my BRADLEY-VPC. The subnet with a private /24 private IP
range. This will allow a broad spectrum of 10.0.0.0/24 private IP addresses to be used inside of the VPC.

(Picture shown in "Images" directory in github. Picture Name: Subnet Creation) 
-----------------------------------------------------------------------------------------------------------------------------------------
Step 3: Creating an internet gateway

I created an internet gateway named BRADLEY-gw, then attached my VPC. This gateway basically gives your vpc internet communication!

(Picture shown in "Images" directory in github. Picture Name: Internet Gateway)
-----------------------------------------------------------------------------------------------------------------------------------------
Step 4: Creating Route Table

I named my route table BRADLEY-routetable. I attached this to my subnet and VPC. Then created 0.0.0.0/0 destination and my BRADLEY-gw 
gateway target. This will send all trafic to gateway giving internet connection!

(Picture shown in "Images" directory in github. Picture Name: Route Table)
-----------------------------------------------------------------------------------------------------------------------------------------
Step 5: Creating Security Group

I created a security group that it attached to my BRADLEY-VPC. I created 2 inbound rules, which gives my AWS and wright state IP 
addresses connection/communication to my VPC. This works as a firewall in which governs the connections allowed to be made to my VPC and outbounding traffic. However, we don't mess with the outbound, only the inbound rules. I made it so the connections are through SSH type 
and the IP's consist of 130.108.0.0/16 "Wright State" and 18.205.222.246/32 "AWS."

(Picture shown in "Images" directory in github. Picture Name: Security Group)
-----------------------------------------------------------------------------------------------------------------------------------------
-----------------------------------------------------------------------------------------------------------------------------------------
(Part 2 - EC2 Instances)

