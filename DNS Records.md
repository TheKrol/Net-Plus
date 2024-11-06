Resource Records (RR)
- Database records of domain name services
There are over 30 different DNS
- IP address, certificates, host alias names, ect...

## Start of Authority (SOA)
This is part of the config file that describes the DNS zone details
Structure
- IN SOA (Internet zone, Start of Authority)
- Serial number
- Refresh, retry and expiry timeframes
- Caching duration/TTL (Time to Live)

## Address records (A IPv4) (AAAA IPv6)
Defines the IP address of a host
- Most popular
A record are for IPv4 address
- Modify the A record to change the host name to IP address resolution
AAAA record are for IPv6 address
- Same DNS server, different records

## Canonical name records (CNAME)
A name is an alias of another, canonical name
- One physical server, multiple services
Can create an Alias for things like chat, ftp, www
## Service records (SRV)
Find a specific service
- Windows Domain Controller?
- Instance Messaging Service?
- Where is the VoIP controller?

## Mail exchanger record (MX)
Determines the host name for the mail server
- This isn't an IP address; it is a name

## Name server records (NS)
List the name servers for a domain
-NS records point to the name of the server

## Pointer record (PTR)
The reverse of an A or AAAA record
- Added to a reverse map zone file

## Text records (TXT)
Human readable text information
- Useful public information
SPF protocol (Sender Policy Framework)
- Prevent mail spoofing
- Mail servers check that incoming mail come from an authorize one.
DKIM (Domain Keys Identify Mail)
- Digitally sign your outgoing mail
- Validated by the mail server, not usually seen by end user
- Put your public key in the DKIM TXT record

## Zone transfers
Replicate a DNS database
- The primary DNS sever has the primary copy of the zone information
Synchronize to a secondary server
- Provide redundancy
Triggered by referencing the serial number
- If the serial number increases, there must have been a change
Full zone transfers can be a security risk
- Attackers can use the data as reconnaissance