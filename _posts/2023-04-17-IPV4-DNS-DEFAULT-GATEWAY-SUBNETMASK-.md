---
published: true
---

ISP gives us 4 things

1)IPV4 address<br>
2)DNS<br>
3)Default Gateway<br>
4)Subnet Mask<br>

ipv4 address is used for identify device on a network and to reach other host on internet<br>
dns used for convert domain name into ip address,used when we provide domain name instead of ip,and dns used in the process of reaching ther host<br>
defulat gateway is the router's ip address<br>
being a host why we need subnet mask<br>
subnet mask is used by routers to direct traffic to the desired subnet,then why hosts need subnet mask?,hosts also use subnet mask<br>
to find whether destination ip is in same network or diffrent network,if destination ip is in same network host will directly send packet<br>
if other network host will send it router and router forwards to the destination<br>
even though host need subnet mask to differntiate diff network ,subnet mask is set in a way that evry ip is belongs to the difrrent network<br>
subnet mask used by our computer's 255.255.255.255<br>
if use above subnet mask and do bitwise AND we get that ip is nid so every ip is treated as its own network<br>
so evry packet must reach the router to send packet even 2 hosts are in same network this will increase privacy of the network<br>
