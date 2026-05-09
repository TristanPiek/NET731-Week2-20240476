# NET731-Week2-20240476
This Repository is for my Week 2 NET practical. 


## Personal Information
Tristan Piek 

20240476




## TechBridge Solutions Scenario

a Small Business called TechBridge Solutions asked me to design and implement a cloud network architecture. I used Microsoft
Azure and created s suitable virtual network, subnets and network security groups (NSGs), and created rules to divide public
access from private access.



## Virtual Network Design

#### Component | Chosen Config.

VNet Name : TechBridge-Solutions-SA-VNet

Address Space : 22.0.0.0/18

Region : South Africa North 



#### Explanation for these choices

The 22.0.0.0/18 address space was chosen because it falls in the private IP range, there would be enough usable addresses
for the orinization for its current business requirements aswell as going forward and allows for further growth and subnet
expansion.


## Subnet Design


| Subnet Name | Address Range | Purpose |
|---|---|---|
| Public-Subnet | 10.0.1.0/24 | Hosts public-facing services |
| Private-Subnet | 10.0.2.0/24 | Hosts internal backend systems |


### Explanation for these choices

Separate subnets were created to improve security and network organisation by isolating public resources from internal
systems.



## Network Security Group (NSG)

| Rule Name | Port | Protocol | Action | Purpose |
|---|---|---|---|---|
| Enable-HTTP | 80 | TCP | Allow | Allows website traffic |
| Enable-HTTPS | 443 | TCP | Allow | Allows secure web traffic |
| Deny-Inbound | * | Any | Deny | Blocks unauthorized inbound traffic |

### NSG Justification
The NSG rules were configured to allow secure web traffic while restricting unnecessary inbound access to the network.



## Screenshots

### Resource Group
![Resource Group](screenshots/resource-group.png)

### Virtual Network
![VNet](screenshots/vnet.png)

### Subnets
![Subnets](screenshots/subnets.png)

### NSG Rules
![NSG](screenshots/nsg.png)

### NSG Attached
![NSG Attached](screenshots/nsg-attached.png)





