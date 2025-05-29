![[Pasted image 20250324235839.png]]
1) They are like network usb sticks.
2) EBS stands for elastic block store. It is a network drive that you can attach to your instance while they run, as they are network drive, they can be attached or detached to another EC2 instance very quickly.
3) One EBS volume can be mounted to only one EC2 instance at the CCP level (exam). Otherwise 16 max.
4) An EC2 instance can have multiple EBS volume attached, like two network USB sticks in one machine.
5) Like EC2 instances, these are also bound to one AZ. EBS in us East 1 canT be attached to EC2 instance in us East 2.

![[Pasted image 20250325000543.png]]
- You have to provision capacity in advance, (specify GBs and IOPs so you're are basically defining how you want your EBS volume to perform) - you get billed for the provisioned capacity.

![[Pasted image 20250325001159.png]]
It is possible to EBS volumes and leave them unattached, and we can attach later on demand

### EBS delete on termination

![[Pasted image 20250325001312.png]]

As we see above, delete on termination is ticked for root volume and not ticked for newly attached EBS. This controls EBS behavior when EC2 instance is being terminated
By default root EBS volume is deleted

While I say that in the previous lecture that EBS volumes cannot be attached to multiple instances, I know it is not true for io1 and io2 volume types: this is called the EBS Multi-Attach feature.