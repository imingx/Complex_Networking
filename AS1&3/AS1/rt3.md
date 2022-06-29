# rt3
## common
```
sys
sysn rt3
inter g 0/0/0
ip addr 200.1.2.3 24
inter g 0/0/1
ip addr 200.1.3.3 24
inter g 0/0/2
ip addr 200.0.0.245 30
inter loop 0
ip addr 1.1.1.3 32
inter loop 1
ip addr 192.168.1.2 32
quit
router id 1.1.1.3
ospf
area 0
network 200.1.2.3 0.0.0.255
network 200.1.3.3 0.0.0.255
network 1.1.1.3 0.0.0.0
network 192.168.1.3 0.0.0.0
import-route bgp
quit
quit
```

## ibgp
```
bgp 1
group as1 internal
peer 1.1.1.1 group as1
peer 1.1.1.2 group as1
peer 1.1.1.4 group as1
peer 1.1.1.5 group as1
peer as1 connect-interface LoopBack 0
```

## ebgp
```
peer 200.0.0.246 as-number 3
network 172.16.1.2 24
```