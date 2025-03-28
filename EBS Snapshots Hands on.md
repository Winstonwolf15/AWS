![[Pasted image 20250328220042.png]]
To create snapshot goto ebs volume, select one volume, click on actions and then create snapshot
![[Pasted image 20250328220140.png]]
Give it a name and then create snapshot

![[Pasted image 20250328220216.png]]

You can copy this snapshot into another region
![[Pasted image 20250328220307.png]]

![[Pasted image 20250328220410.png]]

Another thing you can do is take a snapshot and recreate a volume for it. 

![[Pasted image 20250328221826.png]]

Go to Action - > Create volume from Snapshot.


Here you can enter any destination region you want. This will come in handy incase you want a to have a disaster recovery strategy.

Fill the required details and then Click on create volume.

![[Pasted image 20250328222040.png]]

Now we have 2 volumes. And as you can see that the first one was restored through a snapshot.


### Recycle bin
![[Pasted image 20250328222412.png]]
It protects your EBS snapshots and AMIs from accidental deletion

![[Pasted image 20250328222356.png]]
Click in create retention rule
![[Pasted image 20250328222508.png]]
You can select the resource type, retention period, and apply to all resources.


