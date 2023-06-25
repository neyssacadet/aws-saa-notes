# Routing & Internet Gateways
VOC Router --> highly available device which is present in every VPC (both default or custom). 

## Routing

Every VPC has a VPC Router. The VPC Router’s job is route traffic between subnets. It takes instructions from the route tables inside of each subnet.

Route tables are attached to 0 or more subnets. A subnet always has a route table.

That route table, however, has the potential to either be a custom route table we’ve configured or the default/main route table of the VPC.

Inside of route tables, the higher the prefix, the more specific, the higher the priority. The one exception to this is that local routes always take priority over external routes.

## Internet Gateways

The _Internet Gateway (IGW)_ is a region resilient gateway that can be attached to a VPC. One IGW can cover all of the availability zones in the region the VPC uses.

A VPC can have 0 or 1 IGWs, likewise an IGW can have 0 or 1 VPCs.

IGWs run from within the AWS Public Zone and they route traffic between the VPC and the Internet or the AWS Public Zone.(AWS services)
Performance Managed by AWS 

IPv4 not configured in the OS with a public address

## Bastion Hosts/ Jumpbox
Instance in a public subnet for incoming management connections that arrive in VPC then they access internal VPC resources. For private VPC. Then access internal VPC resources. The only entrypoint to a highly secure VPC.
