EC2 stands for elastic compute cloud, it is IAAS![[Pasted image 20250215151423.png]]


![[Pasted image 20250215151939.png]]

EC2 sizing and configuration options:
OS : Linus, Windows and Mac
[[AI answer for different storage options|Storage can be networ k attached or hardware.]]
Here this means that storage can be attached over network to the host machine, rather than being directly attached to the physical server hosting the machine, example EBS (Elastic block storage) and EFS (Elastic file system)
EC2 user data or bootstrap script => this is to configure data at first launch.

![[Pasted image 20250215155128.png]]

In Bootstrapping certain commands run when a machine starts. Script only runs once. Automate boot tasks such as installing updates, installing software anything else.
One issue is the more tasks you bootstrap, the more the boot time

![[Pasted image 20250215155846.png]]
Above Mem stands for memory
t2.micro - free tier - 1vcpu, 1 Gib, EBS

[[c5d.4xlarge]] - here 400 NVMe is attached to the EC2 instance
