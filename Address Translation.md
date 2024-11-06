## 26th video

### Network Address Translation

Network Address Translation (NAT) and Port Address Translation (PAT)
RFC 1918 what a company can use for private networking
\10. _______
172.16-31
192.168.
Public internet will not forward any packets in those address range
* NAT we will swap out the IP private address to a IP public address so we can traverse the internet. Router/Proxy Server/Firewall will perform the NAT. 
* If we want to hide/ have the real world know what IP address we are using. 
* Fix: Make two of the same network appear as different networks. So two 10.5.4.0/24 can talk to each other (bi-directional NAT)
#### Static NAT

1:1 mapping. 10.1.10.100 -> 8.8.8.8 need a device to swap out the 10.1.10.100 to a public IP 23.1.2.50. Second PC will map from 10.1.20.101 -> 23.1.2.51 Each internal host gets mapped to it's own induvial IP address. 

#### Dynamic NAT

Will set up a pool of address 23.1.2.55-99 Set up a translation of 1:1 to a pool of public IPs.

Source VS Destination NAT/PAT
The NAT device will translate and then untranslated the IP address. 
Source: We are swapping out the source IP address (initial flow), Destination: we are swapping out the destination IP address (Destination NAT)

### Port Address Translation

Uses a many to one translation (Home Network). Your router only have 23.1.2.11 with 500 clients that need to communicate with the internet. It is up to the NAT device to keep track of each client. Mainly at layer 4 it will keep track at the port number. If the port is the same then it will change the port with a swap as well. Can we static or dynamic as well.

## 27th video

### Source Network Address Translation
![[Pasted image 20241008203335.png]]
Client = internal network 10.1.0.0/24
Lab Internet and Rest of Internet = external network
Server(.100) = DMZ (we place servers here to keep our internal network secure) 172.16.1.0/24

When we swap out the Client IP address that is source NAT and we are going out to the internet. 

## 28th video

Using same Network as previous video

### NAT

We are going to set up a static and dynamic NAT from the client.

The client has a IP of 10.1.0.200/24 -> 23.1.2.200/24. As traffic is sent out it will swap out the source IP, and then when the response comes back the NAT device will swap back the private IP address.
#### Static NAT

We set up a 1:1 NAT in a firewall PA-VM. We do a NAT rule to set it up.  Original Packet is coming from the inside zone and be routed to the outside. We add the source address.
Translated Packet: Translation type is static - address 23.1.2.200. You can also do bi-directional. 

In the firewall we go Monitor -> Session Browser -> Find the packet for our current session. Flow1 show our request sent out
IP 10.1.0.200
Flow2 show our return response
IP 23.1.2.200

#### Dynamic NAT

We are going to set up a dynamic NAT now in the firewall PA-VM. Pool 23.1.2.205-220 for dynamic NAT. Policies -> NAT -> New rule. Original Packet coming from inside to outside. Source Address this time is 10.1.0.0 Therefore, any client coming from that network will be translated.
Translated Packet: Translation Type - Dynamic IP - NAT Pool.
Objects: NAT Pool IP range 23.1.2.205-220

In the firewall we go Monitor -> Session Browser -> Find the packet for our current session. Flow1 show our request sent out
IP 10.1.0.200
Flow2 show our return response
IP 23.1.2.205

Second PC
In the firewall we go Monitor -> Session Browser -> Find the packet for our current session. Flow1 show our request sent out
IP 10.1.0.62
Flow2 show our return response
IP 23.1.2.210

## 29th video

### Port Address Translation

We are very likely using a dynamic PAT instead of static
We are going to set up dynamic PAT,
We go to NAT > Policies > We create a PAT rule if traffic is source from the inside and wants to go out side. We setup the IP address or range we are looking to go outside. We will do source address translation to map it to one IP that we can talk to the internet with. 

We check the traffic logs to verify that our rule is working.
Ping uses ICMP
## 30th video

### Destination NAT
We are swapping out on the initial flow the destination IP address.
If traffic comes in at 23.1.2.100 it is swapped at the NAT device to the internal IP that is the rule is assigned to 172.16.1.100 this is the DMZ address.

## 31st video

### Destination PAT

The incoming traffic will be forward to the internal destination IP, but we will map it up by port. An example, would be a web server and an email server being on the same internal network, we will map port 80 to the web, and port 25. This will allow both to talk to the internet and the right traffic gets to the right server. 