## Virtual LANs
### Virtual Local Area Networks
- A group of devices in the same broadcast domain
- Separated logically instead of physically 
## VLAN trunking
![[Pasted image 20241114172659.png]]
## 802.1Q trunking
![[Pasted image 20241114172821.png]]
## Working with data and voice
### Old school: Connect computer to switch, connect phone to PBX (Private Branch Exchange)
- Two physical cables, two different technologies
### Now: Voice over IP (VoIP)
- Connect all devices to the Ethernet switch
- One network cable for both
### Just one problem...
### Voice and data don't like each other
- Voice is very sensitive to congestion
- Data loves to congest the network
### Put the computer on one VLAN and the phone on another
- But the switch interface is not a trunk
- How does that work?
### Each switch interface has a data VLAN and a voice VLAN
- Configure each of them separately
### Data passes as a normal untagged access VLAN
### Voice is tagged with an 802.1Q header

