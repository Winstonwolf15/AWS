![[Pasted image 20250216164738.png]]

SSH allows you to control a remote cloud using CLI
From AWS console get the public IPV4 address of the instance and copy it
Also make sure a TCP port 80 rule is created

We have created an AMI with amazon for ex: ec2-user
and public IP is : 3.250.26.200
EC2Tutorial.pem is downloaded which is a private key file, go to the directory where it is placed.

do chmod 0400 EC2Tutorial.pem
this will secure the file -> 0 is for octal, 4 is for read for owner, 0 is no permission for group, 0 is no permission for others

-i is identity file

now do

ssh  -i EC2Tutorial.pem ec2-user@3.250.26.200

this should connect

Extra commands
$ ping google.com 
CTRL + D - to close


EC2 instance connect is the easiest way
Is it browser based and no extra work is required, even the private key is not shown, eveything in backend

![[Pasted image 20250216171947.png]]

![[Pasted image 20250216172009.png]]
Click on my first instance and then select connect.
![[Pasted image 20250216172103.png]]

![[Pasted image 20250216172211.png]]

