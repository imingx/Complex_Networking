# rt7
## common
```
sys
sysn rt7
inter g 0/0/0
ip addr 200.3.4.7 24
inter g 0/0/1
ip addr 200.3.5.7 24
inter g 0/0/2
ip addr 200.0.0.242 30
inter l 0
ip addr 3.1.1.7 32
quit
router id 3.1.1.7
ospf
area 0
network 200.3.4.7 0.0.0.255
network 200.3.5.7 0.0.0.255
network 3.1.1.7 0.0.0.0
quit
quit
```

## ibgp
```
bgp 3
group as3 internal
peer 3.1.1.6 group as3
peer 3.1.1.8 group as3
peer as3 connect-interface LoopBack 0
```

## ebgp
```
peer 200.0.0.241 as-number 1
```
