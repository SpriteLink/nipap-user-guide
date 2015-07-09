# Modifying a pool
To change a property of a pool later works a lot like changing properties on prefixes. The general invocation is:

  nipap pool modify <name> set <attr> <value> [ attr val ... ]

# Example
```
user@host $ nipap pool modify test-linknets set ipv6_default_prefix_length 110
Pool 'test-linknets' saved.

user@host $
```

