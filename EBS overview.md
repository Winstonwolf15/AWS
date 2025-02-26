Write initial from VDI

It is possible to EBS volumes and leave them unattached, and we can attach later on demand

### EBS delete on termination

![[Pasted image 20250226144912.png]]


As we see above, delete on termination is ticked for root volume and not ticked for newly attached EBS. This controls EBS behavior when EC2 instance is being terminated
By default root EBS volume is deleted