Another day on Cisco Packet Tracer. This time I designed and secured a simulated enterprise campus network using network technologies.

This lab focused heavily on a small-medium scale enterprise network design, redundancy, segmentation, routing, switching, and security implementation across a multi-department environment.

Network Overview

The topology was designed to simulate a medium-scale enterprise network consisting of:

» Dual Core Switch Architecture
» Multiple Access Switches
» Edge Router Connectivity
» Redundant Layer 2 Links
» Department-based VLAN Segmentation

VLAN Segmentation

The network was segmented into multiple departments using VLANs:

» VLAN 10 — Human Resources
» VLAN 20 — Finance
» VLAN 30 — Operations & Logistics
» VLAN 40 — Facility Manager
» VLAN 50 — IT Department

Technologies & Protocols Implemented

VLANs & Trunking

Configured VLAN segmentation and trunk links between switches to allow inter-switch VLAN communication across the campus network.

EtherChannel (LACP)

Configured EtherChannels between the core switches to provide:

» Link redundancy
» Increased bandwidth

This eliminated single points of failure between the distribution layer devices.

Spanning Tree Protocol (STP)

Optimized STP to prevent switching loops and improve traffic flow by configuring:

» CoreSwitch1 as root bridge for VLANs 10, 30 and 50
» CoreSwitch2 as root bridge for VLANs 1, 20 and 40

This ensured deterministic Layer 2 forwarding paths across the topology.

HSRP (Hot Standby Router Protocol)

Implemented HSRP to provide default gateway redundancy for VLANs.

This allowed hosts to maintain connectivity even if one gateway device failed.

EIGRP

Configured EIGRP for dynamic routing across the enterprise network.

Key concepts implemented included:

» Neighbor adjacency formation
» Route advertisement
» Automatic route learning

NAT & PAT

Configured NAT/PAT on the edge router to allow internal private IP addresses to communicate with external networks using public addressing.

This enabled:

» Internet-style connectivity
» Address conservation

ACLs (Access Control Lists)

Implemented multiple ACL policies to enforce network security requirements.

Security policies configured included:

» Only devices in VLAN 50 (IT Department) are allowed to SSH into network devices across the enterprise.
» End devices in VLANs 10–40 are restricted from SSH access to network infrastructure devices.
» External network devices are blocked from accessing internal enterprise devices.
» Internal devices are permitted to communicate internally and access external networks.

This simulated real-world enterprise administrative access control.

SSH Remote Management

Configured secure remote administration on network devices using SSH with local authentication.

NTP (Network Time Protocol)

Configured NTP to synchronize time across devices for:

» Log consistency
» Monitoring accuracy
» Event correlation

Syslog

Configured centralized logging to improve:

» Troubleshooting
» Event monitoring

This lab brought together several concepts I have been learning individually and integrated them into a single enterprise-style topology with both redundancy and security considerations.

#Cisco #Networking #NetworkSecurity #PacketTracer 