## vpc

The open systems interconnection(OSI) model  

1. Physcial layer - Port physcial port cable  
2. Data link layer - MAC  
3. Network layer - IP address  
4. Transport layer - TCP three way handshake  

1. Physcial layer -> bits  -> coax, Fiber , wireless  
2. Data link layer -> Frames  -> Ethernet, 802.11   
3. Network layer -> packets-> IP, IPSEC, ICMP  
4. Transport layer-> segments -> TCP,UDP,TLS  
5. Session layer-> Data -> TCP, RPC  
6. Presentation layer -> Data -> SSL , FTP, SSH, HTML  
7. Application layer -> DATA -> HTTP, FTP,SSH, DNS  

- Media, signal, binary transmission  
- Physical addressing  
- Path determination  
- End-to End connections & reliability  
- Interhost communication  
- Data representation & encryption  

Security groups & Network ALCs  
- A Stateful firewall allows the return traffic automatically  
- A Stateless firewall checks for an allow rule for both connections.  

NACLs apply at the sunet level  
NACLs apply only to traffic entering / exiting the subnet  

Security groups can be applied to instances in any subnet.  
 
Security group  
- Operates at the instance level  
- Supports allow rules only   
- sateful  
- Evaluates all rules  
- Applies to an instance only if associated with a group  

Network ACL 
- Operates at the subnet level  
- Support allow and deny rules  
- stateless  
- Process rules in order  
- Automatically applies to all instance in the subnets its associated with  

