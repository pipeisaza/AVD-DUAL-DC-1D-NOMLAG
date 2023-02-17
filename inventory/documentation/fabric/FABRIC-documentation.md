# FABRIC

# Table of Contents

- [Fabric Switches and Management IP](#fabric-switches-and-management-ip)
  - [Fabric Switches with inband Management IP](#fabric-switches-with-inband-management-ip)
- [Fabric Topology](#fabric-topology)
- [Fabric IP Allocation](#fabric-ip-allocation)
  - [Fabric Point-To-Point Links](#fabric-point-to-point-links)
  - [Point-To-Point Links Node Allocation](#point-to-point-links-node-allocation)
  - [Loopback Interfaces (BGP EVPN Peering)](#loopback-interfaces-bgp-evpn-peering)
  - [Loopback0 Interfaces Node Allocation](#loopback0-interfaces-node-allocation)
  - [VTEP Loopback VXLAN Tunnel Source Interfaces (VTEPs Only)](#vtep-loopback-vxlan-tunnel-source-interfaces-vteps-only)
  - [VTEP Loopback Node allocation](#vtep-loopback-node-allocation)

# Fabric Switches and Management IP

| POD | Type | Node | Management IP | Platform | Provisioned in CloudVision |
| --- | ---- | ---- | ------------- | -------- | -------------------------- |
| DC1 | l3leaf | DC1-LEAF1A | 10.31.100.101/24 | vEOS-LAB | Provisioned |
| DC1 | l3leaf | DC1-LEAF1B | 10.31.100.102/24 | vEOS-LAB | Provisioned |
| DC1 | spine | DC1-SPINE1 | 10.31.100.111/24 | vEOS-LAB | Provisioned |
| DC2 | l3leaf | DC2-LEAF1A | 10.31.100.103/24 | vEOS-LAB | Provisioned |
| DC2 | l3leaf | DC2-LEAF1B | 10.31.100.104/24 | vEOS-LAB | Provisioned |
| DC2 | spine | DC2-SPINE1 | 10.31.100.112/24 | vEOS-LAB | Provisioned |

> Provision status is based on Ansible inventory declaration and do not represent real status from CloudVision.

## Fabric Switches with inband Management IP
| POD | Type | Node | Management IP | Inband Interface |
| --- | ---- | ---- | ------------- | ---------------- |

# Fabric Topology

| Type | Node | Node Interface | Peer Type | Peer Node | Peer Interface |
| ---- | ---- | -------------- | --------- | ----------| -------------- |
| l3leaf | DC1-LEAF1A | Ethernet1 | spine | DC1-SPINE1 | Ethernet1 |
| l3leaf | DC1-LEAF1B | Ethernet1 | spine | DC1-SPINE1 | Ethernet2 |
| l3leaf | DC1-LEAF1B | Ethernet5 | l3leaf | DC2-LEAF1A | Ethernet5 |
| l3leaf | DC1-LEAF1B | Ethernet6 | l3leaf | DC2-LEAF1A | Ethernet6 |
| l3leaf | DC2-LEAF1A | Ethernet1 | spine | DC2-SPINE1 | Ethernet1 |
| l3leaf | DC2-LEAF1B | Ethernet1 | spine | DC2-SPINE1 | Ethernet2 |

# Fabric IP Allocation

## Fabric Point-To-Point Links

| Uplink IPv4 Pool | Available Addresses | Assigned addresses | Assigned Address % |
| ---------------- | ------------------- | ------------------ | ------------------ |
| 172.31.210.0/24 | 256 | 4 | 1.57 % |
| 172.31.220.0/24 | 256 | 4 | 1.57 % |

## Point-To-Point Links Node Allocation

| Node | Node Interface | Node IP Address | Peer Node | Peer Interface | Peer IP Address |
| ---- | -------------- | --------------- | --------- | -------------- | --------------- |
| DC1-LEAF1A | Ethernet1 | 172.31.210.1/31 | DC1-SPINE1 | Ethernet1 | 172.31.210.0/31 |
| DC1-LEAF1B | Ethernet1 | 172.31.210.3/31 | DC1-SPINE1 | Ethernet2 | 172.31.210.2/31 |
| DC1-LEAF1B | Ethernet5 | 10.254.0.0/31 | DC2-LEAF1A | Ethernet5 | 10.254.0.1/31 |
| DC1-LEAF1B | Ethernet6 | 10.254.0.2/31 | DC2-LEAF1A | Ethernet6 | 10.254.0.3/31 |
| DC2-LEAF1A | Ethernet1 | 172.31.220.1/31 | DC2-SPINE1 | Ethernet1 | 172.31.220.0/31 |
| DC2-LEAF1B | Ethernet1 | 172.31.220.3/31 | DC2-SPINE1 | Ethernet2 | 172.31.220.2/31 |

## Loopback Interfaces (BGP EVPN Peering)

| Loopback Pool | Available Addresses | Assigned addresses | Assigned Address % |
| ------------- | ------------------- | ------------------ | ------------------ |
| 192.168.211.0/24 | 256 | 3 | 1.18 % |
| 192.168.221.0/24 | 256 | 3 | 1.18 % |

## Loopback0 Interfaces Node Allocation

| POD | Node | Loopback0 |
| --- | ---- | --------- |
| DC1 | DC1-LEAF1A | 192.168.211.3/32 |
| DC1 | DC1-LEAF1B | 192.168.211.4/32 |
| DC1 | DC1-SPINE1 | 192.168.211.1/32 |
| DC2 | DC2-LEAF1A | 192.168.221.3/32 |
| DC2 | DC2-LEAF1B | 192.168.221.4/32 |
| DC2 | DC2-SPINE1 | 192.168.221.1/32 |

## VTEP Loopback VXLAN Tunnel Source Interfaces (VTEPs Only)

| VTEP Loopback Pool | Available Addresses | Assigned addresses | Assigned Address % |
| --------------------- | ------------------- | ------------------ | ------------------ |
| 192.168.212.0/24 | 256 | 2 | 0.79 % |
| 192.168.222.0/24 | 256 | 2 | 0.79 % |

## VTEP Loopback Node allocation

| POD | Node | Loopback1 |
| --- | ---- | --------- |
| DC1 | DC1-LEAF1A | 192.168.212.3/32 |
| DC1 | DC1-LEAF1B | 192.168.212.4/32 |
| DC2 | DC2-LEAF1A | 192.168.222.3/32 |
| DC2 | DC2-LEAF1B | 192.168.222.4/32 |
