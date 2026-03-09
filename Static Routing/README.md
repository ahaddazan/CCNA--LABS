### 1. Network Topology
![Topology Diagram](topology.png.png)

## Detailed Router Configurations

### 1. Router R1 (Edge Gateway)
R1 connects the local LAN (PC1) to the rest of the network.
* **Commands used:**
```text
R1(config)# interface g0/1
R1(config-if)# ip address 192.168.1.254 255.255.255.0
R1(config-if)# no shutdown
R1(config)# ip route 192.168.3.0 255.255.255.0 192.168.12.2
```
### 2. Router R1 - show ip route
![R1 Routing Table](r1-routingtable.png.png)

2. Router R2 (Hop)
* **Commands used:**
```text
R2(config)# ip route 192.168.1.0 255.255.255.0 192.168.12.1
R2(config)# ip route 192.168.3.0 255.255.255.0 192.168.13.3
```
### 3. Router R2 - show ip route
![R2 Routing Table](r2-routingtable.png.png)

3. Router R3
* **Commands used:**
```text
R3(config)# ip route 192.168.1.0 255.255.255.0 192.168.13.2
### 4. Router R3 - show ip route
```
![R3 Routing Table](r3-routingtable.png.png)

### 5. Connectivity Proof (Tracert)
![PC1 to PC2 Tracert](pc1-tracert.png.png)

### 6. Connectivity Proof (Tracert)
![PC2 to PC3 Tracert](pc2-tracert.png.png)
