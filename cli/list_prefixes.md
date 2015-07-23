# List prefixes or addresses

You can list with the cli:

```
user@host $ nipap address list
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

## Custom columns
Per default the CLI will show a standard selection of columns. It is possible
to customize the selection of columns through the --columns option, which takes
a comma separated list of column names as input. Precede the list with '+' to
append to the default selection of columns instead of replacing it.

Specify complete selection of columns:
```
user@host $ nipap address list --columns vrf_rt,prefix,description,total_addresses,used_addresses,free_addresses
Searching for prefixes in any VRF...
VRF RT  Prefix                              Description  Total addresses       Used addresses  Free addresses
=====================================================================================================================
-       1.0.0.0/8                           foo          16777216              8388608         8388608
-         1.0.0.0/9                         foo          8388608               4194304         4194304
-           1.0.0.0/10                      foo          4194304               2097152         2097152
-             1.0.0.0/11                    foo          2097152               1048576         1048576
-               1.0.0.0/12                  foo          1048576               384             1048192
-                 1.0.0.128/25              kaka         128                   0               128
-                 1.3.3.0/24                foo          256                   0               256
-       2001:db8:1:1::/64                   kaka         18446744073709551616  0               18446744073709551616
```

Append vlan to the selection of columns:
```
user@host $ nipap address list --columns +vlan
Searching for prefixes in any VRF...
VRF RT  Prefix                                 #   Node  Order ID  Customer ID  Description  VLAN
===================================================================================================
-       1.0.0.0/8                           R  -   None  None      None         foo          None
-         1.0.0.0/9                         R  -   None  None      None         foo          None
-           1.0.0.0/10                      R  -   None  None      None         foo          None
-             1.0.0.0/11                    R  -   None  None      None         foo          None
-               1.0.0.0/12                  R  -   None  None      None         foo          None
-                 1.0.0.128/25              A  -   None  None      None         kaka         None
-                 1.3.3.0/24                R  #3  None  None      None         foo          1
-       2001:db8:1:1::/64                   R  -   None  None      None         kaka         None
user@host $
```

If you wish to make your column selection slightly more permanent you can add
the 'prefix_list_columns' option to your .nipaprc file. It is still possible to
override the selection on the command line.
