## LSW7

```shell
sys
sysn ls7

inter vlan 1
ip addr 200.2.2.254 24

quit

router id 2.2.1.7
ospf
area 0
network 200.2.2.254 0.0.0.255
```

## LSW8

```shell
sys
sysn ls8

inter vlan 1
ip addr 200.2.3.254 24

inter g 0/0/4
port link-type access

vlan 2
port g 0/0/4
inter vlan2
ip addr 192.168.0.1 24

quit

router id 2.2.1.8
ospf
area 0
network 192.168.0.1 0.0.0.255
network 200.2.3.254 0.0.0.255
```

## AR17

```shell
sys
sysn rt17

inter g 0/0/0
ip addr 200.2.2.17 24

inter g 0/0/1
ip addr 200.2.3.17 24

inter g 4/0/0
ip addr 200.0.0.233 24

inter loop 0
ip addr 2.1.1.17 32

quit

router id 2.1.1.17
ospf
area 0
network 200.2.2.17 0.0.0.255
network 200.2.3.17 0.0.0.255

quit
quit

bgp 2
group as2 internal
peer 2.1.1.7 group as2
peer 2.1.1.8 group as2
peer 2.1.1.18 group as2
peer as2 connect-interface LoopBack 0
peer 200.0.0.234 as-number 3
```

## AR18

```shell
sys
sysn rt18

inter g 0/0/0
ip addr 200.2.3.18 24

inter g 0/0/1
ip addr 200.2.2.18 24

inter g 4/0/0
ip addr 200.0.0.229 24

inter loop 0
ip addr 2.1.1.18 32

quit

router id 2.1.1.18
ospf
area 0
network 200.2.2.18 0.0.0.255
network 200.2.3.18 0.0.0.255

quit
quit

bgp 2
group as2 internal
peer 2.1.1.7 group as2
peer 2.1.1.8 group as2
peer 2.1.1.17 group as2
peer as2 connect-interface LoopBack 0
peer 200.0.0.230 as-number 3
```
