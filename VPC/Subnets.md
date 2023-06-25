# Subnets

Subnets are what services run from inside VPCs, and they’re how we add structure, functionality, and resilience to VPCs.

Subnets inside of VPCs start off entirely private.

A subnet is just a subnetwork of a VPC that resides within a particular AZ. A subnet can never be in multiple availability zones.

A particular AZ, however, can have zero, one, or many subnets.

Subnets are AZ resilient. If an AZ fails, so does the subnet as well as any services that are running only within that one subnet.

The subnet by default uses IPv4 (subset of the VPC CIDR), but it can be configured to use IPv6.

The CIDR that a subnet uses cannot overlap with any other subnets in that VPC.
Subnets can communicate with other subnets in the VPC freely.

There are 5 reserved IP addresses for each subnet:
IP addresses that you cannot use.
- Network address
- Network address + 1 (VPC router)
- Network address + 2 Reserved DNS
- Network address + 3 (Reserved Future Use)
- Last IP in the subnet (Broadcast Address)

The _Dynamic Host Configuration Protocol (DHCP)_ provides a standard for passing configuration information to hosts on a TPC/IP network.
How computing devices receive IP addresses automatically
DHPC is used to dynamically assign an IP address and other network configuration parameters.

In the context of Amazon VPCs, these other parameters may include domain names, DNS servers, or _Network Time Protocol (NTP)_ servers.
