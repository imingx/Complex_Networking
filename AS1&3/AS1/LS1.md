# ls1
## common
```
sys
sysn ls1
inter g 0/0/1
inter vlan 1
ip addr 200.1.2.254 24
router id 1.1.2.1
inter loop 0
ip addr 1.1.2.1 32
ospf
area 0
network 200.1.2.254 0.0.0.255
network 1.1.2.1 0.0.0.0
```

## ibgp
```
bgp 1
group as1 internal
peer 1.1.2.2 group as1
peer 1.1.1.3 group as1
peer 1.1.1.4 group as1
peer 1.1.1.5 group as1
peer as1 connect-interface LoopBack 0
```
