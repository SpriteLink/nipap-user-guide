# Adding a prefix

Networks or hosts can be added using the CLI.

In its most basic form, the prefix is manually specified along with the required attributes:
```
user@host $ nipap address add prefix 192.0.2.0/24 type reservation description "My test prefix"
Network 192.0.2.0/24 added to VRF 'default' [RT: -]
user@host
```

To simplify adding a prefix, it is possible to instruct NIPAP to add a new prefix by finding the first available one from another, already existing, prefix:
```
user@host $ nipap address add from-prefix 192.0.2.0/24 prefix_length 29 type assignment description "My somewhat smaller prefix"
Network 192.0.2.0/29 added to VRF 'default' [RT: -]
user@host $
```

Similarily, it is possible to add a prefix by finding the first available prefix(es) from a pool:
```
user@host $ nipap address add from-pool link-networks family ipv4 type assignment description "This was added from a pool"
Network 1.3.3.22/31 added to VRF 'default' [RT: -]: This was added from a pool
user@host $
```
