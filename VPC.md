
## Create VPC
#### CIDR Block Adress Allowcation
```
Here I'm Taking VPC CIDR > 10.4.0.0/16
 And Public  Subnet CIDR  > 10.4.1.0/24
```
 
#### For Creating VPC We Have to Follow Below Steps 
#### Create VPC
```
Create VPC, And Enable DNSHostName
  > Here VPC CIDR Block Address > 10.4.0.0/16
```
#### Create Subnets
```
Create Public Subnet.
 > Here Subnet CIDR Block Address > 10.4.1.0/24
And Enable Modify auto-assign IP Settings.
 > This 'Modify auto-assign IP Settings' Option will allow the Assign Auto Public IP to Instances.
```
#### Create Internet Gateway
```
Create Internet gateway (IGW) and attach to VPC.
```
#### Route table
```
Use default Route table for Public Subnet.
 > In Subnet Associations add Public subnet.
 > and also edit routes add '0.0.0.0/0 to IGW'
```
#### Create Security Group
```  
Security Groups 
 > when you create VPC one Security group available ypu can use that security group.
```

