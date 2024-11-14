## Designing the Cloud
### On-demand Computing power
- Click a button
### Elasticity
- Scale up or down as needed
### Applications also scale
- Scalability for large implementations
- Access from anywhere
### Multitenancy
- Many different clients are using the same cloud infrastructure

## Infrastructure as code
### Describe an infrastructure
- Define servers, network, and applications as code
### Modify the infrastructure and create versions
- The same way you version application code
### Use the description (code) to build other applications instances
- Build it the same way every time based on the code
### An important concept for cloud computing
- Build a perfect version every time
## Orchestration
### Automation is the key to cloud computing
- Services appear and disappear automatically, or at the push of a button
### Entire applications instances can be instantly provisioned
- All servers, networks, switches, firewalls, and policies
### Instances can move around the world as needed
- Follow the sun
### The security policies should be part of the orchestration
- As applications are provisioned, the proper security is automatically included
## Connecting to the cloud
### VPN
- Site-to-site virtual private network
- Encrypt through the internet
### Virtual Private Cloud Gateway
- Connects users on the internet
### VPC Endpoint
- Direct connection between cloud providers networks
## Virtual Private cloud endpoints

![[Pasted image 20241114130221.png]]

## VM sprawl avoidance
### Click a button
- You've built a server
- Or multiple servers, networks, and firewalls
### It becomes almost too easy to build instances
- This can get out of hand very quickly
### The virtual machines are sprawled everywhere
- You aren't sure which VMs are related to which applications
- It becomes extremely difficult to deprovision
### Formal process and detailed documentation
- You should have information on every virtual object
## VM escape protection
### The virtual machine is self-contained
- There's no way out
- Or is there?
### Virtual machine escape
- Break out of the VM and interact with the host operating system or hardware
### Once you escape the VM, you have great control
- Control the host and control other guest VMs
### This would be a huge exploit
- Full control of the virtual world

- 