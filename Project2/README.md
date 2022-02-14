PART 1 - BUILD A VPC

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

I created a security group that it attached to my BRADLEY-VPC. I created 2 inbound rules, which gives my personal computer and WSU IP 
addresses connection/communication to my VPC. This works as a firewall in which governs the connections allowed to be made to my VPC and outbounding traffic. However, we don't mess with the outbound, only the inbound rules. I made it so the connections are through SSH type 
and the IP's consist of 130.108.0.0/16 "Wright State" and 98.28.114.87/32 "Personal Computer."

(Picture shown in "Images" directory in github. Picture Name: Security Group)
-----------------------------------------------------------------------------------------------------------------------------------------
PART 2 - EC2 INSTANCES

Step 1: Creating New Instance

For this step I decided to use Ubuntu server 20.04 LTS. The default username for Ubuntu is ubuntu. The instance type I picked is t2.microWhich this is the best option, because we are cheap and want it free!

-----------------------------------------------------------------------------------------------------------------------------------------
Step 2: Attach Instance to VPC

I used the drop down window to select my VPC and subnet.

-----------------------------------------------------------------------------------------------------------------------------------------
Step 3: Determine IPv4

I disabled the auto create, because we are not wanting aws to change our ip address later. Therefore, we will be separately creating the elastic IP and attaching it to the instance.

-----------------------------------------------------------------------------------------------------------------------------------------
Step 4: Attaching Volume

For this part I made the volume 16 GiB.

-----------------------------------------------------------------------------------------------------------------------------------------
Step 5: Adding Tag

For the Tag I made the Key: Name and the Value: BRADLEY-Ubuntu.
 
-----------------------------------------------------------------------------------------------------------------------------------------
Step 6: Security Group

I had to select my BRADLEY-sg which showed my inbound rules and then chose existing key pair, finally I pressed review and launch.

-----------------------------------------------------------------------------------------------------------------------------------------
Step 7: Elastic IP

Had to go to Network and Security tab and select Elastic IPs and then asscoicate my a Private IP.

-----------------------------------------------------------------------------------------------------------------------------------------
Step 8: Screenshot

(Picture shown in "Images" directory in github. Picture Name: Instance Details)
-----------------------------------------------------------------------------------------------------------------------------------------
Step 9: Host Name

To change the Ubuntu's hostname I ran hostname, which showed ubuntu, then ran sudo -u root hostname BRADLEY-AMI. This changed my host
name successfully!

-----------------------------------------------------------------------------------------------------------------------------------------
Step 10: Screenshot

(Picture shown in "Images" directory in github. Picture Name: SSH and Hostname)
----------------------------------------------------------------------------------------------------------------------------------------- 



