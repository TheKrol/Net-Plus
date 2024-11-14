## Routing tables
### A list of directions for your packets
- A table with many routes to your destination
- Packets stop at every router and ask for directions
### Routing table in routers, workstations, and other devices
- Every device needs directions
## The hop
### A hop
- A packet passes through a router
### The next hop
- The destination address of the next gateway
### A router doesn't need to know how to get everywhere
- It just needs to know how to get out of here
- A default route handles everything not specifically listed
### "Time to live" in IPv4, "hop limit" in IPv6
- Avoids a packet looping forever
## Configuring the next hop
### Every router needs to know where traffic should be sent
- Your packet is always asking for directions
### A router with the incorrect next hop will result in a routing problem 
- Data will go the wrong direction
- A routing loop is easy to create 
	- You'll know quickly if there's a loop
## Default routes
### A route when no other route matches
- The "gateway of last resort"
### A remote site may have only one route
- Go that way -> rest of the world
- Destination of 0.0.0.0/0
### Can dramatically simplify the routing process
- Works in conjunction with all other routing methods
## Routing metrics
### Each routing protocol has its own way of calculating the best route
- i.e., RIPv2, OSPF, EIGRP
### Metric values are assigned by the routing protocol
- RIPv2 metrics aren't useful to OSPF or EIGRP
### Use metrics to choose between redundant link
- Choose the lowest metric, i.e., 1 is better than 2
## Administrative distances
### What if you have two routing protocols, and both know about a route to a subnet?
- Two routing protocols, two completely different metric calculations
- You can't compare metrics across routing protocols
- Which one do you choose?
### Administrative distances
- Used by the router to determine which routing protocol has priority
## Managing network utilization
### Many different devices
- Desktop, laptop, VoIP phone, mobile devices
### Many different applications
- Mission critical applications, streaming video, steaming audio
### Different apps have different network requirements
- Voice is real-time
- Recorded streaming video has a buffer
- Database application is interactive
### Some applications are "more important" than others
- Voice traffic needs to have priority over YouTube
## Traffic shaping
### Traffic shaping, packet shaping
### Control by bandwidth usage or data rates
### Set important applications to have higher priorities than other apps
### Manage the Quality of Service (QoS)
- Routers, switches, firewalls, QoS devices
