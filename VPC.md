
## Create VPC
#### CIDR Block Adress Allowcation
```
    Here I'm Taking VPC CIDR > 10.4.0.0/16
	And Public  Subnet CIDR  > 10.4.1.0/24
	And Private Subnet CIDR  > 10.4.2.0/24
	
 ```
 
 #### For Creating VPC We Have to Follow Below Steps 
 ```
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
