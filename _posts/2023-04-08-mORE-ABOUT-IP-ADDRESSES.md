---
  published: false
---

As we have seen in previous post ip address is of 32 bits <br>
With 32 bits,we will get 2^32 diffrent ip addresses,by using formula 2^n  (n is the number of bits)

ip address is combination of two addresses in one address ,they are<br>
1.device address<br>
2.network address in which device in<br>
for example if we have address 200.0.0.1 which is device ip address ,then network address will be 200.0.0.0.<br>
NOTE: ALways first ip address is used for network address,last adresss ip is used for broadcast address.

range of 32 bits <br>
00000000.00000000.00000000.00000000 - 0.0.0.0<br>
11111111.11111111.11111111.11111111 -255.255.255.255<br>
                 
## Initial classification

Initially they have choosen first 8 bits for network address remaining 24 bits for host addresses<br>
with that we will get 2^8 networks ,2^24 hosts per network<br>
256 networks not enough so classful addresses came

## classful classfication
in classful addressing they are 5 diffrent classes class A,B,C,D,E.

Lets go through the difrrent classes

## class A
same as initial classification here also they have choosen first 8 bits for network address remaining 24 bits for host addresses<br>

 fnnnnnnn.hhhhhhhh.hhhhhhhh.hhhhhhhh<br>
 f-fixed bit
 n- network bits
 h - host bits
 
 NOTE:The first octet first bit is fxed and set to 0<br>
 
 total no. of ip's=2^31 
total networks 2^7 = 128 networks = 126(practical) * total no. of hosts can be configured /network 2^24 =16 M Hosts(ips)

## range <br>
 00000000 - 0<br>
 00000001 - 1<br>
     .<br>
     .<br>
 01111111 - 127

range can be 0-127 ,but the practical range can be 1-126
0.0.0.0 , 127.0.0.0 addresses are reserved
usable ip space: 1.0.0.0 - 126.0.0.0
Used for large networks
## class B<br>
In classB they have choosen first  16 bits for network address remaining 16 bits for host addresses<br>

ffnnnnnn.nnnnnnnn.hhhhhhhh.hhhhhhhh

 
 The first octet first two bits are fxed and set to 10<br>
 total no. of ip's we get with 30 bits(32-2fixed bits)=2^30
total networks = 2^14
totla no. of hosts can be configured /network =2^16
## range 
 10000000 - 128<br>
 10000001 - 129<br>
     .<br>
     .<br>
     .<br>
 10111111 - 191
 total no. of ip's we get with 30 bits(32-2fixed bits)=2^30
total networks = 2^14 =16K
totla no. of hosts can be configured /network =2^16
range can be 128-191

range 128.0.0.0 - 191.255.0.0

## class C<br>
In classC they have choosen first  24 bits for network address remaining 8 bits for host addresses<br>
with that we will get 2^24 networks ,2^8 hosts per network

 fffnnnnn.hhhhhhhh.hhhhhhhh.hhhhhhhh
 
 The first octet first three bits are fxed and set to 110<br>
## range 
 11000000 - 192<br>
 11000001 - 193<br>
     .<br>
     .<br>
 11011111 - 223
     total networks = 2^21
     totla no. of hosts can be configured /network =2^8
range can be 192-223

range 192.0.0.0 - 223.255.255.0


Now we can say which class the ip belongs to by seeing its range<br>
classA 1-126<br>
ClassB 128-191<br>
class c 192-223<br>

class D,E addresses used for special purposes







