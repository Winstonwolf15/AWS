Connect with the EC2 instance

To check iam roles attached to the instance run $ aws iam list-users
![[Pasted image 20250216211226.png]]

As there are no credentials present, we can run $ aws credentials, to configure credentials. 

![[Pasted image 20250216211524.png]]
But this is a bad idea, as someone else wo accesses this EC2 instance can see those credentials

Instead we can use IAM roles.
To attach IAM roles, goto Instances -> Action -> Security -> Modify IAM role
![[Pasted image 20250216212413.png]]
![[Pasted image 20250216212431.png]]

Then you have to choose an IAM role (created earlier by you). Then click on save to attach this IAM role to our instance.

Now go back to the instances page, there if you go to security you can see the IAM role
![[Pasted image 20250216212702.png]]

Now run $ aws iam list-users again
![[Pasted image 20250216212854.png]]

So the role is now linked to the EC2 instance, and this is a good way to provide AWS credentials to our EC2 instance.



