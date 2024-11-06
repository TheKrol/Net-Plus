
# IPV6

Functions the same as IPV4. At the network layer it has mask. It is 128 bits long. We represent it in hex. We use 8 groupings. A:B:C:D:E:F:G:H Each group has 16 bits and there are 4 hex in each group of 4 bits. 2045: -> 0010 for the 2 

This is an example of an IPV6 address.
2045:3421:0A59:0041:0000:0000:104F:7248 Like with IPV4 there is a host and network. We also use a mask, but we only use the / notation so /64 would slip the host and network in half. We still have DNS HTTP and HTTPS (Application) TCP/UDP (Transport)

## Address types

Global Unicast Address This address is routable on the internet.  2xxx - 3xxx is a global ipv6 address. They will also have a link-local address. It is only usable on the exact link that it has. It is used for local communication. It starts with FE80: You can package computers on the multicast address. Those address start with FF02::1 Cast address is FF02::2 -(Router)

## Shorthand

Router 3 (Gi0/1)
2003:0DB8:0002:0011:0000:0000:0000:BEEF/64 You can leave off leading 0 and you can group up groups of four 0 with a double colon. So this is shorting to 2003:DB8:2:11::BEEF/64 It also doesn't matter if upper or lower case. 
## Neighbor Discovery Protocol

Router Solicitations -> FF02::2
RA -> 2003:DB8:3:11:: /64 (ICMP)
NS ->
Neighbor Advertisement ->

## Automatic Address Configuration

SLAAC - Stateless Address Automatic Configuration. It will auto configures the address on the PC. Extended Unique Identifier - 64 It will auto give itself a host address and based on this. IT will use the MAC address + 16 bits and flip the 7th bit. The router will give the device the network address and it will use EUI - 64, and it will double check the host address by sending out a neighbor solicitation to see if anyone is already using the address.

## Transition Techniques

Dual Stack - When you run IPV4 and IPV6 together. Tunneling is used. GRE we create an IPV4 tunnel and then we hide the IPV6 information into the header of an IPV4 packet. When a packet gets sent, when it gets to the other side it will see the header and decapsulate the packet to the correct IPV6. 