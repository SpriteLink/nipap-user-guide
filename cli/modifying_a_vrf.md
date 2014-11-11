# Modifying a VRF

To change an attribute of a VRF, for example changing the name, perform the following;
```
user@host ~ $ nipap vrf modify 123:456 set name test-vrf
VRF 'test-vrf' [RT: 123:456] saved.
user@host ~ $
```
The 'modify' command expects the VRF RT as the first parameter to identify the VRF that should be modified.
