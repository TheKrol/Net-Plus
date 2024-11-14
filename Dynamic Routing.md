## Dynamic routing protocols
### Listen for subnet information from other routers
- Sent from router to router
### Provide subnet information to other routers
- Tell other routers what you know
### Determine the best path based on the gathered information
- Every routing protocol has it own way of doing this
### When network changes occur, update the available routes
- Different convergence process for every dynamic routing protocol
## Which routing protocol to use?
### What exactly is a route?
- Is it based on the state of the link?
- Is it based on how far away it is?
### How does the protocol determine the best path?
- Some formula is applied to the criteria to create a metric
- Rank the routers from best to worst
### Recover after a change to the network
- Convergence time can vary widely between routing protocols
### Standard or proprietary protocol?
- OSPF and RIP are standards, some functions of EIGRP are Cisco proprietary
## Distance-vector routing protocols
### Information passed between routers contains network details
- How many "hops" away is another network?
- The deciding "vector" is the "distance"
### Usually automatic
- Relatively little configuration
### Good for smaller networks
- Doesn't scale well to very large networks
### RIP (Routing Information Protocol), EIGRP (Enhanced Interior Gateway Routing Protocol)
## Link-state routing protocols
### Information passed between routers is related to the current connectivity
- If it's up, you can get there.
- If it's down, you can't.
### Consider the speed of the link
- Faster is always better, right?
### Very scalable
- Used most often in large networks
### OSPF (Open Shortest Path First)
- Large, scalable routing protocol
## Hybrid routing protocols
### A little link-state, a little distance-vector
- Not many examples of a hybrid routing protocol
### BGP (Border Gateway Protocol)
- Determines route based on paths, network policies, or configured rule-sets
