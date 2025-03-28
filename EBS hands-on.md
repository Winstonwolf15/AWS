![[Pasted image 20250226150533.png]]
To check the EBS volume attached to the instance go to Instances -> Storage -> Block devices

![[Pasted image 20250328154618.png]]
As you can see there is a block device with 8 GB size attached to EC2 instance.
If you click on the volume it will take you to another more detailed interface.
![[Pasted image 20250328154925.png]]
Here you can see that it is **in-use** and you can see the attached instance name on the bottom right

To create a new volume click on create volume
![[Pasted image 20250328155253.png]]

inside the volume creation page
![[Pasted image 20250328214057.png]]
- Make it as the same availability zone as the instance
- after submitting this, wait for the volume details page to show that volume state is available.
![[Pasted image 20250328214501.png]]


- Once its available you can attach it by clicking on actions -> attach volume
![[Pasted image 20250328214608.png]]

![[Pasted image 20250328214648.png]]
here now select the instance you want to attach it to and the device name and then click on attach volume.

If the az that you select for this volume is different than the az of your EC2 instance, the when trying to attach it will appear like this:
![[Pasted image 20250328215018.png]]

Terminating an instance: 
![[Pasted image 20250328215130.png]]
The first one is set to yes because, it is root volume and if you want to set it to no then you have to change the setting, simple only.

