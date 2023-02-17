# DC1-LEAF1A Commands Output

## Table of Contents

- [show lldp neighbors](#show-lldp-neighbors)
- [show ip interface brief](#show-ip-interface-brief)
- [show interfaces description](#show-interfaces-description)
- [show version](#show-version)
- [show bgp summary](#show-bgp-summary)
- [show bgp evpn summary](#show-bgp-evpn-summary)
## show bgp evpn summary

```
BGP summary information for VRF default
Router identifier 192.168.211.3, local AS number 65101
Neighbor Status Codes: m - Under maintenance
  Description              Neighbor      V AS           MsgRcvd   MsgSent  InQ OutQ  Up/Down State   PfxRcd PfxAcc
  DC1-SPINE1               192.168.211.1 4 65100            464       451    0    0 05:56:00 Estab   18     18
```
## show bgp summary

```
BGP summary information for VRF default
Router identifier 192.168.211.3, local AS number 65101
Neighbor               AS Session State AFI/SAFI                AFI/SAFI State   NLRI Rcd   NLRI Acc
------------- ----------- ------------- ----------------------- -------------- ---------- ----------
10.255.214.1        65101 Established   IPv4 Unicast            Negotiated              7          7
172.31.210.0        65100 Established   IPv4 Unicast            Negotiated              1          1
192.168.211.1       65100 Established   L2VPN EVPN              Negotiated             18         18
```
## show interfaces description

```
Interface                      Status         Protocol           Description
Et1                            up             up                 P2P_LINK_TO_DC1-SPINE1_Ethernet1
Et2                            up             up                 
Et3                            up             up                 MLAG_PEER_DC1-LEAF1B_Ethernet3
Et4                            up             up                 MLAG_PEER_DC1-LEAF1B_Ethernet4
Et5                            up             up                 
Et6                            up             up                 
Et7                            up             up                 
Et8                            up             up                 dc1-server01_Eth0
Lo0                            up             up                 EVPN_Overlay_Peering
Lo1                            up             up                 VTEP_VXLAN_Tunnel_Source
Lo10                           up             up                 Tenant_A_OP_Zone_VTEP_DIAGNOSTICS
Ma1                            up             up                 oob_management
Po3                            up             up                 MLAG_PEER_DC1-LEAF1B_Po3
Vl10                           up             up                 Tenant_A_OP_Zone_10
Vl11                           up             up                 Tenant_A_OP_Zone_11
Vl1199                         up             up                 
Vl4000                         up             up                 MLAG_PEER_L3_iBGP: vrf Tenant_A_OP_Zone
Vl4093                         up             up                 MLAG_PEER_L3_PEERING
Vl4094                         up             up                 MLAG_PEER
Vx1                            up             up                 DC1-LEAF1A_VTEP
```
## show ip interface brief

```
Address
Interface       IP Address           Status     Protocol         MTU    Owner  
--------------- -------------------- ---------- ------------ ---------- -------
Ethernet1       172.31.210.1/31      up         up              1500           
Loopback0       192.168.211.3/32     up         up             65535           
Loopback1       192.168.212.3/32     up         up             65535           
Loopback10      10.255.10.3/32       up         up             65535           
Management1     10.31.100.101/24     up         up              1500           
Vlan10          10.1.10.1/24         up         up              1500           
Vlan11          10.1.11.1/24         up         up              1500           
Vlan1199        unassigned           up         up              9164           
Vlan4000        10.255.214.0/31      up         up              1500           
Vlan4093        10.255.214.0/31      up         up              1500           
Vlan4094        10.255.213.0/31      up         up              1500
```
## show lldp neighbors

```
Last table change time   : 4:39:15 ago
Number of table inserts  : 5
Number of table deletes  : 2
Number of table drops    : 0
Number of table age-outs : 2

Port          Neighbor Device ID       Neighbor Port ID    TTL
---------- ------------------------ ---------------------- ---
Et1           DC1-SPINE1               Ethernet1           120
Et3           DC1-LEAF1B               Ethernet3           120
Et4           DC1-LEAF1B               Ethernet4           120
```
## show version

```
Arista vEOS-lab
Hardware version: 
Serial number: E6CBC42E3A3474FBBFDE0082440CAEF2
Hardware MAC address: 5000.00d5.5dc0
System MAC address: 5000.00d5.5dc0

Software image version: 4.27.8.1M
Architecture: i686
Internal build version: 4.27.8.1M-30109597.42781M
Internal build ID: b7ede8e2-7d97-4224-8646-37ea52284c87
Image format version: 1.0
Image optimization: None

Uptime: 6 hours and 1 minute
Total memory: 4000296 kB
Free memory: 2895956 kB
```
