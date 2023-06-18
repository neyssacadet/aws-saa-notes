# VPC Sizing & Structure
A solid infrastructure platform is just as much about a good design, as it is a good technical implementation. For that reason, there are some things we should think about when designing a VPC.

Virtual Private Cloud -> virtual network infrastructure provided by AWS which allows you to create a logically isolated section of the AWS cloud where you can launch AWS resources (your own private network within AWS cloud) 

## VPC Considerations
- Decide IP range (VPC CIDR) in advance 
- What size should the VPC be
- What Networks can’t be used
- The needs of the application today as well as being scalable to accommodate future needs
- Think of VPC structure (Tiers and Resiliency Zones) 

## VPC Structure
Services run from within subnets (which is where IP addresses are allocated from), not directly within the VPC.
Tiers are different types of infrastructure that run from within a VPC.
thout any further information provided, some basic guidelines to structure a VPC would be:

- Start with three subnets, but allow yourself a spare to grow into
- Start with three tiers, and again allow yourself a spare to grow into
