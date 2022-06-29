# ls4
## common
```
sys
sysn ls4
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
ip addr 200.3.3.4 24
vlan 2
port g 0/0/2
inter vlan 2
ip addr 200.3.5.4 24
vlan 3
port g 0/0/3
inter vlan 3
ip addr 200.3.7.4 24
vlan 4
port g 0/0/4
inter vlan 4
ip addr 200.3.9.4 24
vlan 5
port g 0/0/5
inter vlan 5
ip addr 200.3.10.4 24
vlan 6
port g 0/0/6
inter vlan 6
ip addr 200.3.0.250 30
router id 3.2.1.4
inter loop 1
ip addr 192.168.3.4
ospf
area 0
network 200.3.3.4 0.0.0.255
network 200.3.5.4 0.0.0.255
network 200.3.7.4 0.0.0.255
network 200.3.9.4 0.0.0.255
network 200.3.10.4 0.0.0.255
network 200.3.0.250 0.0.0.3
network 192.168.3.4 0.0.0.0
```