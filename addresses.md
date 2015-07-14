Addresses, networks, prefixes and hosts
=======================================
Address, network, host, prefix - what's the difference?

An address is simply an IPv4 or IPv6 address, for example 192.0.2.0 or 2001:db8::. A prefix is formed by an address together with a subnet mask, for example 192.0.2.0/24 is our previous IPv4 address, now with a prefix-length of 24 bits. 192.0.2.0/24 is a network but a prefix can also express a single host like 192.0.2.1/32, which can be called "host address", "host prefix", "address" or simply "host".

Prefixes in the form address/prefix-length is called CIDR notation, for example 192.0.2.0/24 which can also be expressed as "network address 192.0.2.0/24 with subnet mask: 255.255.255.0".

NIPAP uses the "prefix" term in most situations to accept both networks and single hosts as input. The various terms are used throughout this book somewhat interchangeably.

NOTE: A loopback IP address is meant as an assignement not a host. Just think that the assignment prefix length should always match up to what you see in your routing table.
