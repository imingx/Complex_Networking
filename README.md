# 北航计算机网络实验 复杂组网实验 操作手册及问题解答

[TOC]

## 实验要求

### 理论拓扑结构

![image](https://user-images.githubusercontent.com/60542677/169002769-24563475-ff37-4111-9428-afa6a8d2bf51.png)

### 实际组网拓扑结构

![image](https://user-images.githubusercontent.com/60542677/169002985-b09a509e-3356-45bd-8a5e-965473204a2e.png)


## 操作步骤

1. 为Router15设置IP地址和配置OSPF协议
  ```shell
  sys
  inter g 0/0/0
  ip addr 10.2.3.15 24
  inter g 0/0/1
  ip addr 10.2.2.15 24
  quit
  router id 1.1.1.1
  ospf
  area 2
  network 10.2.0.0 0.0.255.255
  ```
2. 同理，为Router16配置IP地址和配置OSPF协议
  ```shell
  sys
  inter g 0/0/0
  ip addr 10.2.3.16 24
  inter g 0/0/1
  ip addr 10.2.2.16 24
  quit
  router id 2.2.2.2
  ospf
  area 2
  network 10.2.0.0 0.0.255.255
  ```
3. 为Switch7配置vlan和配置IP地址
  ```shell
  sys
  inter g 0/0/1
  port link-type access
  inter g 0/0/2
  port link-type access
  quit
  vlan 1
  port g 0/0/1
  port g 0/0/2
  inter vlan 1
  ip addr 10.2.2.254 24
  ```
4. 同理，为Swith8配置vlan和IP地址，注意其与主机相连
  ```shell
  sys
  inter g 0/0/1
  port link-type access
  inter g 0/0/2
  port link-type access
  quit
  vlan 1
  port g 0/0/1
  port g 0/0/2
  inter vlan 1
  ip addr 10.2.3.254 24
  vlan 2
  port g 0/0/6
  inter vlan 2
  ip addr 192.168.0.1
  ```
5. 为Router17配置ip地址和OSPF协议
  ```shell
  sys
  inter g 0/0/0
  ip addr 10.2.2.17 24
  inter g 0/0/1
  ip addr 10.2.3.17 24
  inter g 0/0/2
  ip addr 10.0.0.233 24
  quit
  router id 3.3.3.3
  ospf
  area 2
  network 10.2.0.0 0.0.255.255
  ```
6. 同理，为Router18配置ip地址和OSPF协议
  ```shell
  sys
  inter g 0/0/0
  ip addr 10.2.3.18 24
  inter g 0/0/1
  ip addr 10.2.2.18 24
  inter g 0/0/2
  ip addr 10.0.0.229 24
  quit
  router id 4.4.4.4
  ospf
  area 2
  network 10.2.0.0 0.0.255.255
  ```
7. 配置主机IP地址（右键-设置-基础配置）
  - ip地址为192.168.0.250，掩码24位
  
## 遇到的技术问题及其解决方案
- 路由器E口无法配置ip地址，建议使用AR1220型号（有两个GE口能配置ip addr）
- E口要配置IP地址需要通过vlan实现
