Working with VRFs using the CLI
===============================
The VRF RT is used as the key in most operations meaning that if you want to view, modify or remove a VRF you should specify the VRF RT to uniquely identify the VRF. Use RT '-' to edit VRF "default" (which doesn't have an RT).

Adding a VRF
------------
The following adds a VRF with RT 123:456, name "test", description "this is my test VRF" and that has the tags "test", "foo" and "bar".
```
user@host ~ $ nipap vrf add rt 123:456 name test description "this is my test VRF" tags test,foo,bar
Added VRF 'test' [RT: 123:456]
user@host ~ $
```


Viewing a VRF
-------------
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


Modifying a VRF
---------------
To change an attribute of a VRF, for example changing the name, perform the following;
```
user@host ~ $ nipap vrf modify 123:456 set name test-vrf
VRF 'test-vrf' [RT: 123:456] saved.
user@host ~ $
```
The 'modify' command expects the VRF RT as the first parameter to identify the VRF that should be modified.


Removing a VRF
--------------

