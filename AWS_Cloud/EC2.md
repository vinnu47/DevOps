## EC2

Scaling up - increasing the size of server
Scaling out - increasing the no of instances

### High Availabilty                                                                    
- Minimal service interruption                                        
- Designed with no single point of failure (redundency) 
- Uptime measured in % e.g 99.99%                                                        
- Synchronous or asynchronous                                            
- lower cost compared to FT                                                          
- Services that create HA:   
    - Elastic load balancing
    - EC2 Auto scaling  
    - Amazon Route 53  

### Fault Tolerance  
- No service interruption   
- specialized hardware with instaneous failover  
- No downtime  
- Synchronous replication  
- Highest cost compared to HA   
- Example of Ft:  
    - fault tolerance NLCS  
    - Disk mirroring  
    - Synchronous DB replication  
    - Redundant power   

- An EC2 instance is a virtual server  
- A selection of instance types comes with varying combination of CPU, memory, storage & networking.  

### Public , private $ Elastic IP address  

Public IP address  
- lost when the instance is stopped  
- used in public subnets  
- No charge  
- Associated with a Private IP address on the instance  
- cannot be moved between instances  

Private IP address    
- Retained when the instance is stopped    
- used in public & private subnets    

Elastic IP address  
- Static public IP address  
- Your are charged if not used  
- Associated with a private IP address on the instance   
- can be moved between instances and elastic network adapters  

### launcing EC2 instance
EC2 instance type  
| Family            | Type       | CPUs | Memory |
|:------------------|------------|------|--------|
| General Purpose   | t2micro    |   1  |   1    |
| Compute optimized | c5n.large  |   2  |  5.25  |
| Memory optimized  | r5ad.large |   3  |   16   |
| Storage optimized | d2.xlarge  |   4  |  30.5  |
| GPU instances     | g2.2xlarge |   8  |   15   |

### Using Access Keys with EC2
- AWS CLI confifured with Access keys  
- The access key is associated with an IAM user  
- The access key will use the permission assigned to the IAM user  


### Type of Elastic load balances
Application load balances  
- Operate at the request level  
- Routes based on the content of the request  
- Supports path based routing, host-based routing,query string parameter-based routing, and source ip address based routing.   
- Support instance, IP address, lambda functions and containers as targets.   

### Network load balancer
- Operate at the connection level  
- Routes connections based on IP Protocol data.  
- Offers ultra high performance, low latancy & tls offloading at scale.   
- Can have a static IP/ Elastic IP   
- Supports UDP & static IP address as targets    

### Gateway load balancer
- Used in front of virtual application such as firewalls, ids/ips, and deep packet inspection systems.  
- operates at layer 3 - listens for all packets on all parts  
- Forward traffic to the TG specified in rules.  
- Exchange traffic with application using the geneve protocol on port 6081  
