<!-- This template removes the micro tutorial for a quicker post and removes images for a full template check out the 000-DAY-ARTICLE-LONG-TEMPLATE.MD-->

**Add a cover photo like:**
![placeholder image](https://via.placeholder.com/1200x600)

# Planing Azure VNets

## Introduction

[2/100] I kicked off the challenge with planning Azure VNets. This is a very good project suggested by @madebygps (Project name: NET01-AZ200 — Plan virtual networks) to get hands on experience on Vnets and subnetting.
Azure VNet, just like a traditional network in a Datacenter, is representation of your own network in the cloud.

## Steps Taken
- Created a VNet with IP address space: 10.0.0.0/27

- Address range: 10.0.0.0 - 10.0.0.31

- Address count: 32

- Created two subnets; subA(10.0.0.0/28) and subB(10.0.0.16/28)

## Cloud Research
- Azure reserves the first four and last IP address for a total of 5 IP addresses within each subnet.
  The first and last IP in each subnet is reserved for the network identification and for broadcast, respectively. 
  Azure also holds 3 additional addresses for internal use starting from the first address in the subnet.
- /27 is known as CIDR notation (Classless Inter domain routing). This represents an IP address and a suffix that indicates network identifier bits in a specified    format
- If you plan to deploy some Azure service resources into a virtual network, they may require, or create, their own subnet, so there must be enough unallocated       space for them to do so.

## Social Proof

[link](link)
