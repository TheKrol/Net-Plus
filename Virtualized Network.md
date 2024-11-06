## 17th video

### Virtual
Hypervisor - allows for some type of virtual machine
VM has everything a regular PC has even if storage is in the cloud. 
Type 1 - hypervisor runs bare metal on the hardware
Type 2 - you can run a VM inside a VM
To allow VM to talk to each other we create a Virtual Network. We create a virtual switch on the hypervisor to allow the VM to talk to each other. 
You can Virtualize a different devices like firewalls and routers(Firewall, Layer 2 switch, Layer 3 Routers)

The one negative is the amount of CPU and RAM that is needed to make sure each one run efficiency.

 \*Which of the following answers refers to a modular network device designed to provide a seamless link between different types of network interfaces?

-    Bridge ( Your answer)
-    Transceiver ( Missed)
## 18th video
### Network Attach Storage

VM needs storage, they make request to the hypervisor to find out where to put the storage. 
1) Local - Direct Attached storage (Not very expandable)
2) Fiber Channel - Storage attached over Fiber (Very Expensive)
3) Fiber Channel over Ethernet - Storage attach over Ethernet (Same as FC just cheaper)
4) iSCSI Sends storage over Ethernet to storage that also speaks iSCSI (You can Virtualize the isCSI adapter) When using a SAN (block based) This is the typical storage

NAS is traditionally file based storage. We read and write by files

## 19th video
### Physical connectivity 

Electric signals over copper
Light signals over fibre

Layer 1

Type 1 Token Ring cable. Shielded cable (Tin foil around with plastic over it)

Ethernet Coax RG-59 You have one wire with T connectors for each PC on each end there is a terminator so the signals don't get bounced around on the network (10BASE2)
If any part of the cable is broken the whole network when down

Layer 1 hub - each port was a repeater we used unshielded twisted pair wires (Ethernet wire). The benefits of this is when one port went down it didn't take down the network.  

Layer 2 Switch - Has the ability to remember port to transfer files faster. Still uses UTP cables

CAT UTP (RJ45)
|CAT|Speed|Frequency|
|5| 100 Mbps| 100 MHz|
|5e |1000 Mbps| 100 MHz|
|6 | 10 Gbps | 250 MHz|
|6a| 10Gbps|500MHz|
|7(shield)|10Gbps|600MHz|
|8(shield)|40Gbps|2GHz|
Max distance is 100 meters to not run into problems with collisions.
If we have to run over 100m we can put a switch in-between to repeat the signal, or use Fiber 

Digital Subscribers Lines (phone wires) (RJ11)

Straight through cable - all pins match 1-1, 2-2, ect...
\*Crossover Cable - Where you cross over every pair of copper table (not included if you only cross over T568A and T568B)
Auto medium dependent interface - Will detect if the cable is crossover or not and will make the signals right. 

## 20th video

### Fiber Optic Cables

Intermediate Distribution Frame (Wiring Closet) Plenum space is between the real ceiling and the drop ceiling. Needs to be less toxic in the case of a fire.

Main Distribution Frame - Main location for the internet, where you get internet from the ISP, router, switches, storage. 

We send between the two with fiber optic cable. 
Multi-Mode - Orange, Aqua - Shorter distance (500m) Transmission of up 2km, less expensive than Single mode, Uses LED as a light source
Single-Mode - Yellow - Longer distance (5000m) Transmission up to 100 km, more expensive, uses laser as a light source 

EMI doesn't interfere with Fiber like it does with UTP. Also harder to ease drop on the signals. 

 \*The shape and angle of the tip of a fiber-optic connector can have an impact on the performance of a fiber-optic communication link. The two basic types of fiber end are Ultra Physical Contact (UPC) and Angled Physical Contact (APC). In the UPC-type connector, the connector end is polished with no angle, while APC connectors feature a fiber end polished at an 8-degree angle, which results in better performance.

-    True ( Missed)
APC like 8 degrees, it is the best, hard to make
UPC is rounded, but better rounded
PC is shit




