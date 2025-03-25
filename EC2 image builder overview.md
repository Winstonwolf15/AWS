![[Pasted image 20250325011842.png]]
- It is used to automate the creation, maintaining, validating and testing of virtual machines(AMI) for EC2 instances.
- It is a free service so you are only going to pay for the underlying resources. For ex, when it creates a new EC2 instance you're going to pay for them, also when the AMI are distributed you are going to pay for the storage of those AMIs.
### Why is image builder required:
Imagine you want to setup multiple servers (EC2 instances) with the same software configurations and security updates. 
If you do this manually, you would, launch an EC2 instance, install security patches and updates, install software etc, **this takes time and is error prone**.
EC2 image builder automates the entire process.

### Why do we need to automate the running of EC2 image builder?
Many companies need their EC2 instances to always run on secure, updated and standardized images. Automating EC2 image builder ensures this: security updates and patching, software config and updates, compliance and governance, performance improvements.

### Why is it an original service ? Chatgpt
