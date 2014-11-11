# Removing a VRF

As always, use the VRF RT as the identifier of the VRF. You will be prompted if you really wish to remove the VRF. Note how removing a VRF will remove all addresses held within that VRF.
```
user@host ~ $ nipap vrf remove 123:456
RT: 123:456
Name: test-vrf
Description: this is my test VRF

WARNING: THIS WILL REMOVE THE VRF INCLUDING ALL ITS ADDRESSES
Do you really want to remove VRF 'test-vrf' [RT: 123:456]? [y/N]: y
VRF 'test-vrf' [RT: 123:456] removed.
user@host ~ $
```
It is not possible to remove VRF "default".
