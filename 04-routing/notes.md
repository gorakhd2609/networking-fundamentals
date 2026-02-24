# Routing Protocols (RIP, OSPF, EIGRP)

## RIP
- RIP v1: Classful  
- RIP v2: Classless (supports CIDR)  
- Metric: Hop count (max 15)  
- Simple but slow convergence  

## OSPF
- Link-State protocol  
- Uses areas  
- Metric: Cost  
- Fast convergence  
- Scales well in large networks  

## EIGRP
- Advanced distance-vector (hybrid)  
- Uses DUAL algorithm  
- Very fast convergence  
- Efficient bandwidth usage  

## Commands (Cisco)
 RIP v2 – Sample Config
Router(config)# router rip  
Router(config-router)# version 2  
Router(config-router)# network 192.168.1.0
Router(config-router)# exit
### What I learned
- RIP converges slowly when links fail  
- Limited to 15 hops, not suitable for large networks  
- Easy to configure but not scalable
  ## OSPF
- Link-State protocol  
- Uses areas  
- Metric: Cost  
- Fast convergence  

### Commands (Cisco)
OSPF - sample config
Router(config)# router ospf 1  
Router(config-router)# network 192.168.1.0 0.0.0.255 area 0
Router(config-router)# exit

### What I learned
- OSPF recalculates routes faster than RIP  
- Area design helps in large networks  
- Better choice for enterprise networks  

## EIGRP
- Advanced distance-vector (hybrid)  
- Uses DUAL algorithm  
- Very fast convergence  
### Commands (Cisco)

EIGRP - sample config
Router(config)# router eigrp 100  
Router(config-router)# network 192.168.1.0  
Router(config-router)# exit
### What I learned
- EIGRP converges very fast  
- Uses DUAL algorithm for loop-free paths

  Add routing protocols notes, configs & observations
- More efficient than RIP in dynamic networks
## 📌 My Practice Setup
- Tool used: Cisco Packet Tracer  
- Topology: 2 Routers + 2 PCs  
- Goal: Compare RIP vs OSPF vs EIGRP convergence and behavior
