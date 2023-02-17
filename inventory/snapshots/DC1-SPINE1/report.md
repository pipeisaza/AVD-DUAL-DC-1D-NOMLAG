# DC1-SPINE1 Commands Output

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
Router identifier 192.168.211.1, local AS number 65100
Neighbor Status Codes: m - Under maintenance
  Description              Neighbor      V AS           MsgRcvd   MsgSent  InQ OutQ  Up/Down State   PfxRcd PfxAcc
  DC1-LEAF1A               192.168.211.3 4 65101            451       465    0    0 05:56:06 Estab   9      9
  DC1-LEAF1B               192.168.211.4 4 65101            456       463    0    0 04:39:20 Estab   9      9
  DC2-SPINE1               192.168.221.1 4 65200             60        56    0    0 00:37:49 Estab   18     18
```
## show bgp summary

```
BGP summary information for VRF default
Router identifier 192.168.211.1, local AS number 65100
Neighbor               AS Session State AFI/SAFI                AFI/SAFI State   NLRI Rcd   NLRI Acc
------------- ----------- ------------- ----------------------- -------------- ---------- ----------
172.31.210.1        65101 Established   IPv4 Unicast            Negotiated              7          7
172.31.210.3        65101 Established   IPv4 Unicast            Negotiated              7          7
192.168.211.3       65101 Established   L2VPN EVPN              Negotiated              9          9
192.168.211.4       65101 Established   L2VPN EVPN              Negotiated              9          9
192.168.221.1       65200 Established   L2VPN EVPN              Negotiated             18         18
```
## show interfaces description

```
Interface                      Status         Protocol           Description
Et1                            up             up                 P2P_LINK_TO_DC1-LEAF1A_Ethernet1
Et2                            up             up                 P2P_LINK_TO_DC1-LEAF1B_Ethernet1
Et3                            up             up                 
Et4                            up             up                 
Et5                            up             up                 
Et6                            up             up                 
Et7                            up             up                 
Et8                            up             up                 
Lo0                            up             up                 EVPN_Overlay_Peering
Ma1                            up             up                 oob_management
```
## show ip interface brief

```
Address
Interface       IP Address           Status     Protocol         MTU    Owner  
--------------- -------------------- ---------- ------------ ---------- -------
Ethernet1       172.31.210.0/31      up         up              1500           
Ethernet2       172.31.210.2/31      up         up              1500           
Loopback0       192.168.211.1/32     up         up             65535           
Management1     10.31.100.111/24     up         up              1500
```
## show lldp neighbors

```
Last table change time   : 4:34:05 ago
Number of table inserts  : 4
Number of table deletes  : 2
Number of table drops    : 0
Number of table age-outs : 1

Port          Neighbor Device ID       Neighbor Port ID    TTL
---------- ------------------------ ---------------------- ---
Et1           DC1-LEAF1A               Ethernet1           120
Et2           DC1-LEAF1B               Ethernet1           120
```
## show version

```
Arista vEOS-lab
Hardware version: 
Serial number: 8609AB1A989D499E2CA13FA6AA9C89E4
Hardware MAC address: 5000.00d7.ee0b
System MAC address: 5000.00d7.ee0b

Software image version: 4.27.8.1M
Architecture: i686
Internal build version: 4.27.8.1M-30109597.42781M
Internal build ID: b7ede8e2-7d97-4224-8646-37ea52284c87
Image format version: 1.0
Image optimization: None

Uptime: 6 hours and 1 minute
Total memory: 4000296 kB
Free memory: 2976804 kB
```
