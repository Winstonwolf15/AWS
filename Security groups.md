Fundamental of network security in AWS
They will control how the traffic is allowed into and out of EC2 instances.
Security groups only contain allow rules
Security groups can have rules that reference either by IP addresses or other security groups. 
This means they can also reference each other

![[Pasted image 20250215222321.png]]

Lets take an example:
We are on public internet from our computer and we are trying to access our EC2 instance from our computer. We are going to create a security group around our EC2 instance, that is firewall around it. Then this security group is going to have rules and these rules are going to say whether or not some inbound traffic from outside into the EC2 instance is allowed, And also if the EC2 instance can perform some outbound traffic. 

![[Pasted image 20250215223056.png]]
This is what security group look like.
SGs regulate
1. Access to ports
2. Authorized IP ranges IPv4 and IPv6 
3. Control the inbound network (from outside to instance)
4. Control the outbound network (from instance to outside)

In the above diagram the source column represents the IP address range. 0.0.0.0/0 means everything

Default for inbound is no access
Default for outbound is all access

![[Pasted image 20250216122044.png]]

In the above diagram we have an EC2 instance that has only one security group (SG 1) attached to it that has inbound rules and outbound rules.
If your computer IP has been authorized on port 22, then traffic can go through from our computer to EC2 instance. But if some other computer tries to access in the same way than firewall is going to block it, and timeout will occur.
For outbound rules we see that by default for any security group, if the instance wants to connect a website it is going to be allowed.


![[Pasted image 20250216122845.png]]

A security group can be attached to multiple instances.
An instance can have multiple security groups.
To switch to another region you have to create new sg. If you create another [[vpc.]] then also you have to create a new security group.
The SGs live outside the EC2, so if traffic is blocked the EC2 instance wont even see it.
Its good to maintain one separate SG just for SSH access.

![[Pasted image 20250216161034.png]]
In the above diagram the EC2 instance authorizes inbound traffic from any ec2 instance that have sg1 or sg2 security groups. So as SG3 is not allowed, it cant access.

![[Pasted image 20250216161646.png]]
22 is for logging into the EC2 instance on linux
21 ftp to share and upload files
22 can also be for sftp, that is to share file using ssh
80 for http to access unsecured websites
443 for https to access secured websites
3389 rdp login to windows instance

To access the complete page of sg from the left side menu - network and security - security groups
![[Pasted image 20250216163043.png]]

![[Pasted image 20250216163104.png]]
Here we see 2 security groups, a default one that is created by default and a launch-wizard-1 that we created when we created our EC2 instance

![[Pasted image 20250216163326.png]]

![[Pasted image 20250216163343.png]]
 SGs have an id as seen above

![[Pasted image 20250216163500.png]]
For first sg, it is SSH port 22 from anywhere
For second sg, it is HTTP from port 80 from anywhere
![[Pasted image 20250216164204.png]]
![[Pasted image 20250216164128.png]]
[[CIDR]]



