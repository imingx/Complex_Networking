# ls3
## common
```
sys
sysn ls3
inter g 0/0/2
port link-type access
inter g 0/0/3
port link-type access
inter g 0/0/4
port link-type access
inter g 0/0/5
port link-type access
inter g 0/0/6
port link-type access
inter vlan 1
ip addr 200.3.2.3 24
vlan 2
port g 0/0/2
inter vlan 2
ip addr 200.3.4.3 24
vlan 3
port g 0/0/3
inter vlan 3
ip addr 200.3.6.3 24
vlan 4
port g 0/0/4
inter vlan 4
ip addr 200.3.8.3 24
vlan 5
port g 0/0/5
inter vlan 5
ip addr 200.3.10.3 24
vlan 6
port g 0/0/6
inter vlan 6
ip addr 200.3.0.249 30
router id 3.2.1.3
ospf
area 0
network 200.3.2.3 0.0.0.255
network 200.3.4.3 0.0.0.255
network 200.3.6.3 0.0.0.255
network 200.3.8.3 0.0.0.255
network 200.3.10.3 0.0.0.255
network 200.3.0.249 0.0.0.3
```