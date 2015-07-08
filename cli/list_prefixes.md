# List prefixes or addresses

You can list with the cli:

```
user@host $ nipap address list
Searching for prefixes in any VRF...
Searching for prefixes in any VRF...
VRF  Prefix              #  Node       Order     Customer  Description
====================================================================================================================
-    192.0.2.0/24      R -  None       None      None      My test prefix
-    192.0.2.0/29      A -  None       None      None      My somewhat smaller prefix
-    192.0.2.8/30      A -  None       None      None      This was added with the dualstacked option
-    2001:db8:14::/48  R -  None       None      None      My test v6 prefix
-    2001:db8:14::/112 A -  None       None      None      This was added with the dualstacked option

user@host $
```

