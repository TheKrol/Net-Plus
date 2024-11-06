## 1st video

Break down the components of networking

## 2nd video 

We go to a website, showing what happens behind the scene with the Open system interconnection(OSI ) model

1 Physical - Forwarding of the traffic -send it already

2 Data Link - Different mailboxes We have the address, but need the mailbox it goes to (I would attribute this to the correct device on the network. Your PC instead of your brother's)

3 Network -network address Find the specific location of where we are connecting (Internet Protocol(IP))

4 Transport -Protocols - some protocols care (TCP / 3 way handshake) / some don't (UDP) (make sure data gets there) 

5 Session -Different tab = different sessions - Managing sessions

6 Presentation -Handling the differences between OS - encoding/compression

7 Application -(service/App) Something you want - web browsing/print/files

Please do not throw sausage pizza away / All people seem to need data processing

## 3rd video

We don't use the OSI model in production. TCP/IP protocol suite is what we actually use.

### TCP/IP model (real)
Application (Application, Presentation, Session) -Application Data/Payload
Transport -Segments
Internet (Network) - Packets
Network Access (Data Link, Physical) - Frames / Bits

### Actual
Application (Application, Presentation, Session) -Application Data/Payload
Transport -Segments
Network - Packets
Data Link - Frames
Physical - Bits

## 4th video

### Application protocol
TCP/IP protocol stack
Domain Name Service/System (DNS) Takes the name and figures out the IP address
https://www.google.com  ask DNS for IP - 142.250.189.238
Use wireshark and filter protocol by DNS to show the query to request the IP address

HTTP (web browsing) - HyperText Transfer Protocol --Does encrypt anyone intercepting can see the data

HTTPS(SSL) (web browsing with security) - HyperText Transfer Protocol Secure (Secure Sockets Layer) - Does encrypt data so anyone intercepting cannot see data easily

Transport Layer Security (TLS) - New form of SSL


## 5th video


### Transport protocols
Transmission Control Protocol / User Datagram Protocol (not only protocols, but most used)

TCP makes sure the data goes to the user
UDP does not make sure the data get to the user (DNS is sent through)

Each data request sent is a segment

TCP sends sequence numbers and acknowledgment numbers in the header to keep track the user has received the data 

3-way handshake
Client sends SYN (synchronize) request to the Sever to make sure it wants to engage in a TCP link
Sever sends the SYN request back to Client
Client send an ACK (acknowledgment) segment back to Sever for agreement 

TCP port 80 - HTTP
TCP port 443 - HTTPS
UDP port 53 - DNS

## 6th video

### Network Layer

Address information
Source: 10.1.10.150 and destination address: 8.8.8.8 (Logical addresses)
It adds this information into the header, which then creates the packet
The TCP/IP model works the same for IPv4 and IPv6
Routers are in this layer

## 7th video

### Data Link Layer

Here we are getting the mailbox # which is the Media Access Control (MAC) Address. This address is added on this layer. Address Resolution Protocol which is use to add the MAC address to the packet. 
The device used here is a switch.

## 8th video

### Physical Layer

Data is spit onto the device/network with the network interface card.

When the server receives the packet, it checks each layer to see if it is for them before looking at the data. decapsulates the data layer by layer

When the client sends the data it packs all the data together for the model it encapsulates them into one full packet



