# Week 3 Journal

## Task 2 : View Your Addresses
  
### Commands Used
- Get-NetAdapter
- Get-NetIPAddress
- Get-NetIPAddress -InterfaceAlias "Ethernet"
- Get-NetIPAddress -InterfaceAlias "Ethernet 3"
  
![Github](./images/week3-task2-addresses.png)
![Github](./images/week3-task2-IPAdresses.png)
### Ethernet
![Github](./images/week3-task2-ethernet.png)
 - IPv4 Address (Ethernet) : 10.178.32.125 - Identifies my computer on the local network.
 - IPv6 Address (Ethernet) : fe80::a748:97db:d02c:5cf5%8 - An IPv6 address used to identify my device on the network.
 - MAC Address (Ethernet) : 74-86-E2-38-A8-84 - Unique hardware address of the physical network adapter.
### Ethernet 3
![Github](./images/week3-task2-ethernet3.png)
 - IPv4 Address (Ethernet 3) : 192.168.56.1 - Identifies the VirtualBox Host-Only Adapter on the local virtual network.
 - IPv6 Address (Ethernet 3) : fe80::5dd8:81b2:45a2:35b9%7 - An IPv6 address used to identify the VirtualBox Host-Only Adapter on the network.
 - MAC Address (Ethernet 3) : 0A-00-27-00-00-07 - Unique hardware address of the VirtualBox virtual network adapter.

## Task 3 : Ping Your Local Router
![Github](./images/week3-task3-localrouter2.png)
 - Router IP Address (Default Gateway): 10.178.32.1
 Minimum Delay: 0 ms
 Average Delay: 0 ms
 Maximum Delay: 0 ms
 Packet Loss: 0%
 - After testing the ping command to test connectivity. The router responded successfully with 0 ms minimum, average, and maximum delay, indicating a very fast local network connection.

## Task 4 : Ping your OpenWRT Linux Server
- ### Commands Used
  - ip link
  - ip addr
  - Packet Capture Command : tcpdump -i eth0 -w week3-task4-ping.pcap
  - Ping Command from Windows Host : ping 192.168.56.2
![Github](./images/week3-task4-ping-openwrtpng)
 - Destination IP: 192.168.56.2
 - Packets Sent: 4
 - Packets Received: 4
 - Packet Loss: 0%
 - Minimum Delay: 0 ms
 - Maximum Delay: 0 ms
 - Average Delay: 0 ms


## Task 7 : Find Addresses of a Website
- ![Computer Information](./images/ComputerInfo.png)

## Task 8 : Home Internet Connection
- ![Computer Information](./images/ComputerInfo.png)

