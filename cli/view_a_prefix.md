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
  Added                      : 2014-11-10 18:57:43
  Last modified              : 2014-11-10 18:57:43
  Expires                    : -
  Addresses Used / Free      : 0 / 256 (0.00% of 256)
-- Extra Attributes
-- Tags
-- Inherited Tags
-- Comment

user@host $
```
'None' is used to signify that no value has been set. For a more in-depth explanation of statistics, see XXX
