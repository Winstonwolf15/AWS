Key pair to securely connect to your instance.
![[Pasted image 20250215162244.png]]

.pem for mac and windows 10
.ppk for less than windows 10

![[Pasted image 20250215162207.png]]
First security group automatically created by AWS is called launch-wizard-1

![[Pasted image 20250215162402.png]]
Free tier can get 30 gb of general purpose SSD

![[Pasted image 20250215162537.png]]
this is going to run only once in the whole lifecycle of the instance
As per the above commands:
1. Perform some updates
2. Install Httpd web server
3. Start and enable httpd
4. Html file that will be on the webserver.

![[Pasted image 20250215163003.png]]

Now the instance is running : we see
1. Instance name
2. Instance ID - UID
3. Public IP - To access the instance
4. Private IP - To access the instance internally on AWS network

![[Pasted image 20250215163444.png]]
The AMI is Amazon Linux 

![[Pasted image 20250215170658.png]]
As we see here the instance is running
![[Pasted image 20250215170735.png]]
To stop the instance

Why do you stop an instance? The longer it runs the more you pay

When you stop then start an instance , the public IP changes , but the private IP remains the same.

To open the webpage of the running instance, put http://{publicIPaddress} not https://