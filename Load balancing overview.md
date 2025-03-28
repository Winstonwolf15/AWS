![[Pasted image 20250326174837.png]]
The more users we have, the more it will balance the load across multiple EC2 instances, and this will allow us to scale our backend better.

![[Pasted image 20250326175301.png]]
- Provide SSL termination for your websites, it does this by handling SSL/TLS encryption and decryption process on behalf of backend servers - Receive HTTPS request, decrypt SSL/TLS, forward plain HTTP traffic.

![[Pasted image 20250326175913.png]]

Out of scope - 7 layers of OSI model - 
1) This is a physical layer - The plate of cake - this is like the actual wires, WIFI signals or cables that connect the computer. Without the plate the cake would fail, without this layer there is no internet.
2) Data link layer - the cake base - this layer makes sure that data moves from one device to another without crashing. Uses MAC address.
3) Network layer - The roads, GPS - this layer finds the best route for your data. It uses IP addresses to figure out where the data should go . finds the next path to send it.
4) Transport layer - the mail truck - this layer makes sure that data gets delivered safely - it breaks big messages into smaller pieces and reassembles them at destination - breaks the messages into smaller pieces.
5) Sessions layer - the mailbox - opens and closes communication between computers - keeps the chat open.
6) Presentation layer - If one speaks Chinese and the other speaks English, this layer translates them - formally it converts your texts into format internet understands.
7) Application layer - you - this is the layer you actually see - like websites, WhatsApp.

### ALB vs NLB vs GWLB:
![[Pasted image 20250328144441.png]]

- ALB - Architecture is very simple - users access your load balancers on one of these protocols - HTTP/HTTPS/gRPC - and then load balancers route traffic to one of the downstream EC2 instances or any other target specified by you.
- NLB 
	- gives Static IP not Static URL as ALB
	- It gives static IP through the use of  elastic IP, which are IP that you own and can move around - Unlike public IP which changes when you restart an instance, elastic IP remains same unless you manually release it.
	- The architecture is same as ALB, the traffic is being sent to the NLB on the TCP and UDP protocol and then forwarded to downstream targets.

- GLB 
	- Its use case is to direct traffic to firewalls that you manage on the EC2 instance, so you can do classic firewall or intrusion detection (detects intrusion, looks for attack patterns) or deep packet inspection (inspects the packet contents not just the headers, can filter contents)
	- Architecture is a little more complicated. It doesn't balance the load of your app, it actually balances the load to virtual appliances that run on EC2 instance so you can analyze the traffic. That's why its called 3rd party security virtual appliances.
	- So the traffic first goes to the gateway load balancer, then it sends traffic to these EC2 instances that will then analyze the traffic. The traffic will then be sent back to the gateway load balancer and then forwarded back to the applications.
