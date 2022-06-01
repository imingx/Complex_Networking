## AR19

```shell
sys
sysn r19

inter g 4/0/0
ip addr 200.0.0.234 24

inter g 0/0/1
ip addr 200.4.3.19 24

inter g 0/0/0
ip addr 200.4.2.19 24

inter loop 0
ip addr 4.1.1.19 32

quit

router id 4.1.1.19
ospf
area 0
network 200.4.2.19 0.0.0.255
network 200.4.3.19 0.0.0.255

quit
quit

bgp 4
group as4 internal
peer 4.1.1.20 group as4
peer 4.1.1.21 group as4
peer 4.1.1.22 group as4
peer 4.1.1.23 group as4
peer 4.1.1.24 group as4
peer 4.1.1.25 group as4
peer 4.1.1.26 group as4
peer 4.2.1.9 group as4
peer 4.2.1.10 group as4
peer as4 connect-interface LoopBack 0
peer 200.0.0.233 as-number 2
```

## AR20

```shell
sys
sysn rt20

inter g 4/0/0
ip addr 200.0.0.230 24

inter g 0/0/1
ip addr 200.4.2.20 24

inter g 0/0/0
ip addr 200.4.3.20 24

inter loop 0
ip addr 4.1.1.20 32

quit

router id 4.1.1.20
ospf
area 0
network 200.4.2.20 0.0.0.255
network 200.4.3.20 0.0.0.255

quit
quit

bgp 4
group as4 internal
peer 4.1.1.19 group as4
peer 4.1.1.21 group as4
peer 4.1.1.22 group as4
peer 4.1.1.23 group as4
peer 4.1.1.24 group as4
peer 4.1.1.25 group as4
peer 4.1.1.26 group as4
peer 4.2.1.9 group as4
peer 4.2.1.10 group as4
peer as4 connect-interface LoopBack 0
peer 200.0.0.229 as-number 2
```

## AR21

```shell
sys
sysn rt21

inter g 0/0/0
ip addr 200.4.4.21 24

inter g 0/0/1
ip addr 200.4.5.21 24

inter se 4/0/0
ip addr 200.4.6.21 24

inter se 4/0/1
ip addr 200.4.7.21 24

inter loop 0
ip addr 4.1.1.21 32

quit

router id 4.1.1.21
ospf
area 0
network 200.4.4.21 0.0.0.255
network 200.4.5.21 0.0.0.255
network 200.4.6.21 0.0.0.255
network 200.4.7.21 0.0.0.255

quit
quit

bgp 4
group as4 internal
peer 4.1.1.19 group as4
peer 4.1.1.20 group as4
peer 4.1.1.22 group as4
peer 4.1.1.23 group as4
peer 4.1.1.24 group as4
peer 4.1.1.25 group as4
peer 4.1.1.26 group as4
peer 4.2.1.9 group as4
peer 4.2.1.10 group as4
peer as4 connect-interface LoopBack 0
```

## AR22

```shell
sys
sysn rt22

inter g 0/0/0
ip addr 200.4.5.22 24

inter g 0/0/1
ip addr 200.4.4.22 24

inter se 4/0/0
ip addr 200.4.8.22 24

inter se 4/0/1
ip addr 200.4.9.22 24

inter loop 0
ip addr 4.1.1.22 32 

quit

router id 4.1.1.22
ospf
area 0
network 200.4.4.22 0.0.0.255
network 200.4.5.22 0.0.0.255
network 200.4.8.22 0.0.0.255
network 200.4.9.22 0.0.0.255

quit
quit

bgp 4
group as4 internal
peer 4.1.1.19 group as4
peer 4.1.1.20 group as4
peer 4.1.1.21 group as4
peer 4.1.1.23 group as4
peer 4.1.1.24 group as4
peer 4.1.1.25 group as4
peer 4.1.1.26 group as4
peer 4.2.1.9 group as4
peer 4.2.1.10 group as4
peer as4 connect-interface LoopBack 0
```

## AR23

```shell
sys
sysn r23

inter se 4/0/0
ip addr 200.4.6.23 24

inter g 0/0/0
ip addr 200.4.10.23 24

inter g 0/0/1
ip addr 200.4.11.23 24

inter loop 0
ip addr 4.1.1.23 32 

quit

router id 4.1.1.23
ospf
area 0
network 200.4.6.23 0.0.0.255
network 200.4.10.23 0.0.0.255
network 200.4.11.23 0.0.0.255

quit
quit

bgp 4
group as4 internal
peer 4.1.1.19 group as4
peer 4.1.1.20 group as4
peer 4.1.1.21 group as4
peer 4.1.1.22 group as4
peer 4.1.1.24 group as4
peer 4.1.1.25 group as4
peer 4.1.1.26 group as4
peer 4.2.1.9 group as4
peer 4.2.1.10 group as4
peer as4 connect-interface LoopBack 0
```

## AR24

```shell
sys
sysn r24

inter se 4/0/0
ip addr 200.4.8.24 24

inter g 0/0/0
ip addr 200.4.10.24 24

inter g 0/0/1
ip addr 200.4.11.24 24

inter loop 0
ip addr 4.1.1.24 32 

quit

router id 4.1.1.24
ospf
area 0
network 200.4.8.24 0.0.0.255
network 200.4.10.24 0.0.0.255
network 200.4.11.24 0.0.0.255

quit
quit

bgp 4
group as4 internal
peer 4.1.1.19 group as4
peer 4.1.1.20 group as4
peer 4.1.1.21 group as4
peer 4.1.1.22 group as4
peer 4.1.1.23 group as4
peer 4.1.1.25 group as4
peer 4.1.1.26 group as4
peer 4.2.1.9 group as4
peer 4.2.1.10 group as4
peer as4 connect-interface LoopBack 0
```

## AR25

```shell
sys
sysn r25

inter se 4/0/0
ip addr 200.4.7.25 24

inter g 0/0/0
ip addr 200.4.12.25 24

inter g 0/0/1
ip addr 200.4.13.25 24

inter loop 0
ip addr 4.1.1.25 24

quit

router id 4.1.1.25
ospf
area 0
network 200.4.7.25 0.0.0.255
network 200.4.12.25 0.0.0.255
network 200.4.13.25 0.0.0.255

quit
quit

bgp 4
group as4 internal
peer 4.1.1.19 group as4
peer 4.1.1.20 group as4
peer 4.1.1.21 group as4
peer 4.1.1.22 group as4
peer 4.1.1.23 group as4
peer 4.1.1.24 group as4
peer 4.1.1.26 group as4
peer 4.2.1.9 group as4
peer 4.2.1.10 group as4
peer as4 connect-interface LoopBack 0
```

## AR26

```shell
sys
sysn r26

inter se 4/0/0
ip addr 200.4.9.26 24

inter g 0/0/0
ip addr 200.4.12.26 24

inter g 0/0/1
ip addr 200.4.13.26 24 

inter loop 0
ip addr 4.1.1.26 32 

quit

router id 4.1.1.26
ospf
area 0
network 200.4.9.26 0.0.0.255
network 200.4.12.26 0.0.0.255
network 200.4.13.26 0.0.0.255

quit
quit

bgp 4
group as4 internal
peer 4.1.1.19 group as4
peer 4.1.1.20 group as4
peer 4.1.1.21 group as4
peer 4.1.1.22 group as4
peer 4.1.1.23 group as4
peer 4.1.1.24 group as4
peer 4.1.1.25 group as4
peer 4.2.1.9 group as4
peer 4.2.1.10 group as4
peer as4 connect-interface LoopBack 0
```

## LSW9

```shell
sys
sysn ls9

inter g 0/0/1
port link-type access

inter g 0/0/2
port link-type access

inter g 0/0/3
port link-type access

inter g 0/0/4
port link-type access

vlan 2
port g 0/0/3
port g 0/0/4

inter vlan 2
ip addr 200.4.2.9 24

vlan 3
port g 0/0/1
port g 0/0/2

inter vlan 3
ip addr 200.4.4.9  24

vlan 4
port g 0/0/5

inter vlan 4
ip addr 200.4.0.249 24

inter loop 0
ip addr 4.2.1.9 32

quit

router id 4.2.1.9
ospf
area 0
network 200.4.2.9 0.0.0.255
network 200.4.4.9 0.0.0.255
network 200.4.0.249 0.0.0.255
```

## LSW10

```shell
sys
sysn ls10

inter g 0/0/1
port link-type access

inter g 0/0/2
port link-type access

inter g 0/0/3
port link-type access

inter g 0/0/4
port link-type access

vlan 2
port g 0/0/3
port g 0/0/4

inter vlan 2
ip addr 200.4.3.10 24

vlan 3
port g 0/0/1
port g 0/0/2

inter vlan 3
ip addr 200.4.5.10  24

vlan 4
port g 0/0/5

inter vlan 4
ip addr 200.4.0.250 24

inter loop 0
ip addr 4.2.1.10 32

quit

router id 4.2.1.10
ospf
area 0
network 200.4.3.10 0.0.0.255
network 200.4.5.10 0.0.0.255
network 200.4.0.250 0.0.0.255
```


