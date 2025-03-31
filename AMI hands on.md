![[Pasted image 20250328222753.png]]

- Go to instances -> Click on launch an instance
- Select security groups, OS, volume, 
- In the user data - > install http commands only
- It will take time to start so if you open the IP address very soon then it will fail.

Now the instance has been created. So to create AMI:
![[Pasted image 20250328223809.png]]
Right click on the instance, then click on image and template then click on create image.
A page will open asking for details about the image. Fill the name and leave remaining details as is and click on create image. 

![[Pasted image 20250328224232.png]]

So the AMI is registered. 

![[Pasted image 20250328224258.png]]

Now you can launch instances from this AMI
1. You can launch by clicking on launch instances from AMI (above pic)
2. Or you can click on Instances tab -> Launch instances -> in the quick start
3. ![[Pasted image 20250401005358.png]]
4. Select your AMI - (Demo image is the AMI you just created) -> Now follow the same steps
5. For user data copy just the last line that shows the http URL. You don't need the earlier lines (installing HTTP etc.) because AMI you created this from already contains http user data, so reinstalling HTTP is not required. **This will speed up boot time**