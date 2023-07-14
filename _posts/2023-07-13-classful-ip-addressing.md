---
published: false
---
ip addressing is clasified into two forms<br>
1.classfull addresing<br>
2.classless addressing system<br>

we know ip address is of 32 bits,with 32 bits we will get 2^32 = 4294967296 ip addresses. <br>
we know ip address has two addresses in one address(network address/nid ,host address/hid).<br>
initially they classified it like this<br>
#img<br>
so they divided entire 32 bits into 8 bits for NID,remaining 24 bits for HID<br>
total networks we get 2^8 = 256<br>
Total hosts/network 2^24 = 16777216<br>
256 networks not enough for today,also 16M hosts is very big number,due to this disadvantages classfull addressing come into picture.<br>

# classfull classification
In classfull addressing they divided entire ip address space into 5 classes<br>
CLASS A,CLASS B,CLASS C,CLASS D,CLASS E<br>
let's go through each class<br>

CLASS A<br>

so we have address space 32 bits right range<br>
0.0.0.0 to 255.255.255.255<br>

0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0<br>

if we choose one bit in binary the space is divided into 2 parts<br>

# Binary Division

0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 <br>
<hr>
1 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 <br>

now first bit is choosen adn fixed to zero to divided entire address space into two parts,now we have only 31 bits so total addresses in class a we will get is 2^31.<br>

nid,hid division
8 nid,24 hid 

first octet first bit is set to zero so total networks we will get with remaining 7 bits is 2^7=128(practical number 126)<br>
total hosts/network = 2^24<br>

# Range:
by seeing first octet if first bit is start from 0 in binary we can say it belongs to class a<br>
by examining first octet we can get range<br>

0 0 0 0 0 0 0 0 - 0 <br>

0 0 0 0 0 0 0 1 - 1<br>

0 0 0 0 0 0 1 0 - 2<br>
.<br>
.<br>
.<br>

0 1 1 1 1 1 1 1 - 127<br>

range (0-127)<br>

first network and last network of class a is reseved<br>
practical range can be (1-126)<br>

example ip addresses:1.0.0.0,1.0.0.1,1.0.0.2...........126.255.255.255<br>

this class a ipp addresses used for large networks

# Class  B

from previous binary division we got two parts right,lets take remaining part


1 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 <br>

first bit is already fixed to 1,by dividing space again into 2 parts we get

1 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 <br>
<hr>
1 1 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 <br>

here we take second bit for division again entire address space is divided into 2 parts

here first two bits are fixed and set to 1 0 ,so the address space contain 30 bits only
with 30 bits we will get 2^30 addresses

nid,hid,division
16 nid,16hid

first octet first two bits set to 1 0 with remianing avialble bits in nid is 14 
total networks of class b : 2^14
totals no. of hosts/network: 2^16

# Range:
by seeing first octet if first bit is start from 1 0 in binary we can say it belongs to class b<br>
so by examining first octet we can get range in decimal<br>

1 0  0 0 0 0 0 0 - 128 <br>

1 0 0 0 0 0 0 1 - 129<br>

1 0 0 0 0 0 1 0 - 130<br>
.<br>
.<br>
.<br>

1 0  1 1 1 1 1 1 - 191<br>

range (128-191)<br>


example ip addresses:128.0.0.0,128.0.0.1,...etc

this class b ipp addresses used for medium networks

# class c
lets take remaining half from previous binary division and divide into two halves

1 1 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 <br>
<hr>
1 1 1 0 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 <br>

lets take first half

1 1 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 <br>

for the binary division we took third bit which is set to 0,from prviously got binary number first 2 bits are fixed ,so now we got
110 as prefix which is fixed

first 3 bits are fixed ,remaining bits are 29,with 29 bits we have total addresses 2^29 in class c

nid,hid division
nid 24,hid 8

in network portion total we have 24 bits,but 3 bits are fixed cant change so finally we have 21 bits only.
total networks:2^21
total hosts:2^8

# Range:
by examining first octet we get range


1 1 0 0 0 0 0 0 - 192
1 1 0 0 0 0 0 1 - 193
1 1 0 0 0 0 1 0 - 194
.
.
.
1 1 0 1 1 1 1 1 - 223

range (192-223)

this classc ipp addresses are used for small networks.example home network,small office...etc

class a,b,c are used for hosts

# Class D
we got this below from previous binary divisio

1 1 1 0 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 <br>

divide the above binary data into two parts,by taking 1 bit

1 1 1 0 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 <br>
<hr>
1 1 1 1 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 <br>

nid,hid
there's no nid,hid part in classd,addresses uses as it is as whole

total number of ip addresses we get :2^28

# Range:

1 1 1 0 0 0 0 0 - 224
1 1 1 0 0 0 0 1 - 225
.
.
.
1 1 1 0 1 1 1 1 - 239


used for multicasting

# class E
lets take remainng half from previous binary division

1 1 1 1 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 . 0 0 0 0 0 0 0 0 <br>

nid,hid
there's no nid,hid part in classd,addresses uses as it is as whole

total number of ip addresses we get :2^28

# Range:

1 1 1 1 0 0 0 0 - 240
1 1 1 1 0 0 0 1 - 241
.
.
.
1 1 1 1 1 1 1 1 - 255

range (240-255)

this ip's are reserved















