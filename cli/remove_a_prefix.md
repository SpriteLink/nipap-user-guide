# Remove

To remove a prefix:
```
user@host $ nipap address remove 192.0.2.0/24

```

Just as for the modify command, to remove a prefix in a VRF you must also specify the VRF RT:
```
user@host $ nipap address remove 192.0.2.0/24 vrf_rt 123:456
```

Prefixes can be recursively deleted, which means that all prefixes contained within a prefix will be deleted:
```
user@host $ nipap address remove 192.0.2.0/24 recursive
Recursively deleting 192.0.2.0/24 in VRF 'default' [RT: -] will delete the following prefixes:
192.0.2.0/24                  R  None                None           None           My test prefix                          
  192.0.2.0/29                A  None                None           None           My somewhat smaller prefix              
  192.0.2.8/31                A  None                None           None           This was added from a pool              
Do you really want to recursively remove 3 prefixes in VRF 'default' [RT: -]? [y/N]: y
Prefix 192.0.2.0/24 and 2 other prefixes in VRF 'default' [RT: -] removed.
user@host $
```
