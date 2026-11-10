09/11/2026

Mission 01

Reserved IP	Purpose
10.0.1.0	Network address
10.0.1.1	VPC router
10.0.1.2	Reserved by AWS (DNS-related reservation)
10.0.1.3	Reserved for future use
10.0.1.255	Broadcast address


These are the three official private IPv4 ranges
Private range	CIDR
10.0.0.0 – 10.255.255.255	/8
172.16.0.0 – 172.31.255.255	/12
192.168.0.0 – 192.168.255.255	/16


However, there are other special IPv4 ranges, such as: 
127.0.0.0/8 → Loopback (localhost).
169.254.0.0/16 → Link-local addresses.
100.64.0.0/10 → Shared addresses, commonly used for Carrier-Grade NAT.


CIDR: Classless Inter-Domain Routing
It's a method for defining IP address ranges and routing networks.
Size	CIDR	Total IP addresses
Smallest	/28	16
Largest	/16	65,536



Mission 02

AWS uses a rule called Longest Prefix Match: when multiple routes match an IP address, AWS chooses the one with the largest prefix lenght (/16 instead of /0)

A public subnet is a subnet whose associated route table contains a route to an Internet Gateway. To actually communicate with the internet over IPv4, an EC2 instance also needs a public IPv4 address and appropriate security rules.



Mission 03


