## Network Time Protocol (NTP)
Every device has it own clock including servers, firewalls ect..
Synchronizing the clocks becomes critical
- Log files, authentication information, outage details
Automatic Updates
- No flashing 12:00 lights
Flexible
- You control how clocks are updated
Very accurate
- Accuracy is better than 1 millisecond on a local network

## NTP clients and servers
NTP server listens on udp/123 responds to time requests from NTP clients 
- Does not modify their own time
NTP client
- request time updates from NTP server
NTP client/server
- Will update the other clients
- Will also update their own time
Important to plan your NTP strategy
- Know which devices will be a client or server or both
## NTP Stratum layers
Stratum 0
- Atomic clock, GPS clock
- Very accurate
Stratum 1
- sync to stratum 0 clocks
- Primary time servers
Stratum 2
- sync to stratum 1 clocks

## Configuring NTP
NTP client
- Specify the NTP server address (IP or hostname)
- Use multiple NTP servers (if available) for redundancy
NTP server
- You need at least one clock source
- Specify the stratum level of the clock
- If there's a choice, the lower stratum level wins
