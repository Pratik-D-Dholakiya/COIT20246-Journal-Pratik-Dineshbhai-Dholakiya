# Week 5 Journal

## Task 1 : Completed knowledge test

## Task 2 : View Routing Table
![Github](./images/week5-task2-routing-table.png)

## Task 3 : View Your Addresses  
![Github](./images/week5-task3-network-diagram.png)

#### Router 1 Routing Table
| Network Destination | Netmask | Gateway (Next Hop) | Interface |
| :--- | :--- | :--- | :--- |
| 74.24.0.0 | 255.255.255.0 | 0.0.0.0 (Direct) | Fa0/0 |
| 172.16.100.0 | 255.255.255.252 | 0.0.0.0 (Direct) | Se0/0 |
| 10.0.56.0 | 255.255.255.0 | 172.16.100.2 | Se0/0 |

#### Router 2 Routing Table
| Network Destination | Netmask | Gateway (Next Hop) | Interface |
| :--- | :--- | :--- | :--- |
| 10.0.56.0 | 255.255.255.0 | 0.0.0.0 (Direct) | Fa0/0 |
| 172.16.100.0 | 255.255.255.252 | 0.0.0.0 (Direct) | Se0/0 |
| 74.24.0.0 | 255.255.255.0 | 172.16.100.1 | Se0/0 |


