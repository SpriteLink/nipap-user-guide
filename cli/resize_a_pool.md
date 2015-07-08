# Resizing a pool, or adding/removing prefixes to the pool
To grow or shrink a poo, you need to add prefixes to it.

The type for the range to add depends on the pools' return-type: If
the pool should return assignments, you need to add a reservation prefix
to the pool; if the pool returns hosts, you need to add either a reservation or assignment to the pool.

```
user@host $ nipap pool resize test-linknets add 192.0.2.0/24
Prefix 192.0.2.0/24 in VRF 'None' [RT: all] added to pool 'test-linknets'.

user@host $
```

You are now able to request prefixes from this pool.


