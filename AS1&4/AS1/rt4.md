# rt4
## common
```
sys
sysn rt4
inter g 0/0/0
ip addr 200.1.2.4 24
inter g 0/0/1
ip addr 200.1.3.4 24
inter g 0/0/2
ip addr 200.0.0.241 30
router id 1.1.1.4
ospf
area 0
network 200.1.2.4 0.0.0.255
network 200.1.3.4 0.0.0.255
```

## bgp
```
quit
quit
bgp 1
group as1 internal
peer 1.1.1.1 group as1
peer 1.1.1.2 group as1
peer 1.1.1.3 group as1
peer 1.1.1.5 group as1
peer as1 connect-interface LoopBack 0
```
