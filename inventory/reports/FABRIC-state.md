
# Validate State Report

**Table of Contents:**

- [Validate State Report](validate-state-report)
  - [Test Results Summary](#test-results-summary)
  - [Failed Test Results Summary](#failed-test-results-summary)
  - [All Test Results](#all-test-results)

## Test Results Summary

### Summary Totals

| Total Tests | Total Tests Passed | Total Tests Failed |
| ----------- | ------------------ | ------------------ |
| 202 | 197 | 5 |

### Summary Totals Devices Under Tests

| DUT | Total Tests | Tests Passed | Tests Failed | Categories Failed |
| --- | ----------- | ------------ | ------------ | ----------------- |
| DC1-LEAF1A |  46 | 44 | 2 | Interface State, BGP |
| DC1-LEAF1B |  52 | 51 | 1 | Interface State |
| DC1-SPINE1 |  13 | 12 | 1 | NTP |
| DC2-LEAF1A |  43 | 43 | 0 | - |
| DC2-LEAF1B |  35 | 34 | 1 | BGP |
| DC2-SPINE1 |  13 | 13 | 0 | - |

### Summary Totals Per Category

| Test Category | Total Tests | Tests Passed | Tests Failed |
| ------------- | ----------- | ------------ | ------------ |
| NTP |  6 | 5 | 1 |
| Interface State |  70 | 68 | 2 |
| LLDP Topology |  20 | 20 | 0 |
| MLAG |  4 | 4 | 0 |
| IP Reachability |  12 | 12 | 0 |
| BGP |  34 | 32 | 2 |
| Routing Table |  32 | 32 | 0 |
| Loopback0 Reachability |  24 | 24 | 0 |

## Failed Test Results Summary

| Test ID | Node | Test Category | Test Description | Test | Test Result | Failure Reason |
| ------- | ---- | ------------- | ---------------- | ---- | ----------- | -------------- |
| 3 | DC1-SPINE1 | NTP | Synchronised with NTP server | NTP | FAIL | Not synchronised to NTP server |
| 36 | DC1-LEAF1A | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel7 - dc1-fw1_PortChannel | FAIL | Interface shutdown: False - interface status: down - line protocol status: lowerLayerDown |
| 38 | DC1-LEAF1B | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel7 - dc1-fw1_PortChannel | FAIL | Interface shutdown: False - interface status: down - line protocol status: lowerLayerDown |
| 136 | DC1-LEAF1A | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.221.3 | FAIL | Session state: Connect |
| 144 | DC2-LEAF1B | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.211.4 | FAIL | Session state: Connect |

## All Test Results

| Test ID | Node | Test Category | Test Description | Test | Test Result | Failure Reason |
| ------- | ---- | ------------- | ---------------- | ---- | ----------- | -------------- |
| 1 | DC1-LEAF1A | NTP | Synchronised with NTP server | NTP | PASS | - |
| 2 | DC1-LEAF1B | NTP | Synchronised with NTP server | NTP | PASS | - |
| 3 | DC1-SPINE1 | NTP | Synchronised with NTP server | NTP | FAIL | Not synchronised to NTP server |
| 4 | DC2-LEAF1A | NTP | Synchronised with NTP server | NTP | PASS | - |
| 5 | DC2-LEAF1B | NTP | Synchronised with NTP server | NTP | PASS | - |
| 6 | DC2-SPINE1 | NTP | Synchronised with NTP server | NTP | PASS | - |
| 7 | DC1-LEAF1A | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet3 - MLAG_PEER_DC1-LEAF1B_Ethernet3 | PASS | - |
| 8 | DC1-LEAF1A | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet4 - MLAG_PEER_DC1-LEAF1B_Ethernet4 | PASS | - |
| 9 | DC1-LEAF1A | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet1 - P2P_LINK_TO_DC1-SPINE1_Ethernet1 | PASS | - |
| 10 | DC1-LEAF1A | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet6 - TESTA_WAN1 | PASS | - |
| 11 | DC1-LEAF1A | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet8 - dc1-server01_Eth0 | PASS | - |
| 12 | DC1-LEAF1A | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet5 - dc1-server03_Eth1 | PASS | - |
| 13 | DC1-LEAF1A | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet7 - dc1-fw1_eth0 | PASS | - |
| 14 | DC1-LEAF1B | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet3 - MLAG_PEER_DC1-LEAF1A_Ethernet3 | PASS | - |
| 15 | DC1-LEAF1B | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet4 - MLAG_PEER_DC1-LEAF1A_Ethernet4 | PASS | - |
| 16 | DC1-LEAF1B | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet1 - P2P_LINK_TO_DC1-SPINE1_Ethernet2 | PASS | - |
| 17 | DC1-LEAF1B | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet5 - P2P_LINK_TO_DC2-LEAF1A_Ethernet5 | PASS | - |
| 18 | DC1-LEAF1B | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet6 - P2P_LINK_TO_DC2-LEAF1A_Ethernet6 | PASS | - |
| 19 | DC1-LEAF1B | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet8 - dc1-server02_Eth1 | PASS | - |
| 20 | DC1-LEAF1B | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet7 - dc1-fw1_eth1 | PASS | - |
| 21 | DC1-SPINE1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet1 - P2P_LINK_TO_DC1-LEAF1A_Ethernet1 | PASS | - |
| 22 | DC1-SPINE1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet2 - P2P_LINK_TO_DC1-LEAF1B_Ethernet1 | PASS | - |
| 23 | DC2-LEAF1A | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet3 - MLAG_PEER_DC2-LEAF1B_Ethernet3 | PASS | - |
| 24 | DC2-LEAF1A | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet4 - MLAG_PEER_DC2-LEAF1B_Ethernet4 | PASS | - |
| 25 | DC2-LEAF1A | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet1 - P2P_LINK_TO_DC2-SPINE1_Ethernet1 | PASS | - |
| 26 | DC2-LEAF1A | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet5 - P2P_LINK_TO_DC1-LEAF1B_Ethernet5 | PASS | - |
| 27 | DC2-LEAF1A | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet6 - P2P_LINK_TO_DC1-LEAF1B_Ethernet6 | PASS | - |
| 28 | DC2-LEAF1A | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet8 - dc2-server01_Eth0 | PASS | - |
| 29 | DC2-LEAF1B | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet3 - MLAG_PEER_DC2-LEAF1A_Ethernet3 | PASS | - |
| 30 | DC2-LEAF1B | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet4 - MLAG_PEER_DC2-LEAF1A_Ethernet4 | PASS | - |
| 31 | DC2-LEAF1B | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet1 - P2P_LINK_TO_DC2-SPINE1_Ethernet2 | PASS | - |
| 32 | DC2-LEAF1B | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet8 - dc2-server02_Eth1 | PASS | - |
| 33 | DC2-SPINE1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet1 - P2P_LINK_TO_DC2-LEAF1A_Ethernet1 | PASS | - |
| 34 | DC2-SPINE1 | Interface State | Ethernet Interface & Line Protocol == "up" | Ethernet2 - P2P_LINK_TO_DC2-LEAF1B_Ethernet1 | PASS | - |
| 35 | DC1-LEAF1A | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel3 - MLAG_PEER_DC1-LEAF1B_Po3 | PASS | - |
| 36 | DC1-LEAF1A | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel7 - dc1-fw1_PortChannel | FAIL | Interface shutdown: False - interface status: down - line protocol status: lowerLayerDown |
| 37 | DC1-LEAF1B | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel3 - MLAG_PEER_DC1-LEAF1A_Po3 | PASS | - |
| 38 | DC1-LEAF1B | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel7 - dc1-fw1_PortChannel | FAIL | Interface shutdown: False - interface status: down - line protocol status: lowerLayerDown |
| 39 | DC2-LEAF1A | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel3 - MLAG_PEER_DC2-LEAF1B_Po3 | PASS | - |
| 40 | DC2-LEAF1B | Interface State | Port-Channel Interface & Line Protocol == "up" | Port-Channel3 - MLAG_PEER_DC2-LEAF1A_Po3 | PASS | - |
| 41 | DC1-LEAF1A | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4093 - MLAG_PEER_L3_PEERING | PASS | - |
| 42 | DC1-LEAF1A | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4094 - MLAG_PEER | PASS | - |
| 43 | DC1-LEAF1A | Interface State | Vlan Interface & Line Protocol == "up" | Vlan10 - Tenant_A_OP_Zone_10 | PASS | - |
| 44 | DC1-LEAF1A | Interface State | Vlan Interface & Line Protocol == "up" | Vlan11 - Tenant_A_OP_Zone_11 | PASS | - |
| 45 | DC1-LEAF1A | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4000 - MLAG_PEER_L3_iBGP: vrf Tenant_A_OP_Zone | PASS | - |
| 46 | DC1-LEAF1A | Interface State | Vlan Interface & Line Protocol == "up" | Vlan20 - Tenant_A_WEB_Zone_1 | PASS | - |
| 47 | DC1-LEAF1A | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4001 - MLAG_PEER_L3_iBGP: vrf Tenant_A_WEB_Zone | PASS | - |
| 48 | DC1-LEAF1B | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4093 - MLAG_PEER_L3_PEERING | PASS | - |
| 49 | DC1-LEAF1B | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4094 - MLAG_PEER | PASS | - |
| 50 | DC1-LEAF1B | Interface State | Vlan Interface & Line Protocol == "up" | Vlan10 - Tenant_A_OP_Zone_10 | PASS | - |
| 51 | DC1-LEAF1B | Interface State | Vlan Interface & Line Protocol == "up" | Vlan11 - Tenant_A_OP_Zone_11 | PASS | - |
| 52 | DC1-LEAF1B | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4000 - MLAG_PEER_L3_iBGP: vrf Tenant_A_OP_Zone | PASS | - |
| 53 | DC1-LEAF1B | Interface State | Vlan Interface & Line Protocol == "up" | Vlan20 - Tenant_A_WEB_Zone_1 | PASS | - |
| 54 | DC1-LEAF1B | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4001 - MLAG_PEER_L3_iBGP: vrf Tenant_A_WEB_Zone | PASS | - |
| 55 | DC2-LEAF1A | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4093 - MLAG_PEER_L3_PEERING | PASS | - |
| 56 | DC2-LEAF1A | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4094 - MLAG_PEER | PASS | - |
| 57 | DC2-LEAF1B | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4093 - MLAG_PEER_L3_PEERING | PASS | - |
| 58 | DC2-LEAF1B | Interface State | Vlan Interface & Line Protocol == "up" | Vlan4094 - MLAG_PEER | PASS | - |
| 59 | DC1-LEAF1A | Interface State | Vxlan Interface Status & Line Protocol == "up" | Vxlan1 | PASS | - |
| 60 | DC1-LEAF1B | Interface State | Vxlan Interface Status & Line Protocol == "up" | Vxlan1 | PASS | - |
| 61 | DC2-LEAF1A | Interface State | Vxlan Interface Status & Line Protocol == "up" | Vxlan1 | PASS | - |
| 62 | DC2-LEAF1B | Interface State | Vxlan Interface Status & Line Protocol == "up" | Vxlan1 | PASS | - |
| 63 | DC1-LEAF1A | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS | - |
| 64 | DC1-LEAF1A | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback1 - VTEP_VXLAN_Tunnel_Source | PASS | - |
| 65 | DC1-LEAF1A | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback10 - Tenant_A_OP_Zone_VTEP_DIAGNOSTICS | PASS | - |
| 66 | DC1-LEAF1A | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback20 - Tenant_A_WEB_Zone_VTEP_DIAGNOSTICS | PASS | - |
| 67 | DC1-LEAF1B | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS | - |
| 68 | DC1-LEAF1B | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback1 - VTEP_VXLAN_Tunnel_Source | PASS | - |
| 69 | DC1-LEAF1B | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback10 - Tenant_A_OP_Zone_VTEP_DIAGNOSTICS | PASS | - |
| 70 | DC1-LEAF1B | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback20 - Tenant_A_WEB_Zone_VTEP_DIAGNOSTICS | PASS | - |
| 71 | DC1-SPINE1 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS | - |
| 72 | DC2-LEAF1A | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS | - |
| 73 | DC2-LEAF1A | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback1 - VTEP_VXLAN_Tunnel_Source | PASS | - |
| 74 | DC2-LEAF1B | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS | - |
| 75 | DC2-LEAF1B | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback1 - VTEP_VXLAN_Tunnel_Source | PASS | - |
| 76 | DC2-SPINE1 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS | - |
| 77 | DC1-LEAF1A | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet3 - remote: DC1-LEAF1B_Ethernet3 | PASS | - |
| 78 | DC1-LEAF1A | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet4 - remote: DC1-LEAF1B_Ethernet4 | PASS | - |
| 79 | DC1-LEAF1A | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet1 - remote: DC1-SPINE1_Ethernet1 | PASS | - |
| 80 | DC1-LEAF1B | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet3 - remote: DC1-LEAF1A_Ethernet3 | PASS | - |
| 81 | DC1-LEAF1B | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet4 - remote: DC1-LEAF1A_Ethernet4 | PASS | - |
| 82 | DC1-LEAF1B | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet1 - remote: DC1-SPINE1_Ethernet2 | PASS | - |
| 83 | DC1-LEAF1B | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet5 - remote: DC2-LEAF1A_Ethernet5 | PASS | - |
| 84 | DC1-LEAF1B | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet6 - remote: DC2-LEAF1A_Ethernet6 | PASS | - |
| 85 | DC1-SPINE1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet1 - remote: DC1-LEAF1A_Ethernet1 | PASS | - |
| 86 | DC1-SPINE1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet2 - remote: DC1-LEAF1B_Ethernet1 | PASS | - |
| 87 | DC2-LEAF1A | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet3 - remote: DC2-LEAF1B_Ethernet3 | PASS | - |
| 88 | DC2-LEAF1A | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet4 - remote: DC2-LEAF1B_Ethernet4 | PASS | - |
| 89 | DC2-LEAF1A | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet1 - remote: DC2-SPINE1_Ethernet1 | PASS | - |
| 90 | DC2-LEAF1A | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet5 - remote: DC1-LEAF1B_Ethernet5 | PASS | - |
| 91 | DC2-LEAF1A | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet6 - remote: DC1-LEAF1B_Ethernet6 | PASS | - |
| 92 | DC2-LEAF1B | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet3 - remote: DC2-LEAF1A_Ethernet3 | PASS | - |
| 93 | DC2-LEAF1B | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet4 - remote: DC2-LEAF1A_Ethernet4 | PASS | - |
| 94 | DC2-LEAF1B | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet1 - remote: DC2-SPINE1_Ethernet2 | PASS | - |
| 95 | DC2-SPINE1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet1 - remote: DC2-LEAF1A_Ethernet1 | PASS | - |
| 96 | DC2-SPINE1 | LLDP Topology | LLDP topology - validate peer and interface | local: Ethernet2 - remote: DC2-LEAF1B_Ethernet1 | PASS | - |
| 97 | DC1-LEAF1A | MLAG | MLAG State active & Status connected | MLAG | PASS | - |
| 98 | DC1-LEAF1B | MLAG | MLAG State active & Status connected | MLAG | PASS | - |
| 99 | DC2-LEAF1A | MLAG | MLAG State active & Status connected | MLAG | PASS | - |
| 100 | DC2-LEAF1B | MLAG | MLAG State active & Status connected | MLAG | PASS | - |
| 101 | DC1-LEAF1A | IP Reachability | ip reachability test p2p links | Source: DC1-LEAF1A_Ethernet1 - Destination: DC1-SPINE1_Ethernet1 | PASS | - |
| 102 | DC1-LEAF1B | IP Reachability | ip reachability test p2p links | Source: DC1-LEAF1B_Ethernet1 - Destination: DC1-SPINE1_Ethernet2 | PASS | - |
| 103 | DC1-LEAF1B | IP Reachability | ip reachability test p2p links | Source: DC1-LEAF1B_Ethernet5 - Destination: DC2-LEAF1A_Ethernet5 | PASS | - |
| 104 | DC1-LEAF1B | IP Reachability | ip reachability test p2p links | Source: DC1-LEAF1B_Ethernet6 - Destination: DC2-LEAF1A_Ethernet6 | PASS | - |
| 105 | DC1-SPINE1 | IP Reachability | ip reachability test p2p links | Source: DC1-SPINE1_Ethernet1 - Destination: DC1-LEAF1A_Ethernet1 | PASS | - |
| 106 | DC1-SPINE1 | IP Reachability | ip reachability test p2p links | Source: DC1-SPINE1_Ethernet2 - Destination: DC1-LEAF1B_Ethernet1 | PASS | - |
| 107 | DC2-LEAF1A | IP Reachability | ip reachability test p2p links | Source: DC2-LEAF1A_Ethernet1 - Destination: DC2-SPINE1_Ethernet1 | PASS | - |
| 108 | DC2-LEAF1A | IP Reachability | ip reachability test p2p links | Source: DC2-LEAF1A_Ethernet5 - Destination: DC1-LEAF1B_Ethernet5 | PASS | - |
| 109 | DC2-LEAF1A | IP Reachability | ip reachability test p2p links | Source: DC2-LEAF1A_Ethernet6 - Destination: DC1-LEAF1B_Ethernet6 | PASS | - |
| 110 | DC2-LEAF1B | IP Reachability | ip reachability test p2p links | Source: DC2-LEAF1B_Ethernet1 - Destination: DC2-SPINE1_Ethernet2 | PASS | - |
| 111 | DC2-SPINE1 | IP Reachability | ip reachability test p2p links | Source: DC2-SPINE1_Ethernet1 - Destination: DC2-LEAF1A_Ethernet1 | PASS | - |
| 112 | DC2-SPINE1 | IP Reachability | ip reachability test p2p links | Source: DC2-SPINE1_Ethernet2 - Destination: DC2-LEAF1B_Ethernet1 | PASS | - |
| 113 | DC1-LEAF1A | BGP | ArBGP is configured and operating | ArBGP | PASS | - |
| 114 | DC1-LEAF1B | BGP | ArBGP is configured and operating | ArBGP | PASS | - |
| 115 | DC1-SPINE1 | BGP | ArBGP is configured and operating | ArBGP | PASS | - |
| 116 | DC2-LEAF1A | BGP | ArBGP is configured and operating | ArBGP | PASS | - |
| 117 | DC2-LEAF1B | BGP | ArBGP is configured and operating | ArBGP | PASS | - |
| 118 | DC2-SPINE1 | BGP | ArBGP is configured and operating | ArBGP | PASS | - |
| 119 | DC1-LEAF1A | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 10.255.214.1 | PASS | - |
| 120 | DC1-LEAF1A | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.210.0 | PASS | - |
| 121 | DC1-LEAF1B | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 10.255.214.0 | PASS | - |
| 122 | DC1-LEAF1B | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.210.2 | PASS | - |
| 123 | DC1-LEAF1B | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 10.254.0.1 | PASS | - |
| 124 | DC1-LEAF1B | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 10.254.0.3 | PASS | - |
| 125 | DC1-SPINE1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.210.1 | PASS | - |
| 126 | DC1-SPINE1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.210.3 | PASS | - |
| 127 | DC2-LEAF1A | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 10.255.224.1 | PASS | - |
| 128 | DC2-LEAF1A | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.220.0 | PASS | - |
| 129 | DC2-LEAF1A | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 10.254.0.0 | PASS | - |
| 130 | DC2-LEAF1A | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 10.254.0.2 | PASS | - |
| 131 | DC2-LEAF1B | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 10.255.224.0 | PASS | - |
| 132 | DC2-LEAF1B | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.220.2 | PASS | - |
| 133 | DC2-SPINE1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.220.1 | PASS | - |
| 134 | DC2-SPINE1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.220.3 | PASS | - |
| 135 | DC1-LEAF1A | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.211.1 | PASS | - |
| 136 | DC1-LEAF1A | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.221.3 | FAIL | Session state: Connect |
| 137 | DC1-LEAF1B | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.211.1 | PASS | - |
| 138 | DC1-LEAF1B | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.221.3 | PASS | - |
| 139 | DC1-SPINE1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.211.3 | PASS | - |
| 140 | DC1-SPINE1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.211.4 | PASS | - |
| 141 | DC2-LEAF1A | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.221.1 | PASS | - |
| 142 | DC2-LEAF1A | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.211.4 | PASS | - |
| 143 | DC2-LEAF1B | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.221.1 | PASS | - |
| 144 | DC2-LEAF1B | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.211.4 | FAIL | Session state: Connect |
| 145 | DC2-SPINE1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.221.3 | PASS | - |
| 146 | DC2-SPINE1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.221.4 | PASS | - |
| 147 | DC1-LEAF1A | Routing Table | Remote VTEP address | 192.168.212.3 | PASS | - |
| 148 | DC1-LEAF1A | Routing Table | Remote VTEP address | 192.168.222.3 | PASS | - |
| 149 | DC1-LEAF1B | Routing Table | Remote VTEP address | 192.168.212.3 | PASS | - |
| 150 | DC1-LEAF1B | Routing Table | Remote VTEP address | 192.168.222.3 | PASS | - |
| 151 | DC2-LEAF1A | Routing Table | Remote VTEP address | 192.168.212.3 | PASS | - |
| 152 | DC2-LEAF1A | Routing Table | Remote VTEP address | 192.168.222.3 | PASS | - |
| 153 | DC2-LEAF1B | Routing Table | Remote VTEP address | 192.168.212.3 | PASS | - |
| 154 | DC2-LEAF1B | Routing Table | Remote VTEP address | 192.168.222.3 | PASS | - |
| 155 | DC1-LEAF1A | Routing Table | Remote Lo0 address | 192.168.211.3 | PASS | - |
| 156 | DC1-LEAF1A | Routing Table | Remote Lo0 address | 192.168.211.4 | PASS | - |
| 157 | DC1-LEAF1A | Routing Table | Remote Lo0 address | 192.168.211.1 | PASS | - |
| 158 | DC1-LEAF1A | Routing Table | Remote Lo0 address | 192.168.221.3 | PASS | - |
| 159 | DC1-LEAF1A | Routing Table | Remote Lo0 address | 192.168.221.4 | PASS | - |
| 160 | DC1-LEAF1A | Routing Table | Remote Lo0 address | 192.168.221.1 | PASS | - |
| 161 | DC1-LEAF1B | Routing Table | Remote Lo0 address | 192.168.211.3 | PASS | - |
| 162 | DC1-LEAF1B | Routing Table | Remote Lo0 address | 192.168.211.4 | PASS | - |
| 163 | DC1-LEAF1B | Routing Table | Remote Lo0 address | 192.168.211.1 | PASS | - |
| 164 | DC1-LEAF1B | Routing Table | Remote Lo0 address | 192.168.221.3 | PASS | - |
| 165 | DC1-LEAF1B | Routing Table | Remote Lo0 address | 192.168.221.4 | PASS | - |
| 166 | DC1-LEAF1B | Routing Table | Remote Lo0 address | 192.168.221.1 | PASS | - |
| 167 | DC2-LEAF1A | Routing Table | Remote Lo0 address | 192.168.211.3 | PASS | - |
| 168 | DC2-LEAF1A | Routing Table | Remote Lo0 address | 192.168.211.4 | PASS | - |
| 169 | DC2-LEAF1A | Routing Table | Remote Lo0 address | 192.168.211.1 | PASS | - |
| 170 | DC2-LEAF1A | Routing Table | Remote Lo0 address | 192.168.221.3 | PASS | - |
| 171 | DC2-LEAF1A | Routing Table | Remote Lo0 address | 192.168.221.4 | PASS | - |
| 172 | DC2-LEAF1A | Routing Table | Remote Lo0 address | 192.168.221.1 | PASS | - |
| 173 | DC2-LEAF1B | Routing Table | Remote Lo0 address | 192.168.211.3 | PASS | - |
| 174 | DC2-LEAF1B | Routing Table | Remote Lo0 address | 192.168.211.4 | PASS | - |
| 175 | DC2-LEAF1B | Routing Table | Remote Lo0 address | 192.168.211.1 | PASS | - |
| 176 | DC2-LEAF1B | Routing Table | Remote Lo0 address | 192.168.221.3 | PASS | - |
| 177 | DC2-LEAF1B | Routing Table | Remote Lo0 address | 192.168.221.4 | PASS | - |
| 178 | DC2-LEAF1B | Routing Table | Remote Lo0 address | 192.168.221.1 | PASS | - |
| 179 | DC1-LEAF1A | Loopback0 Reachability | Loopback0 Reachability | Source: DC1-LEAF1A - 192.168.211.3 Destination: 192.168.211.3 | PASS | - |
| 180 | DC1-LEAF1A | Loopback0 Reachability | Loopback0 Reachability | Source: DC1-LEAF1A - 192.168.211.3 Destination: 192.168.211.4 | PASS | - |
| 181 | DC1-LEAF1A | Loopback0 Reachability | Loopback0 Reachability | Source: DC1-LEAF1A - 192.168.211.3 Destination: 192.168.211.1 | PASS | - |
| 182 | DC1-LEAF1A | Loopback0 Reachability | Loopback0 Reachability | Source: DC1-LEAF1A - 192.168.211.3 Destination: 192.168.221.3 | PASS | - |
| 183 | DC1-LEAF1A | Loopback0 Reachability | Loopback0 Reachability | Source: DC1-LEAF1A - 192.168.211.3 Destination: 192.168.221.4 | PASS | - |
| 184 | DC1-LEAF1A | Loopback0 Reachability | Loopback0 Reachability | Source: DC1-LEAF1A - 192.168.211.3 Destination: 192.168.221.1 | PASS | - |
| 185 | DC1-LEAF1B | Loopback0 Reachability | Loopback0 Reachability | Source: DC1-LEAF1B - 192.168.211.4 Destination: 192.168.211.3 | PASS | - |
| 186 | DC1-LEAF1B | Loopback0 Reachability | Loopback0 Reachability | Source: DC1-LEAF1B - 192.168.211.4 Destination: 192.168.211.4 | PASS | - |
| 187 | DC1-LEAF1B | Loopback0 Reachability | Loopback0 Reachability | Source: DC1-LEAF1B - 192.168.211.4 Destination: 192.168.211.1 | PASS | - |
| 188 | DC1-LEAF1B | Loopback0 Reachability | Loopback0 Reachability | Source: DC1-LEAF1B - 192.168.211.4 Destination: 192.168.221.3 | PASS | - |
| 189 | DC1-LEAF1B | Loopback0 Reachability | Loopback0 Reachability | Source: DC1-LEAF1B - 192.168.211.4 Destination: 192.168.221.4 | PASS | - |
| 190 | DC1-LEAF1B | Loopback0 Reachability | Loopback0 Reachability | Source: DC1-LEAF1B - 192.168.211.4 Destination: 192.168.221.1 | PASS | - |
| 191 | DC2-LEAF1A | Loopback0 Reachability | Loopback0 Reachability | Source: DC2-LEAF1A - 192.168.221.3 Destination: 192.168.211.3 | PASS | - |
| 192 | DC2-LEAF1A | Loopback0 Reachability | Loopback0 Reachability | Source: DC2-LEAF1A - 192.168.221.3 Destination: 192.168.211.4 | PASS | - |
| 193 | DC2-LEAF1A | Loopback0 Reachability | Loopback0 Reachability | Source: DC2-LEAF1A - 192.168.221.3 Destination: 192.168.211.1 | PASS | - |
| 194 | DC2-LEAF1A | Loopback0 Reachability | Loopback0 Reachability | Source: DC2-LEAF1A - 192.168.221.3 Destination: 192.168.221.3 | PASS | - |
| 195 | DC2-LEAF1A | Loopback0 Reachability | Loopback0 Reachability | Source: DC2-LEAF1A - 192.168.221.3 Destination: 192.168.221.4 | PASS | - |
| 196 | DC2-LEAF1A | Loopback0 Reachability | Loopback0 Reachability | Source: DC2-LEAF1A - 192.168.221.3 Destination: 192.168.221.1 | PASS | - |
| 197 | DC2-LEAF1B | Loopback0 Reachability | Loopback0 Reachability | Source: DC2-LEAF1B - 192.168.221.4 Destination: 192.168.211.3 | PASS | - |
| 198 | DC2-LEAF1B | Loopback0 Reachability | Loopback0 Reachability | Source: DC2-LEAF1B - 192.168.221.4 Destination: 192.168.211.4 | PASS | - |
| 199 | DC2-LEAF1B | Loopback0 Reachability | Loopback0 Reachability | Source: DC2-LEAF1B - 192.168.221.4 Destination: 192.168.211.1 | PASS | - |
| 200 | DC2-LEAF1B | Loopback0 Reachability | Loopback0 Reachability | Source: DC2-LEAF1B - 192.168.221.4 Destination: 192.168.221.3 | PASS | - |
| 201 | DC2-LEAF1B | Loopback0 Reachability | Loopback0 Reachability | Source: DC2-LEAF1B - 192.168.221.4 Destination: 192.168.221.4 | PASS | - |
| 202 | DC2-LEAF1B | Loopback0 Reachability | Loopback0 Reachability | Source: DC2-LEAF1B - 192.168.221.4 Destination: 192.168.221.1 | PASS | - |
