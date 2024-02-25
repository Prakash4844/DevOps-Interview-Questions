## Introduction

An RFC1918 address is an IP address that is assigned by an enterprise organization to an internal host. These IP addresses are used in private networks, which are not available, or reachable, from the Internet.

In fact, one of the basic requirements of the Internet is that each host has a unique IP address. RFC1918 removes this requirement. RFC1918 IP addresses can be used on multiple networks, as long as they’re private and isolated from each other. To implement this solution every Internet router must be configured to discard IP packets with these addresses. IP packets carrying private addresses can only flow on internal, private networks. This aspect contributes to network security by creating a clear distinction between internal and external networks. Devices with private addresses are not directly reachable from the Internet, which adds a layer of isolation and protection against certain types of cyber threats.

## RFC1918 Motivations

This RFC was drafted in 1996 when it became clear to Internet operators that the IPv4 address space, consisting of 4,294,967,296 unique addresses, was not sufficient to address every single computer in the world. By that time, the Internet was rapidly growing beyond initial expectations. Soon, no IPv4 addresses would be available to use, limiting the Internet’s growth. As a solution, RFC1918 was drafted to enable private organizations to use these addresses internally. Organizations can use private addresses without asking permission to the Internet Assigned Numbers Authority (IANA), which governs the IP addresses assignment. 

The only drawback of RFC1918 is that computers configured with private addresses cannot be reached from the Internet. With this new standard, computers were basically divided between public and private hosts. Hosts configured with private addresses are basically “clients”: they can connect to Internet servers, or other internal hosts, but can’t be reached from the Internet.

## RFC1918 Subnets

The RFC1918 address space includes the following networks:

    10.0.0.0 – 10.255.255.255  (10/8 prefix)
    172.16.0.0 – 172.31.255.255  (172.16/12 prefix)
    192.168.0.0 – 192.168.255.255 (192.168/16 prefix)

The ten-dot network (10/8) is typically used within large organizations that have thousands of hosts. The 172 and 192 subnets are more common within smaller organizations or home networks. If you are reading this article from home, most probably, your laptop is configured via DHCP with a 192 address. 

## NAT, Network Address Translation

Network Address Translation (NAT) is a technology that makes RFC1918 a feasible solution to the IPv4 address exhaustion problem. NAT enables an internal host to communicate with an Internet server. A NAT device, generally a network router or a firewall, sits between the Internet and a private network. The Internet interface is configured with a public IP address while the private interface is connected to the internal network and configured with an RFC1918 address.

When the NAT device receives a packet from an internal host, it rewrites the packet using its own public IP address as source before sending it to the Internet. This process is also called “masquerading” because it seems as if the conversation was (falsely) originated by the NAT device itself. By allowing many devices to share a small set of public IP addresses, the implementation of RFC1918 and NAT alleviated the pressure on the dwindling pool of globally unique IPv4 addresses. Some applications and protocols might require adjustments to function properly in environments with RFC1918 addresses and NAT. This is particularly relevant when dealing with real-time communication, peer-to-peer connections, and certain gaming applications.

## Beyond RFC1918, IPv6

IPv6 is the new addressing scheme that provides 3.4×1038 unique addresses. Many networks are now assigning IPv6 addresses to their hosts in parallel with IPv4, a configuration that is often referred to as dual stack. Adoption of IPv6 is slowly moving forward, so it’s safe to expect that RFC1918 addresses are here to stay for quite some time.