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