## VoIP phone
### Voice over internet Protocol
- Instead of analog phone line or the Plain Old Telephone Services (POTS)
### A relatively complex embedded system
- Can be an important resource
### Each device is a computer
- Separate boot process and network connection
- Individual configurations
- Different capabilities and functionalities
## Printer
### Color and B&W output
- Paper documents
- Photos
### All-in-one - AIO
- Printers, scanners, copier, fax
### Connectivity
- Ethernet
- 802.11 Wireless
- USB
- Bluetooth / Infrared
## Access control devices
### Card reader
- Access with a smart card
### Biometric authentication
- Fingerprint, retina, voiceprint
### Usually stores a mathematical representation of your biometric
- Your actual fingerprint isn't usually saved
### Ethernet connected
- IP address configured static or DHCP
## Cameras
### CCTV (Closed circuit television)
- Can replace physical guards
### Camera features are important
- Motion recognition can alarm and alert when something moves
- Object detection can identify a license plate or person's face
### Often many different cameras
- Networked together and recorded over time
## Surveillance systems
### Video/audio surveillance
- Embedded systems in the cameras and the monitoring stations
### IP addressable
- Multicast video
- High definition
## HVAC
### Heating, Ventilation, and Air Conditioning
- Thermodynamics, fluid mechanics, and heat transfer
### A complex science
- Not something you can properly design yourself
- Must be integrated into the fire system
### PC manages equipment
- Makes cooling and heating decisions for workspaces and data centers
- Network connectivity is critical
## IoT (Internet of Things) devices
### Appliances
- Refrigerators
### Smart Devices
- Smart speakers respond to voice commands
### Air control
- Thermostats, temperature control
### Access 
- Smart doorbells
### May require a segmented network
- Limit any security breaches
## SCADA / ICS
### Supervisory Control and Data Acquisition System
- Large-scale, multi-site Industrial Control Systems (ICS)
### PC manages equipment
- Power generation, refining, manufacturing equipment
- Facilities, industrial, energy, logistics
### Distributed control systems
- Real-time information
- System control
### Requires extensive segmentation
- No access from the outside
## Hub
### Multi-port repeater
- Traffic going in one port is repeated to every other port
- OSI Layer 1
### Everything is half-duplex
- Can only send or receive data. Not do both
### Becomes less efficient as network traffic increases
### 10 megabit / 100 megabit
### Difficult to find today
## Bridge
### Imagine a switch with two to four ports
- Makes forwarding decisions in software
### Connects different physical networks
- Can connect different topologies
- Gets around physical network size limitations / collisions
### OSI Layer 2 device
- Distributes traffic based on MAC address
### An example of a modern bridge is a wireless access point
- Bridges wired Ethernet to wireless
## Switch
### Bridging done in hardware
- Application-specific integrated circuit (ASIC)
### An OSI layer 2 device
- Forwards traffic based on data link address
### Many ports and features
- The core of an enterprise network
- May provide Power over Ethernet (PoE)
### Multilayer switch
- Includes Layer 3 (routing) functionality
## Router
### Routes traffic between IP subnets
- OSI layer 3 device
- Routers inside of switches sometimes called "layer 3 switches"
- Layer 2 = Switch
- layer 3 = Router
### Often connects diverse network types
- LAN, WANT, copper, fiber
## Access point
### Not a wireless router
- A wireless router is a router and an access point in a single device
### An access pint is a bridge
- Extends the wired network onto the wireless network
- OSI layer 2 device
## Cable modem
### Broadband
- Transmission across multiple frequencies
- Different traffic types
### Data on the "cable" network
- DOCSIS (Data Over Cable Service Interface Specification)
### High-speed networking
- 4 Mbits/s through 250 Mbits/s are common
- Gigabit speeds are possible
### Multiple services
- Data, voice, video
## DSL modem
### ADSL (Asymmetric Digital Subscriber Line)
- Uses telephone lines
### Download speed is faster than the upload speed (asymmetric)
- ~10,000 foot limitation from the central office (CO)
- 52 Mbit/s downstream / 16 Mbit/s upstream are common
- Faster speeds may be possible if closer to the CO
## Repeater
### Receive signal, regenerate, resend
- No forwarding decisions to make
### Common use
- Boost copper or fiber connections
- Convert one network media to another
- Extend wireless network reach
## Converting media
### OSI Layer 1
- Physical layer signal conversion
### Extend a copper wire over a long distance
- Convert it to fiber, and back again
### You have fiber
- The switch only has copper ports
### Almost always powered
- Especially fiber to copper
## Layer 3 capable switch
### A switch (Layer 2) and router (Layer 3) in the same physical device
- Layer 3 switch
- Layer 2 router?
### Switching still operates at OSI Layer 2 routing still operates at OSI Layer 3
- There's nothing new or special happening here
## Wireless networks everywhere
### Wireless networking is pervasive
- And you probably don't just have a single access point
### Your access points may not even be in the same building
- One (or more) at every remote site
### Configurations may change at any moment
- Access policy, security policies, AP configs
### The network should be invisible to your users
- Seamless network access, regardless of role
## Wireless LAN controllers
### Centralized management of access points
- A single "pane of glass"
### Deploy new access points
### Performance and security monitoring
### Configure and deploy changes to all sites
### Report on access point use
### Usually a proprietary system
- The wireless controller is paired with the access points
## Balancing the load
### Distribute the load
- Multiple servers
- Invisible to the end-user
### Large-scale implementations
- Web server farms, database farms
### Fault tolerance
- Server outages have no effect
- Very fast convergence
## Load balancer

![[Pasted image 20241114134646.png]]
## IDS and IPS
### Intrusion Detection System / Intrusion Prevention System
- Watch network traffic
### Intrusions
- Exploits against operating systems, applications, etc.
- Buffer overflows, cross-site scripting, other vulnerabilities
### Detection vs. Prevention
- Detection - Alarm or alert
## Proxies
### Sits between the users and the external network
### Receives the user requests and sends the request on their behalf (the proxy)
### Useful for caching information, access control, URL filtering, content scanning
### Applications may need to know how to user the proxy (explicit)
### Some proxies are invisible (transparent)
## Application proxies
### Most proxies in use are application proxies
- The proxy understands the way the application works
### A proxy may only know one application
- HTTP
### Many proxies are multipurposed proxies
- HTTP, HTTPS, FTP, ect.
## VPN concentrator
### Virtual Private Network
- Encrypted (private) data traversing a public network
### Concentrator / head-end
- Encryption/decryption access device
- Often integrated into a firewall
### Many deployment options
- Specialized cryptographic hardware
- Software-based options available
### Used with client software
- Sometimes built into the OS
## VoIP technologies
### PBX (Private Branch Exchange)
- The "phone switch"
- Connects to phone provider network
- Analog telephone lines to each desk 
### VoIP PBX
- Integrate VoIP devices with a corporate phone switch
### Voice gateway
- Convert between VoIP protocols and traditional PSTN protocols
- Often built-in to the VoIP PBX
## Network-based firewalls
### Filter traffic by port number or application
- Traditional vs. NGFW (Next Generation Firewalls)
### Encrypt traffic
- VPN between sites
### Most firewalls can be layer 3 devices (routers)
- Often sits on the ingress/egress of the network
- Network Address Translation (NAT)
- Dynamic routing