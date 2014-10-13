VRFs
====
VRFs in NIPAP are just like the VRFs in a router - addresses are not allowed to overlap or collide within one VRF but multiple VRFs can be used to describe multiple routing domain with overlapping addresses. Google it if you want to know more ;)

The VRF RT (route-target) is a value used in networks to identify the VRF and must be unique to separate the VRF from other VRFs. In addition, the name is also treated as an identifying attribute and must be unique within NIPAP. NIPAP comes pre-installed with one VRF, called the VRF "default", which doesn't have an RT value. This VRF is usually used to represent the default routing table in a router and typically carries Internet routes, it is however up to the user to define it's use. The VRF "default" can be renamed.

As per RFC4364, the RT value can be in the form of <ASN>:<ID> or <IP>:<ID>.

There are no restrictions on the name attribute but to simplify use in the web-UI and CLI, it is recommended that the name be kept short  using letters or numbers and avoiding spaces and special characters.

Unlike the name attribute, the description attribute should be a text, longer than the name attribute but still brief, describing the use of the VRF.

Tags can be added to a VRF for the purpose of filtering on them when searching.
