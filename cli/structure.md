CLI argument structure
======================
Don't let the title intimidate you. This is really about the basics of using the NIPAP CLI.

All commands in the CLI follow a logical pattern. For example;
```
nipap address list FOO
nipap address view 192.0.2.0/24
nipap pool list
nipap vrf add rt 123:456 name test-vrf
```
The first command lists IP addresses matching 'foo'. The second shows a detailed view of the prefix 192.0.2.0/24, the third will list all pools while the last command adds a new VRF. We can see how commands are first grouped into the type of object they deal with, ie 'address', 'pool' or 'vrf', and then followed by the type of action to perform. The most common operations are 'add', 'modify', 'remove', 'view' and 'list' while certain types of objects also support other commands, for example, a pool can be resized and the commands to do that all start with 'nipap pool resize ...'.

If you try to enter any of the above commands you might also notice that the NIPAP CLI comes with tab completion and it does a fairly good job of providing completion help for most commands. If you are unsure about a command, try hitting tab twice to get some suggestions how to move forward.
```
user@host $ nipap pool <tab><tab>
add list modify remove resize view
user@host $ nipap pool 
```

You will see that the command structure is very similar across different types of objects and once you get to know it you will feel quite at home.
