![[Pasted image 20250218142849.png]]

## On-demand instances:
![[Pasted image 20250321022332.png]]
Pay for what you use. They are good for short workloads, pay by the second. Has highest cost but no upfront payment. 
Recommended for short term uninterrupted workload, where you cant predict how the application will behave.

## Reserved instances:
![[Pasted image 20250321022349.png]]
Up to 72%** discount compared to on demand.
You reserve for specific instance attributes - instance type, OS, region, [[tenancy]]
A reservation period is specified, from 1 to 3 years to get even more discounts. More discount for 3 years.
Payment options are upfront, partial upfront, no upfront, Upfront is max discount.
You can choose the scope to be in a particular region or scope, regional or zonal.
Recommended for steady-state app usage apps like database.
Can buy sell in marketplace.

Convertible reserved instance - it can change the EC2 instance type, instance family, OS, scope tenancy. Up to 66% discounts.

## Savings plan:![[Pasted image 20250321022411.png]]
Discount for long term usage is up to 72%. You have to commit for a certain type of usage, like $10/hr. for 1 to 3 years. Usage after this is billed as per on-demand price.

In this the user is locked to a specific instance family and AWS region.
Not locked for 
1. instance sizes, m5.xlarge, m5.2xlarge
2. OS
3. Tenancy - dedicated, host, default

## Spot instance: 
![[Pasted image 20250321022426.png]]
Discount up to 90%
Suitable for workload with flexible start and end time
Not suitable for critical jobs
Not suitable for database
But you can lose at any point in time. This happens because initially you are asked for a max price, that you are wiling to pay. If the spot price goes over that, then you will lose the instance.
They are the most cost efficient instances in AWS.
They are helpful is your workload is resilient to failure.

## EC2 Dedicated hosts
![[Pasted image 20250321022438.png]]
The physical server - EC2 instance is fully dedicated to your use.
This is better if you have to address compliance requirement
Purchasing options on demand, reserved. 
Most expensive
Helpful in regulatory and security compliance.

## Dedicated instance
![[Pasted image 20250321022904.png]]
They are like - you rent a private apartment in a building but the landlord decides which unit to give you.
Dedicated hosts - you rent an entire building and decide which rooms to use and for what purpose.

So in dedicated instance you have no control over instance placement. 

## Capacity reservation
![[Pasted image 20250321023238.png]]
This ensures that you have guaranteed compute capacity in a specific AZs when needed.
Reserve, on demand instance 
