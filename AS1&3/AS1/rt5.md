# rt5
## common
```
sys
sysn rt5
inter g 0/0/0
ip addr 200.1.2.5 24
inter g 0/0/1
ip addr 200.1.3.5 24
inter g 0/0/2
ip addr 200.0.0.237 30
inter loop 0
ip addr 1.1.1.5 32
quit
router id 1.1.1.5
ospf
area 0
network 200.1.2.5 0.0.0.255
network 200.1.3.5 0.0.0.255
peer 200.0.0.238 as-number 3
quit
quit
```

## ibgp
```
bgp 1
group as1 internal
peer 1.1.1.1 group as1
peer 1.1.1.2 group as1
peer 1.1.1.3 group as1
peer 1.1.1.4 group as1
peer as1 connect-interface LoopBack 0
```
