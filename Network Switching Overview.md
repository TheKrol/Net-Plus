## The switch
### Forward or drop frames
- Based on the destination MAC address
### Gather a constantly updating list of MAC addresses
- Builds the list based on the source MAC address of incoming traffic
### Maintain a loop-free environment
- Using Spanning Tree Protocol (STP)
### Switches examine incoming traffic
- Makes a note of the source MAC address
### Adds unknown MAC address to the MAC address table
- Sets the output interface to the received interface
### The switch doesn't always have a MAC address in the table
### When in doubt, send the frame to everyone
### Determine a MAC address based on an IP address
- You need the hardware address to communicate
### arp -a 
- View local ARP (Address Resolution Protocol) table
## NDP (Neighbor Discovery Protocol)
### No broadcasts!
- Operates using multicast with ICMPv6
### Neighbor MAC Discovery
- Replaces the IPv4 ARP
### SLAAC (Stateless Address Autoconfiguration)
- Automatically configure an IP address without a DHCP server
### DAD (Duplicate Address Detection)
- No duplicate IPs!
### There's no ARP in IPv6
- So how do you find out the MAC address of a device?
### Neighbor Solicitation (NS)
- Sent as a multicast
### Neighbor Advertisement (NA)
![[Pasted image 20241114171848.png]]
## Power over Ethernet (PoE)
### Power provided on an Ethernet cable
- One wire for both network and electricity
- Phones, cameras, wireless access pints
- Useful in difficult-to-power areas
### Power provided at the switch
- Built-in power - Endspans
- In-line power injector - Midspans
### Power modes
- Mode A - Power on the data pairs
- Mode B - Power on the spare pairs
### PoE: IEEE 802.3af-2003
- The original PoE specification
- Now part of the 802.3 standard
- 15.4 watts DC power
- Maximum current of 350 mA
### PoE+: IEE 802.3at-2009
- An updated PoE specification
- Now also part of the 802.3 standard
- 25.5 watts DC power
- Maximum current of 600 mA
