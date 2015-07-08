# Adding a pool

Add a pool with the 'nipap pool add' command followed by the arguments for creating a pool:
```
user@host $ nipap pool add name link-networks \
     description "Link networks for my test network" \
     default-type  assignment \
     ipv4_default_prefix_length 30 \
     ipv6_default_prefix_length 112
Pool 'link-networks' created.

user@host $
```

This allows us to make assignments from this pool automatically.

If you request a prefix from this pool you will get:

* a prefix with the type 'assignment'
* a /30 if you requested an IPv4 prefix
* a /112 if you requested an IPv6 prefix


