# Viewing a pool
To display all information on a pool:
```
user@host $ nipap pool view test-linknets
-- Pool 
  ID                         : 16
  Name                       : test-linknets
  Description                : Link networks for my test network
  Default type               : assignment
  Implied VRF RT / name      : None / None
  Preflen (v4/v6)            : 30 / 112
-- Extra Attributes
-- Tags
-- Statistics
  IPv4 prefixes Used / Free  : N/A (No IPv4 member prefixes)
  IPv6 prefixes Used / Free  : N/A (No IPv6 member prefixes)
  IPv4 addresses Used / Free  : N/A (No IPv4 member prefixes)
  IPv6 addresses Used / Free  : N/A (No IPv6 member prefixes)

-- Prefixes in pool - v4: 0  v6: 0

user@host $
```
