----
published: true
----
Dividing big network into many smaller networks is called subnetting.

# advantages:
privacy.

# Example:
we have 200.0.0.0 network address<br>
by seeing first octet we can tell it's cllas c,and have 256 hosts,for small network itsa huge right let's divide the network into 2 subnets

if we choose one bit from binary we have divided the bits into parts<br>
|0|
|-|
|1|<br>

if we choose 2 bits entire bit space divided into 4 parts

|00|
|-|
|01|
|10|
|11|

like wise 3 bits 8 parts (2^3=8)<br>

To divide network into 2 parts we need one bit ,so borrow one bit from host id<br>
|part-1|part2|
|------|-----|
00000000 |1000000|

range
subnet-1|subnet-2|
|-------|-----|
|00000000 |10000000|
|01111111  |11111111|
| 0-127 | 128-255|

now we have 2 subnets one subnet contains 0-127,other 128-255

# what is networkid and what is broadcat id if we do subnetting?
if u are inside network u know u done subnetting and u tell nid ,bid of subnets only<br>
if u are outside the network nid,bid used as usual frist and last ip.

# subnet mask

32 bit number<br>
series of 1's represents nid&sid<br>
series of 0's represents  host id<br>

subnet mask for the class c network is 255.255.255.0<br>
subnet mask of classc network in binary binary 11111111.11111111.11111111.00000000<br>
now we borrow 1 bit from host id so our new subnet mask contain 11111111.11111111.11111111.10000000 i.e 255.255.255.128<br>
by using incomming packet router has to identify  network to which ip address belongs to<br>
router will take incoming ip and do bitwise and with subnet mask to get nid to which ip belongs to in routing taable.

# Routing table
|nid |subnet mask |interface|
|-|-|-|
|200.0.0.0 |255.255.255.128 |a|
|200.0.0.128| 255.255.255.128 |b|
|0.0.0.0 |0.0.0.0 |c|


