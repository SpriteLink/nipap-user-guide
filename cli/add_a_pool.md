# Adding a pool
Following the other examples in this chapter, we would add a pool using
the following command:
```
  $ nipap pool add name link-networks description "Link networks for my test network" default-type  assignment ipv4_default_prefix_length 30 ipv6_default_prefix_length 112
```

This allows us to make assignments from this pool automatically.

If one requests a prefix from this group, one will get:

* it is of a type 'assignment'
* an ipv4 you get a /30
* an ipv6 you receive a /112


