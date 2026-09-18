# Week 6 Journal

## Task 1 : Completed knowledge test.

## Task 2 : Create Web Pages in OpenWRT
- Created a new HTML page 12327424.html on the OpenWRT web server and linked it from the existing `index.html` page and added a button to display the current date and time.
- Created an external CSS file and linked it with 12327424.html page to change the colour of text.
- index.html ![Github](./images/index.html)
- 12327424.html ![Github](./images/12327424.html)
- myStyles.css ![Github](./images/myStyles.css)
![Github](./images/week6-task2-webpage.png)

## Task 3 : Capture HTTP Packets.
### Commands used:
- cd (to change back to default directory)
- tcpdump -i eth0 -n -w http-12345678.pcap (to generate pcap file and trace the webpage activity)
- Ctrl^C : to stop the packet capture process
![Github](./images/week6-task3-arp-table.png)



