
There are several commands that can be used to verify interface configuration. The most useful of these is the **show ip interface brief** and **show ipv6 interface brief** commands, as shown in the example.

```
R1#  show ip interface brief 
Interface              IP-Address      OK? Method Status                Protocol GigabitEthernet0/0/0   192.168.10.1    YES manual up                    up GigabitEthernet0/0/1   209.165.200.225 YES manual up                    up Vlan1                  unassigned      YES unset  administratively down down 

R1#  show ipv6 interface brief
GigabitEthernet0/0/0      [up/up]    FE80::201:C9FF:FE89:4501    2001:DB8:ACAD:10::1
GigabitEthernet0/0/1      [up/up]    FE80::201:C9FF:FE89:4502    2001:DB8:FEED:224::1

Vlan1                      [administratively down/down]    unassigned 

R1#
```