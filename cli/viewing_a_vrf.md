# Viewing a VRF

To view a VRF, simply enter its RT;
```
user@host ~ $ nipap vrf view 123:456
-- VRF
  ID                         : 10
  RT                         : 123:456
  Name                       : test-vrf
  Description                : this is my test VRF
-- Extra Attributes
-- Tags
  bar
  foo
  test
-- Statistics
  IPv4 prefixes              : 0
  IPv4 addresses Used / Free : 0 / 0 (0.00% of 0)
  IPv6 prefixes              : 0
  IPv6 addresses Used / Free : 0.0000e+00 / 0.0000e+00 (0.00% of 0.0000e+00)
user@host ~ $
```
