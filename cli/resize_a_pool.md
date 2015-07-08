# Resizing a pool, or adding/removing prefixes to the pool
Grow or shrink a pool by adding or removing prefixes to/from it.

Please note that you should not mix the types of the member prefixes of a pool.
For example, if the pools' default-type is host you should add prefixes of type
assignment to the pool.

```
user@host $ nipap pool resize test-linknets add 192.0.2.0/24
Prefix 192.0.2.0/24 in VRF 'None' [RT: all] added to pool 'test-linknets'.
user@host $
```

You are now able to request prefixes from this pool.

You can disassociate a single prefix from a pool with the following command. The prefix will continue to exist.
```
user@host $ nipap pool resize test-linknets remove 192.0.2.0/24
Prefix 192.0.2.0/24 removed from pool 'test-linknets'.
user@host $
```

