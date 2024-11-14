## The Ethernet frame
![[Pasted image 20241114164614.png]]
## The MAC address
### Ethernet Media Access Control address
- The "physical" address of a network adapter
- Unique to a device
### 48 bits / 6 byes long
- Display in hexadecimal
- 8c:2d:aa:4b:98:a7
![[Pasted image 20241114164757.png]]
## Duplex
### Half-duplex
- A device cannot send and receive simultaneously
- All LAN hubs are half-duplex devices
- Switch interfaces can be configured as half-duplex
	- But usually only when connecting to other half-duplex device
### Full-duplex
- Data can be sent and received at the same time
- A properly configured switch interface will be set to full-duplex
## CSMA/CD
### CS - Carrier Sense
- Is there a carrier?
- Is there a signal available that we can use to send some data?
### MA - Multiple Access
- More than one device on the network
### CD - Collision Detect
- Collision - Two stations talking at once
- Identify when data gets garbled
### Half-duplex Ethernet
- Not used any longer
### Listen for an opening
- Don't transmit if the network is already busy
### Send a frame of data
- You send data whenever you can 
- There's no queue or prioritization
### If a collision occurs
- Transmit a jam signal to let everyone know a collision has occurred
- Wait a random amount of time
- Retry the transmission
## Full-duplex Ethernet
### Sam's PC creates an Ethernet frame
- Sam's MAC address is the source 
- SGC Server MAC address is the destination
### Frame is sent to Switch A
### Switch A examines the destination MAC address
- Sends frame out the interface that matches the destination MAC
- Device at the other end is Switch B
### Switch B forwards the frame to the interfaces that matches the destination (SGC Server) MAC address
- Destination PC receives the frame, identifies a matching destination MAC
- Destination PC accepts the frame
### Full-duplex
- Send and receive simultaneously

