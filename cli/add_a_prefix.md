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

## Examples

### dual-stack allocation
When adding from a pool it is possible to get both an IPv4 and IPv6 prefix at the same time. Use the same syntax as for adding a single prefix but instead of specifying family 4 or 6, you specify family dual-stack:
```
user@host $ nipap address add from-pool link-networks family dual-stack type assignment description "This was added from a pool"
Network 1.3.3.22/31 added to VRF 'default' [RT: -]: This was added from a pool
Network 2001:db8::14/64 added to VRF 'default' [RT: -]: This was added from a pool
user@host $
```
When using dual-stack it is not possible to manually specify the prefix length. The pool's default prefix length for respective address family will be used.

Also note that using family dual-stack does not result in one atomic operation - there are two requests to the backend. This means that if one request fails, for example due to shortage of addresses, the other one might succeed. It is up to the user to handle this.  


