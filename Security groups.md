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