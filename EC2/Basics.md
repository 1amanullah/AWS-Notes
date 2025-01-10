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
   - **vCPUs (Virtual CPUs):- 1**
   - **Memory (GB):-  0.5**
   - **Network performance:-  Low to Moderate**
  ###### 2. Compute Optimized:-
   - In compute optimized would have a lot more CPU in comparition to Memory or Storage.
   - So, as a ratio the compute optimized have more CPU then memory or storage or network.
   - When we want CPU intensive workload, high performance computing workload in compute optimized.
   - **Type:- c5n.large**
   - **vCPUs:- 2**
   - **Memory (GB):- 5.25**
   - **Network Performance: up to 25 Gigabit**
  ###### 3. GPU Instance:-
   - GPU Instance are great to use for graphic processing workloads.
   - Use for 3D graphic and media processing applications.
   - **Type:- g4dn.xlarge**
   - **vCPUs:- 4**
   - **Memory (GB):- 16**
   - **Instance Storage:- 1 x 125 (SSD)**
   - **Network Performance:- Up to 25 Gigabit**
  ###### 4. Memory Optimized:-
   - Memory Optimized have a lot of memory compare to CPU, Storage and Network Performance.
   - This are optimized for running things like memory caches so for memory cache, distributed caches and things like.
   - **Type:- r5ad.large**
   - **Memory (GB):- 16**
   - **Instance Storage:- 1 x 25(SSD)**
   - **Network Performance: Up to 10 Gigabit**
  ###### 5. Storage Optimized:-
   - Storage Optimized have a lot of storage attached with then compare CPU and Memory.
   - This use for running data ware houses or run I/O intensive applications.
   - **Type:- d2.xlarge**
   - **vCPUs:- 4**
   - **Memory:- 30.5**
   - **Instance Storage:- 3 x 2048**
   - **Network Performance:- Moderate**
###### Select now from **Genral Purpose** like **t2.micro** it is free tier elible.
#### Step 3:- Configure Instance Details
  - Not worry and move to next step.
#### Step 4:- Add Storage
  - In this we need to attached a root disk with EC2 instance.
  - The default size of 8GB is perfect and we use a Genral Purpose hard disk.
#### Step 5:- Add Tag
  - Add tags to EC2 instances.
  - Tags are very underrated but one most of the important feature in AWS.
  - There we add tag to indicating for example:
   
    | #Key | #Value |
    | ---- | ------
    | Name | First EC2 Instance
    | Environment  | Dev
    | Business Unit| A
    
#### Step 6:- Configure Security Group
  - Security Group is nothing but a fierwall, virtual fierwall in front of EC2 instance.
  - We can decide what kind of traffic want to allocate into the EC2 instance and what kind of traffic want to allow outside of EC2 instance.
  - Create a new security group
  - **Security Group Name: ec2_security_group**
  - **Type: SSH**
  - **Protocol: TCP**
  - **Port Range: 22**
  - **Source: custom 0.0.0.0/0 (from everywhere)**
#### Step 7:- Review Instance Launch
  - In AWS their is no password only public and private key.

## EC2 Instance Type:-
  - Optimized combination of compute (CPU,GPU), memory, disk, storage and networking for specific workloads.
  - 270+ instances acress 40+ instance types for different workloads.
  - t2.micro
     - **t :- Instance Family.**
     - **2 :- Genration. Improvement with eac genration.**
     - **micro :- Size ( nano < micro < small < medium).**
  - As size increases, compute (CPU,GPU), memory and networking compabilities increase proportionately.
  - Connect to your instance.
  - EC2 Instance connect (browser-based SSH connection).
