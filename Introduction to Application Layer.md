	
## Application Layer Services

A server is making a dns request to get the information about a name like www.cbtnuggets.com UDP is the protocol used which also includes source and destination IP address. It will use a high number port number for the source S: 52,768 and always port D: 53 
UPD - S 54,768 D:53
IP  - S: PC D :8.8.8.8
L2 - S: PC D: S/W

## Email Related Apps

Insecure                                                                       Secure
![[Pasted image 20241024203819.png]]

We need to know the related ports because we want to make sure our network is using the secure ports instead of the older unsecure ones.

## Remote Access

### FUN
GUI
RDP port 3389
VLC
### Boring
CLI
Telnet port 23 (Don't use, it is unsecure)
SSH port 22

## Behind the Scene Services
DHCP - UDP - Client port: 68, Sever port 67 This is to assign an IP to a device
DNS - UDP - port: 53 This is to get an IP from a name like www.google.com
NTP - UDP - port: 123 This is the network time protocol

## File Services
Not Secure
TFTP (Trivial File Transfer Protocol) - UDP port 69 
FTP - TCP port 21 or port 20
Secure
SFTP (Secure File Transfer Protocol) -TCP port 22
SMB (Server Message Block) - TCP port 445,139 UDP 445

## Inf. Services
SNMP (Simple Network Management Protocol) Make sure you are using version 3 port 161 TCP and UDP. Trap on port 162
LDAP (Lightweight Directory Access Protocol) port 389
LDAPS (Lightweight Directory Access Protocol over SSL) port 636 This one is secure
Syslog port 514 +

## Database services
Microsoft SQL Server TCP 1433
Oracle port TCP 1521
MySQL TCP 3306

## Multi-Media + VoIP
H.323 TCP ports 1720,1731
SIP TCP/UDP port 5060, 5061
Zoom A bunch of ports that use other service to make them function
Google Hangouts TCP 80,443,5222,5224,5228,5229
