![[Pasted image 20250325221127.png]]
 1) It stands for elastic file system.
 2) It is the third type of storage that you can attach to the EC2 instance.
 3) It is a managed network file system. Here managed means that it is maintained by AWS, that means it doesn't require manual scaling when more storage is needed.
 4) It can be mounted to 100s of EC2 instances at a time. Unlike EBS volume that is attached only to one instance. So, this is also a shared NFS.
 5) EFS works only with Linux EC2, and it works across multiple availability zones. Different instances from different AZs can be attached to the same EFS. For EBS volumes its not possible across different AZs, to move over we were required to create snapshots there. But this would be a copy and not an in-sync replica.
 6) It is highly available, scalable, three times as expensive as EBS volume.
 7) You pay per use and don't' plan for capacity.
 
![[Pasted image 20250325222505.png]]

### EFS infrequent access
![[Pasted image 20250325222702.png]]
1) If you enable EFS- IA then EFS will automatically move your files to EFS-IA based on the last time they were accessed.(no read or writes)(Something called a lifecycle policy)
2) Next time the file is accessed it will be put back in EFS standard.
3) You app doesn't need to know whether the file is in EFS standard or EFS-IA, it will access all the files the same way.

