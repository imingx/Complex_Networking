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
3. 同理，为Router16配置IP地址和配置OSPF协议
  ```shell
  sys
  inter g 0/0/0
  ip addr 10.2.2.16 24
  inter g 0/0/1
  ip addr 10.2.3.16 24
  quit
  router id 2.2.2.2
  ospf
  area 2
  network 10.2.0.0 0.0.255.255
  ```
## 遇到的技术问题及其解决方案
- AR201型号的路由器无法配置ip地址，转而使用AR1220型号的
