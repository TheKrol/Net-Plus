If DHCP does not work the PC can end up with an APIPA address

## Plan Out

Figure out the scope/pool of address we are going to need. For example, how many PC are we going to have in the office. 10.1.0.101-199. Some vendors only allow you to set up full subnets 10.1.0.0/24 then we have exclusions. 
### Probe
Before it hands out an IP address it tries to ping it. 
### Reservation
We link an IP address to the MAC address.
### Lease
We get to use an IP address for a specific amount of time. If a PC doesn't turn off they will ask for a renew of the lease about half way through the lease. 

A broadcast
Layer 2: Broadcast FFF.FFF.FFF.FFF
Layer 3: Broadcast 255.255.255.255
Layer 4: UDP:67

A offer is sent by the DHCP server. Then the PC will Request to use that IP address. Lastly the DHCP will acknowledge the request. 


### Setting up a DHCP on a Router
We are using a cisco router
IP 10.3.0.3/24
Pool 10.3.0.11-49
G/W 10.3.0.3
DNS 8.8.8.8

We have to set up the full network with a 10.3.0.0/24 Then we exclude from 1-10 and 50-254 so we only have a pool from 11-49. We set up IP for router, then set up IP for DNS.

### DHCP Relay

We are setting up a DHCP pool outside the network for 10.2.0.150-160 with a default gateway 10.2.0.2 and dns of 8.8.8.8. IP helper and UDP forwarding. We set up an IP helper to a different device that did DHCP and it routed it to the destination IP to get DHCP from.



## Notes from Don
DHCP provides IP, DNS, Gateway, NTP, Options for firmware and config for modems, SIP registrations and VoIP. 
A lot of places use Relay/IP helper because it is easier to set up on a single device over everything. 
You don’t want users on the same network as critical servers so you can easily restrict how they talk to those servers.

Putting them on the same broadcast domain is dangerous

Zero trust

Krol 
Is it easier to restrict how you talk to different networks then interal?

Donjuanal
It just shifts where the restriction is placed.
It allows for it to be handled on usually more purpose built or “beefier” hardware
Filtering at a single firewall that controls 20 networks is less work than filtering on every host on that common broadcast domain.

 Can my router do a relay? Like if I wanted to connect to Pipe's DHCP would I be able to do it?
Donjuanal _—_ Today at 10:22 PM
Your router might be able to do relay but no, without a tunnel you wouldn’t be able to reach his relay server
 ISPs will block dhcp ports on the external interfaces of your equipment.