# Adding a VRF

The following adds a VRF with RT 123:456, name "test", description "this is my test VRF" and that has the tags "test", "foo" and "bar".
```
user@host ~ $ nipap vrf add rt 123:456 name test description "this is my test VRF" tags test,foo,bar
Added VRF 'test' [RT: 123:456]
user@host ~ $
```
