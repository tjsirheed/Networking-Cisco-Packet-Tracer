# EtherChannels and EIGRP Config

## Objective
This lab focuses on two important enterprise networking concepts: EtherChannel and EIGRP.

## Tools Used
- Cisco Packet Tracer 9.0.0


## Lab Tasks

In the Etherchannel lab, I configured two switches using LACP and PAgP.

EtherChannel is a Layer 2 technology that allows multiple physical Ethernet links to be bundled into a single logical link called a Port-Channel. 

Instead of relying on a single connection between switches, EtherChannel combines interfaces to provide:

» Increased bandwidth

» Link redundancy

» Load balancing

Without EtherChannel, redundant links between switches can cause switching loops and are typically blocked by STP. EtherChannel solves this by allowing multiple links to operate as one logical interface while still preventing loops.

Etherchannel is usually deployed between core-to-distribution switch uplinks.

For this lab, I implemented LACP & PAgP while also verifying the configuration using:

» show etherchannel summary

» show etherchannel port-channel

I also confirmed successful interface bundling into Port-Channel 10.


I also configured EIGRP between routers connected over a serial link and verified neighbor adjacency formation and route exchange.

What I learned about EIGRP:

EIGRP (Enhanced Interior Gateway Routing Protocol) is an advanced distance-vector routing protocol developed by Cisco that combines features of both distance-vector and link-state routing protocols.

Key concepts I learnt here are:

» Neighbor discovery and adjacency formation

» Reliable routing updates using RTP (Reliable Transport Protocol)

» Diffusing Update Algorithm (DUAL) for loop-free path selection

» Feasible Distance (FD) and Reported Distance (RD) metrics

» Successor and feasible successor routes for backup path selection

I configured EIGRP on both routers and set up router authentication and telnet.

Verification commands used:

show ip eigrp neighbors

show ip eigrp interfaces

show ip route

These labs helped me better understand how modern networks achieve redundancy, scalability, bandwidth aggregation, and efficient dynamic routing.
