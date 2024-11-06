## Three-tier architecture
Core
- The center of the network
- Web servers, databases, application
- Many people need access to this
Distribution
- A midpoint between the core and the users
- Manage path between end users and the core
Access
- Where the users connect
- End stations, printers

## SDN (Software Defined Networking)
Networking devices have different function planes of operations
- Data, control, and management planes
Split the functions into separate logical units
- Extend the functionality and management of a single device
- Perfectly built for the cloud
### Infrastructure layer / Data plan
- Process the network frames and packets
- Forwarding, trunking, encrypting, NAT
### Control Layer / Control Plane
- Routing tables, session tables, NAT tables
- Manages the actions of the data play
- Dynamic routing protocol updates
### Application layer / Management
- Where the network managers controls all the controls 
- SSH, SNMP, API

## Spine and leaf architecture
Each leaf switch connects to each spin switch
Leaf switches do not connect to each other
Top of rack switching
- Each leaf is on the "top" of a physical network rack
Advantages
- Simple cabling
- Redundant
- Fast
Disadvantages
- Additional switches may be costly

## Traffic flows
Important to know where traffic starts and ends
East-west
- Traffic between devices in the same data center
- Relatively fast response times
North-south
- Ingress/egress to an outside device
- A different security posture than east-west

## Network locations
Branch office
- A remote location
- Client Devices, printers, switch/router/firewall
On-premises data center
- Technology is located in-house
- Requires power, cooling, and ongoing monitoring
Colocation
- Share a data center with others
- Local oversight and monitoring


