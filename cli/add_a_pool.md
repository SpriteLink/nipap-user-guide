# Adding a pool
Following the other examples in this chapter, we would add a pool using
the following command:
```
  $ nipap pool add name link-networks \
     description "Link networks for my test network" \
     default-type  assignment \
     ipv4_default_prefix_length 30 \
     ipv6_default_prefix_length 112
```

This allows us to make assignments from this pool automatically.

If you request a prefix from this group you will get:

* a prefix with the type 'assignment'
* a /30 if you requested v4 space
* a /112 if you requested v6 space


