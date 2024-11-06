## 21st video

### IP addressing

It is a lot like street name and house numbers
10th street with 3 building with 101,103,105 house numbers. Therefore, the address would be 101 10th street

If a packet isn't going to your network it must go to the default gateway then to the router or routers to get to the destination 
## 22nd video

### IPv4

net - host
192.168.1.151
255.255.255.0

Made up of 32 bits. Dotted Decimal Each number is made up of 8 bits. 
The Mask determines where the line between net ends and the host begins
The 255 represents the network address. 192.168.1.  |  151
								 255.255.255. | 0 
192.168.1.1 is the end point (default gateway) if a packet needs to go out of network it will travel to here first. 
* A question can be: Do we always use the first 3 numbers for a net address? A: No

Defaults Mask
A: 255.0.0.0   1-127 start of IP would be a class A
B: 255.255.0.0  128-191 start of IP would be a class B
C: 255.255.255.0   192-254 start of IP would be a class C

Classless Inter-Domain Routing (CIDR) notation which is a /24
192.168.1.151/24
10.1.7.1/24

## 23rd video

### IP Address (continue)

Every device on a network needs an IP address 10.1.10.50
Each device needs the correct mask 255.255.255.0
Every device needs to know the default gateway 10.1.10.100
Every device needs to have DNS 8.8.8.8

Dynamic Host Configuration Protocol (DHCP) Automatic get an IP, MASK, gateway and DNS from the gateway. 
DHCP server can be built into a device or a stand alone server. 
Scope or Pool of address for the DHCP to hand out IP address for. 

Devices we don't want to DHCP for, We want the IP to be the same each time. We assign a static IP address to. Reservation for a MAC address to always assign a predefined IP address. 

If a client cannot find a DHCP server will sign Automatic Private Internet Protocol Addressing (169.254.0.0/16).

## 24th video

### IP Packets

Some packets are indented for every, some for a small portion, some for only on device.

Uni-cast - Only goes to one destination

Multi-cast - A packet that is design to go to a multi-cast group. Class D 224.

Broad-cast - ARP An example would be if a device needs to figure out a MAC address of a device. 10.1.10.255 is the broad-cast IP address 255.255.255.255 A router will not forward or route a broadcast to a different network.

Any-cast - More than one destination that has the same IP address. Like Google's DNS. It is routed to the nearest 8.8.8.8 IP address. 

## 25th video

### IP address Private

RFC 1918
Setting assign for specific IP address for corporations(anyone) to use.
A: 10._____
B: 172.16-31.
C: 192.168.

Private > Customer > ISP The private address are not routable over the internet
Network Addresses Translation (NAT) IT takes the private IP and shows as the public IP to make sure we can route over the inter. 

