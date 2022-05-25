# rt8
## common
```
sys
sysn rt8
inter g 0/0/0
ip addr 200.3.6.8 24
inter g 0/0/1
ip addr 200.3.7.8 24
inter g 0/0/2
ip addr 200.0.0.238 30
inter l 0
ip addr 3.1.1.8 32
quit
router id 3.1.1.8
ospf
area 0
network 200.3.6.8 0.0.0.255
network 200.3.7.8 0.0.0.255
network 3.1.1.8 0.0.0.0
quit
quit
```

## ibgp
```
bgp 3
group as3 internal
peer 3.1.1.6 group as3
peer 3.1.1.7 group as3
peer as3 connect-interface LoopBack 0
```
