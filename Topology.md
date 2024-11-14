## 9th video

We are going to talk about topology,
## 10th video

### Topology

Underlay network is the actual path from one device to another. (real interfaces)
From router to service provider
Cable Modem (Coax Cable)
DSL (Phone Cable)
Leased Line
Optical Fiber
Demarcation point - The main plug we get internet from, the barrier between us and the ISP

Overlay is the physical network that we have. (Overhead view)
We put tunnel between two places. (Logical tunnel) Generic Routing encapsulation tunnel

IPsec - Takes every packet and encrypts it before it sends it over.

We can hide IPv6 traffic inside our GRE tunnel so the world will only see IPv4. Need to see the payload to determine if there is IPv6 data.
## 11th video

### More Topology
#### LAN

Cables are 10 base2 200 meters 1 signal. That contains taps to different PC. This is referred as a bus or a collision Domain or broadcast domain. Only one device can talk at a time. (Coaxal Cable) (Logical bus)
Then the hub was created. Basically the same thing, but all the same as the previous (Logica Bus) But it is a physical star (Hub is a center)

Layer 2 switch basically operators at layer 2 (data link - mac address) Can handle more traffic, every port is a collision domain.  Still only 1 broadcast domain through. Physical Star, but also operating as a bus with each device having it's own freeway. 

Ring 4 devices connected in a ring fashion.  Physical Ring and Logical Ring
Token ring with a Multi-station Access Unit which is wired as a physical star
Logical Ring it goes from one device to another then loops arounds. 

#### WAN
Headquarter (Site #1) - Could - Site #2 - Site #3 (Not in the same building)
If Site 2 and Site 3 connect to Site 1 - Hub and Spoke
If Site 2 and Site 3 also connects - Full Mesh
Hybrid - Some with Hub and Spoke Others have a Full Mesh
## 12th video

### Network Types

Could (Don't have to describe what is inside) connected to A and B where A & B is connected as well Peer to Peer Network

Client to server (clearly defined roles)
Server 1 - HTTPS, DNS, Streaming
Client - Consume services 

Personal Area Network
Bluetooth between two devices. 


3 Tier
A  B  C                     D
|    |   |                       |
Access                 Access (Can have a lot of access points) Wireless (SSID)
Distribution     Distribution

Campus Area Network
Covers a small area like a Campus

Metropolitan Area Network
A metro Ethernet network creates a secure, private network within a city using fiber-optic cabling and Ethernet technology. CompTIA refers to this networking technology as metro-optical. The metropolitan area network (MAN) created does not use the Internet to connect and thus doesn’t require security.

Software Design WAN Not free have to pay a vendor. You can roll out configs and software over the network. You can augurate different connections to the internet. 

GRE tunnel can authenticate users and allow users to connect off site. Multipoint GRE tunnel all you to connect to multiple sites with the same config. 

Service Provider Has Layer 3 routers where it forwards traffic by IP traffic
MPLS multi point label switches Instead of using IP address it uses Labels. L3 VPN (label switching) Each router is taking off current label, and adding the new destination one. 
