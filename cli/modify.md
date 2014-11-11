# Modifying a prefix

Modifying a prefix works much like adding one through the specification of one or more attributes or their value. The key difference is naturally that the prefix to be modified is first specified:
```
user@host $ nipap address modify 192.0.2.0/24 set description "New description"
```

To modify a prefix in a VRF, also specify the VRF RT:
```
user@host $ nipap address modify 192.0.2.0/24 vrf_rt 123:456 set description "New description"
```
