# Viewing a pool
To display all information on a pool:
```
user@host $ nipap pool view servers
-- Pool 
  ID                         : 15
  Name                       : test-linknets
  Description                : Link networks for my test network
  Default type               : assignment
  Implied VRF RT / name      : None / default
  Preflen (v4/v6)            : 30 / 112
-- Extra Attributes
-- Tags
-- Statistics
  IPv4 prefixes Used / Free  : 1 / 62 (1.59% of 63)
  IPv6 prefixes Used / Free  : N/A (No IPv6 member prefixes)
  IPv4 addresses Used / Free : 8 / 248 (3.12% of 256)
  IPv6 addresses Used / Free  : N/A (No IPv6 member prefixes)

-- Prefixes in pool - v4: 1  v6: 0
  192.0.2.0/24

user@host $
```
'None' is used to signify that no value has been set. For a more in-depth explanation of statistics, see XXX
