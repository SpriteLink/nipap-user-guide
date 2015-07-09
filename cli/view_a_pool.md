# Viewing a pool
To display all information on a pool:
```
user@host $ nipap pool view test-linknets
-- Pool 
  ID                         : 16
  Name                       : test-linknets
  Description                : Link networks for my test network
  Default type               : assignment
  Implied VRF RT / name      : None / default
  Preflen (v4/v6)            : 30 / 112
-- Extra Attributes
-- Tags
-- Statistics
  IPv4 prefixes Used / Free  : 2 / 61 (3.17% of 63)
  IPv6 prefixes Used / Free  : 1.0000e+00 / 1.8447e+19 (0.00% of 1.8447e+19)
  IPv4 addresses Used / Free : 12 / 244 (4.69% of 256)
  IPv6 addresses Used / Free : 6.5536e+04 / 1.2089e+24 (0.00% of 1.2089e+24)

-- Prefixes in pool - v4: 1  v6: 1
  192.0.2.0/24
  2001:db8:14::/48

user@host $
```
