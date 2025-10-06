At this point, your routers have their basic configurations. The next step is to configure their interfaces. This is because routers are not reachable by end devices until the interfaces are configured. There are many different types of interfaces available on Cisco routers. For example, the Cisco ISR 4321 router is equipped with two Gigabit Ethernet interfaces:

- **GigabitEthernet 0/0/0 (G0/0/0)**
- **GigabitEthernet 0/0/1 (G0/0/1)**

The task to configure a router interface is very similar to a management SVI on a switch. Specifically, it includes issuing the following commands:

```
Router(config)# interface type-and-number    
Router(config-if)# description description-text   
Router(config-if)# ip address  ipv4-address subnet-mask    
Router(config-if)# ipv6 address  ipv6-address/prefix-length    
Router(config-if)# no shutdown
```

