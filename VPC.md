# Smaple CI/CD 
Design and deploy the given application on to AWS cloud using CI/CD best practices

Clone the sample express application Express App

```sh
Create a custom VPC
Create private & public subnets
Create CI/CD pipeline using CodeCommit, CodeBuild, CodeDeploy and Pipeline
Application can deployed on ECS / EC2
The application should run on private instances and serve through ELB
Whenever the code gets committed to the master branch, the application should be redeployed.
High level documentation
```


#### Create VPC
```sh
    Here I'm Taking VPC CIDR > 10.4.0.0/16
	And Public  Subnet CIDR  > 10.4.1.0/24
	And Private Subnet CIDR  > 10.4.2.0/24
	
 ```
 
 #### For Creating VPC We Have to Follow Below Steps 
 ```sh
    1. Create VPC, And Enable DNSHostName
	   > Here VPC CIDR Block Address > 10.4.0.0/16
	2. Create Public Subnet, And Enable Modify auto-assign IP Settings.
	   > Here Subnet CIDR Block Address > 10.4.1.0/24
	   > This 'Modify auto-assign IP Settings' Option will allow the Assign Auto Public IP to Instances.
	3. Create Public Subnet.
	   > Here Subnet CIDR Block Address > 10.4.2.0/24
	4. Create Internet gateway (IGW) and attach to VPC.
	5. Use default Route table for Public Subnet.
	   > In Subnet Associations add Public subnet.
	   > and also edit routes add '0.0.0.0/0 to IGW'
	6. Now Create NAT Gateway For Private Subnet Internet.
	   > When you create NAT Gateway It Asking for subnet and EIP.
	     > Note Choose 'Public Subnet'.
	7. Create New Route Table For Private Subnets.
	   > In Subnet Associations add Private subnet.
	   > and also edit routes add '0.0.0.0/0 to NAT Gateway' 
	8. Security Groups 
	   > when you create VPC one Security group available ypu can use that security group.
  ```
#### Create Codecommit Repo
```sh
   1. Create one repo in AWS Codecommit.
   2. for git operations, you need code-commit crediatils.
   3. 
```
