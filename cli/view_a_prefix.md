# Viewing a prefix
To display all information on a prefix:
```
user@host $ nipap address view 192.0.2.0/24
-- Address 
  Prefix                     : 192.0.2.0/24
  Display prefix             : 192.0.2.0/24
  Type                       : reservation
  Status                     : assigned
  Family                     : IPv4
  VRF                        : None
  Description                : My test prefix
  Node                       : None
  Country                    : None
  Order                      : None
  Customer                   : None
  VLAN                       : None
  Alarm priority             : None
  Monitor                    : False
  Added                      : 2015-07-08 16:30:14
  Last modified              : 2015-07-08 16:30:14
  Expires                    : -
  Addresses Used / Free      : 12 / 244 (4.69% of 256)
-- Extra Attributes
-- Tags
-- Inherited Tags
-- Comment

user@host $
```
'None' is used to signify that no value has been set. For a more in-depth explanation of statistics, see XXX
