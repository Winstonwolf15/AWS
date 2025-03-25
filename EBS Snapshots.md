![[Pasted image 20250325001816.png]]
- They are backups of your EBS volumes
- We can copy snapshots across various AZ or region. As EBS volumes are limited to one az, after copying a snapshot, we can use this snapshot to restore a new ebs volume in another region.

![[Pasted image 20250325005931.png]]
- EBS snapshot archive - useful for snapshots that you don't want to restore in a rush and you want to save some cost on them.
- Recycle bin - set up recycle bin for snapshots with some rules.