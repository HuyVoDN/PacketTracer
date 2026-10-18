# My interpretation:

My understanding is that each routers must be configured to being able to use the DNS to read hostnames.
Prior to it, the routers could ping each other with just ip addresses.

The DNS server sits at 10.10.10.10/24

Commands to configure: *enable* --> *configure terminal* --> *ip domain-lookup* --> *ip name-server 10.10.10.10*

## How the packets flow in between:

Since before the configuration, R3 will send a DNS request to 10.10.10.10 when you ask for *ping R1*, the packet will travel from R3 to SW2 to R2, then to SW1 and finally reaches the DNS server. 

The DNS server will then send a reply going the same route back to R3 with the ip address for R1 that we originally requested. Once that is established, the ICMP ping will actually be sent out and traverse to R1 from R3.