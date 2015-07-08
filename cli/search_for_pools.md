# Search for pools
To display a list of pools you run the following command:

```
user@host $ nipap pool list
Name           # Description                        Default type  4 / 6   Implied VRF
------------------------------------------------------------------------------------------------
test-linknets  - Link networks for my test network  assignment   30 / 112 [RT: -] -

user@host $
```

You can optionally limit the amount of returned pools by supplying an argument. This is parsed as a regular expression:
```
user@host $ nipap pool list test
Name           # Description                        Default type  4 / 6   Implied VRF
------------------------------------------------------------------------------------------------
test-linknets  - Link networks for my test network  assignment   30 / 112 [RT: -] -

user@host $
```


You will get the following error when no matching pool is found:
```
user@host $ nipap pool list nomatch
No matching pools found

user@host $
```
