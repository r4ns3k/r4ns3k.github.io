As we have seen in previous post ip address is of 32 bits 
for 32 bits,we will get 2^32 diffrent ip addresses,by using formula 2^n  (n is the number of bits),

ip address is combination of two addresses in one address ,they are
1.device address
2.network address in which device in
for example if we have address 200.0.0.1 which is device ip address ,then network address will be 200.0.0.0
NOTE: ALways first ip address is used for network address,last adresss ip is used for broadcast address.

range of 32 bits 00000000.00000000.00000000.00000000 - 0.0.0.0
                 11111111.11111111.11111111.11111111 -255.255.255.255
                 
## Initial classification

Initially they have choosen first 8 bits for network address remaining 24 bits for host addresses
with that we will get 2^8 networks ,2^24 hosts per network
256 networks not enough so cllassful addresses came

## classful classficatio
in classful addressing they are 5 diffrent classes class A,B,C,D,E.

Lets go through the difrrent classes

## class A
same as initial classification here also they have choosen first 8 bits for network address remaining 24 bits for host addresses
with that we will get 2^8 networks ,2^24 hosts per network

 xxxxxxxx.xxxxxxxx.xxxxxxxx.xxxxxxxx
 |--NID--||-----------HID----------|
 
 NOTE:The first octet first bit is fxed and set to 0
## range 
 00000000 - 0
 00000001 - 1
     .
     .
 01111111 - 127
     
range can be 0-127 but the practical range can be 1-126

range 1.0.0.0 - 126.0.0.0

## class B
In classB they have choosen first  16 bits for network address remaining 16 bits for host addresses
with that we will get 2^16 networks ,2^16 hosts per network

 xxxxxxxx.xxxxxxxx.xxxxxxxx.xxxxxxxx
 |----NID---------|----HID---------|
 
 The first octet first two bits are fxed and set to 10
## range 
 10000000 - 128
 10000001 - 129
     .
     .
 10111111 - 191
     
range can be 128-191

range 128.0.0.0 - 191.255.0.0

## class C
In classC they have choosen first  24 bits for network address remaining 8 bits for host addresses
with that we will get 2^24 networks ,2^8 hosts per network

 xxxxxxxx.xxxxxxxx.xxxxxxxx.xxxxxxxx
 |----NID------------------|---HID--|
 
 The first octet first three bits are fxed and set to 110
## range 
 11000000 - 192
 11000001 - 193
     .
     .
 11011111 - 223
     
range can be 192-223

range 192.0.0.0 - 223.255.255.0


Now we can say which class the ip belongs to by seeing its range
classA 1-127
ClassB 128-191
class c 192-223

class D,E addresses used for special purposes







