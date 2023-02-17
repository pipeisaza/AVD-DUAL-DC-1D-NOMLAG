# DC1-LEAF1B Commands Output

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
Router identifier 192.168.211.4, local AS number 65101
Neighbor Status Codes: m - Under maintenance
  Description              Neighbor      V AS           MsgRcvd   MsgSent  InQ OutQ  Up/Down State   PfxRcd PfxAcc
  DC1-SPINE1               192.168.211.1 4 65100            364       360    0    0 04:39:15 Estab   18     18
```
## show bgp summary

```
BGP summary information for VRF default
Router identifier 192.168.211.4, local AS number 65101
Neighbor               AS Session State AFI/SAFI                AFI/SAFI State   NLRI Rcd   NLRI Acc
------------- ----------- ------------- ----------------------- -------------- ---------- ----------
10.254.0.1          65201 Established   IPv4 Unicast            Negotiated              4          4
10.254.0.3          65201 Established   IPv4 Unicast            Negotiated              4          4
10.255.214.0        65101 Established   IPv4 Unicast            Negotiated              3          3
172.31.210.2        65100 Established   IPv4 Unicast            Negotiated              1          1
192.168.211.1       65100 Established   L2VPN EVPN              Negotiated             18         18
```
## show interfaces description

```
Interface                      Status         Protocol           Description
Et1                            up             up                 P2P_LINK_TO_DC1-SPINE1_Ethernet2
Et2                            up             up                 
Et3                            up             up                 MLAG_PEER_DC1-LEAF1A_Ethernet3
Et4                            up             up                 MLAG_PEER_DC1-LEAF1A_Ethernet4
Et5                            up             up                 P2P_LINK_TO_DC2-LEAF1A_Ethernet5
Et6                            up             up                 P2P_LINK_TO_DC2-LEAF1A_Ethernet6
Et7                            up             up                 
Et8                            up             up                 dc1-server02_Eth1
Lo0                            up             up                 EVPN_Overlay_Peering
Lo1                            up             up                 VTEP_VXLAN_Tunnel_Source
Lo10                           up             up                 Tenant_A_OP_Zone_VTEP_DIAGNOSTICS
Ma1                            up             up                 oob_management
Po3                            up             up                 MLAG_PEER_DC1-LEAF1A_Po3
Vl10                           up             up                 Tenant_A_OP_Zone_10
Vl11                           up             up                 Tenant_A_OP_Zone_11
Vl1199                         up             up                 
Vl4000                         up             up                 MLAG_PEER_L3_iBGP: vrf Tenant_A_OP_Zone
Vl4093                         up             up                 MLAG_PEER_L3_PEERING
Vl4094                         up             up                 MLAG_PEER
Vx1                            up             up                 DC1-LEAF1B_VTEP
```
## show ip interface brief

```
Address
Interface       IP Address           Status     Protocol         MTU    Owner  
--------------- -------------------- ---------- ------------ ---------- -------
Ethernet1       172.31.210.3/31      up         up              1500           
Ethernet5       10.254.0.0/31        up         up              1500           
Ethernet6       10.254.0.2/31        up         up              1500           
Loopback0       192.168.211.4/32     up         up             65535           
Loopback1       192.168.212.3/32     up         up             65535           
Loopback10      10.255.10.4/32       up         up             65535           
Management1     10.31.100.102/24     up         up              1500           
Vlan10          10.1.10.1/24         up         up              1500           
Vlan11          10.1.11.1/24         up         up              1500           
Vlan1199        unassigned           up         up              9164           
Vlan4000        10.255.214.1/31      up         up              1500           
Vlan4093        10.255.214.1/31      up         up              1500           
Vlan4094        10.255.213.1/31      up         up              1500
```
## show lldp neighbors

```
Last table change time   : 4:26:14 ago
Number of table inserts  : 6
Number of table deletes  : 1
Number of table drops    : 0
Number of table age-outs : 0

Port          Neighbor Device ID       Neighbor Port ID    TTL
---------- ------------------------ ---------------------- ---
Et1           DC1-SPINE1               Ethernet2           120
Et3           DC1-LEAF1A               Ethernet3           120
Et4           DC1-LEAF1A               Ethernet4           120
Et5           DC2-LEAF1A               Ethernet5           120
Et6           DC2-LEAF1A               Ethernet6           120
```
## show version

```
Arista vEOS-lab
Hardware version: 
Serial number: 681DBD7721C089B2F8EC5C73ED7698F6
Hardware MAC address: 5000.0003.3766
System MAC address: 5000.0003.3766

Software image version: 4.27.8.1M
Architecture: i686
Internal build version: 4.27.8.1M-30109597.42781M
Internal build ID: b7ede8e2-7d97-4224-8646-37ea52284c87
Image format version: 1.0
Image optimization: None

Uptime: 4 hours and 43 minutes
Total memory: 4000296 kB
Free memory: 2892048 kB
```
