## Storage Area Network (SAN)
- Looks and feels like a local storage device
- Block-level access
- Very efficient reading and writing
Requires a lot of bandwidth
- May use an isolated network and high-speed technology
## Fibre Channel (FC)
A specialized high-speed topology
- Connect servers to storage
- 2,4,8,16 Gbps
-  Support over both fibre and copper
Servers and storage connect to a fibre channel
- Server needs a FC interface
- Storage is commonly referenced by SCSI, SAS, or SATA
## Fibre Channel over Ethernet (FCoE)
Use Fibre Channel over an Ethernet network
- No special networking hardware needed
- Usually integrates with an existing Fibre Channel infrastructure 
- Not routable
## iSCSI
Internet Small Computer System Interface
- Send SCSI commands over an IP network
- Created by IBM and Cisco, now an RFC standard
Makes a remote disk look and operate like a local disk
- Like Fibre Channel
Can be managed quite well in software
- Drivers available for many operating systems
- No proprietary topologies or hardware needed