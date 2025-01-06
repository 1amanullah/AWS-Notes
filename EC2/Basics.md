# EC2 (Elastic Compute Cloud)
- In corporate data centers, applications are deployed to physical servers.
- Where do we deploy applications in the cloud ?
- ANSWER
  - Rent virtual servers, these virtual servers called EC2 instances.
  - EC2 Instances :- virtual servers in AWS ( billed by second).
  - EC2 Services :- Provision EC2 instances or virtual servers.
## EC2 Features:-
- Create and manage lifecycle of EC2 instances.
- Load balancing and auto scaling for multiple EC2 instances.
- Attach storage (& network storage) to your EC2 instance.
- Manage network connectivity for an EC2 instance.
## Our Goal:-
- Setup EC2 instances as HTTP server.
- Distributes load with Load Balancers.
## EC2 Instances:-
- In services select or search the EC2.
- Select the EC2 virtual servers in the cloud.
- Go on running instance and launch instance.
#### step 1:- Choose an Amazon Machine Image (AMI)
  - If we want to create the EC2 Instance first we need to know which OS is we need , which software we instance virtual server.
  - Select the Amazon Linux2 AMI (HVM), SSD Volume Type because it is free tier eligible so we no need to pay.
#### step 2:- Choose an instance type
  - When we create EC2 instance we need to decide how powerfull the instance should be like how much CPU we wants, how much memory we wants and how much storage we wants what is kind of network we want depending kind of application for EC2 instance type. 
  - There are total 5 type of instance 1.Genral Purpose 2.Compute Optimized 3.GPU Instances 4.Memory Optimized 5. Storage Optimized.
  - What is the diffrence between this instances? think each of this instances type is optimized for specific workload.
###### 1. Genral Purpose:- 
  - **Type:- t2.nano**
  - **VCPUs (Virtual CPUs):- 1**
  - **Memory (GB):-  0.5**
  - **Network performance:-  Low to Moderate**
###### 2. Compute Optimized:-
  - In compute optimized would have a lot more CPU in comparition to Memory or Storage.
  - So, as a ratio the compute optimized have more CPU then memory or storage or network.
  - When we want CPU intensive workload, high performance computing workload in compute optimized.
  - **Type:- c5n.large**
  - **vCPU:- 2**
  - **Memory:- 5.25**
  - **Network Performance: up to 25 Gigabit**
###### 3. GPU Instance:-
  - GPU Instance are great to use for graphic processing workloads.
  - Use for 3D graphic and media processing applications.
  - **Type:- 
