# DC2-SPINE1 Commands Output

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
Router identifier 192.168.221.1, local AS number 65200
Neighbor Status Codes: m - Under maintenance
  Description              Neighbor      V AS           MsgRcvd   MsgSent  InQ OutQ  Up/Down State   PfxRcd PfxAcc
  DC1-SPINE1               192.168.211.1 4 65100             56        60    0    0 00:37:42 Estab   18     18
  DC2-LEAF1A               192.168.221.3 4 65201            450       467    0    0 04:39:10 Estab   9      9
  DC2-LEAF1B               192.168.221.4 4 65201            450       464    0    0 05:56:16 Estab   9      9
```
## show bgp summary

```
BGP summary information for VRF default
Router identifier 192.168.221.1, local AS number 65200
Neighbor               AS Session State AFI/SAFI                AFI/SAFI State   NLRI Rcd   NLRI Acc
------------- ----------- ------------- ----------------------- -------------- ---------- ----------
172.31.220.1        65201 Established   IPv4 Unicast            Negotiated              7          7
172.31.220.3        65201 Established   IPv4 Unicast            Negotiated              7          7
192.168.211.1       65100 Established   L2VPN EVPN              Negotiated             18         18
192.168.221.3       65201 Established   L2VPN EVPN              Negotiated              9          9
192.168.221.4       65201 Established   L2VPN EVPN              Negotiated              9          9
```
## show interfaces description

```
Interface                      Status         Protocol           Description
Et1                            up             up                 P2P_LINK_TO_DC2-LEAF1A_Ethernet1
Et2                            up             up                 P2P_LINK_TO_DC2-LEAF1B_Ethernet1
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
Ethernet1       172.31.220.0/31      up         up              1500           
Ethernet2       172.31.220.2/31      up         up              1500           
Loopback0       192.168.221.1/32     up         up             65535           
Management1     10.31.100.112/24     up         up              1500
```
## show lldp neighbors

```
Last table change time   : 4:34:56 ago
Number of table inserts  : 4
Number of table deletes  : 2
Number of table drops    : 0
Number of table age-outs : 1

Port          Neighbor Device ID       Neighbor Port ID    TTL
---------- ------------------------ ---------------------- ---
Et1           DC2-LEAF1A               Ethernet1           120
Et2           DC2-LEAF1B               Ethernet1           120
```
## show version

```
Arista vEOS-lab
Hardware version: 
Serial number: 1AEB84471A0B41039BA787400CD3CCBC
Hardware MAC address: 5000.00cb.38c2
System MAC address: 5000.00cb.38c2

Software image version: 4.27.8.1M
Architecture: i686
Internal build version: 4.27.8.1M-30109597.42781M
Internal build ID: b7ede8e2-7d97-4224-8646-37ea52284c87
Image format version: 1.0
Image optimization: None

Uptime: 6 hours and 1 minute
Total memory: 4000296 kB
Free memory: 2979980 kB
```
