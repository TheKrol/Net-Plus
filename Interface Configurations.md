## Basic interface configuration
### Speed and duplex
- Speed: 10 / 100/ 1,000 / 10 Gig
- Duplex: Half/Full
- Automatic and manual
- Needs to match on both sides
### IP address management
- Layer 3 interfaces
- VLAN interfaces
- Management interfaces
- IP address, subnet mask/ CIDR block, default gateway, DNS (optional)
## VLANs
### VLAN assignment
- Each device port should be assigned a VLAN
### Trunking
- Connecting switch together
- Multiple VLANs in a single link
### Tagged and untagged VLANs
- A non-tagged frame is on the default VLAN
	- Also called the native VLAN
- Trunk ports will tag the outgoing frames
	- And remove the tag on incoming frames
## LAG and mirroring
### Port bonding / Link aggregation (LAG)
- Multiple interfaces acts like one big interface
- LACP (Link Aggregation Control Protocol)
	- Adds additional automation and management
### Port mirroring
- Copy traffic from one interface
- Used for packet captures, IDS
- Mirror traffic on the same switch
- Mirror traffic from one switch to another
### Examine a copy of the traffic
- Port mirror (SPAN), network tap
## Jumbo frames
### Ethernet frames with more than 1,500 bytes of payload
- Up to 9,216 bytes (9,000 is the accepted norm)
### Increases transfer efficiency
- Per-packet size
- Fewer packets to switch/route
### Ethernet devices must support jumbo frames
- Switches, interface cards
- Not all devices are compatible with others
## Ethernet flow control
### Ethernet is non-deterministic
- You never know just how fast or slow traffic will flow
### If things get busy, tell the other device to slow down
- Switches only have so much buffer
### One popular flow control method is IEEE 802.3X
- The "pause" frame
### Enhancements have been made through the years
- Incorporates CoS (Class of Service)
## Port security
### Prevent unauthorized users from connecting to a switch interface
- Alert of disable the port
### Based on the source MAC address
- Even if forwarded from elsewhere
### Each port has its own config
- Unique rules for every interface
## Port security operation
### Configure a maximum number of source MAC addresses on an interface
- You decide how many is too many
- You can also configure specific MAC addresses
### The switch monitors the number of unique MAC addresses
- Maintains a list of every source MAC address
### Once you exceed the maximum, port security activates
- Default is to disable the interface
