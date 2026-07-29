<!--
  ~ Copyright (c) 2026 Arista Networks, Inc.
  ~ Use of this source code is governed by the Apache License 2.0
  ~ that can be found in the LICENSE file.
  -->

# 📊 ANTA Report <a id="anta-report"></a>

**Table of Contents:**

- [ANTA Report](#anta-report)
  - [Test Results Summary](#test-results-summary)
    - [Summary Totals](#summary-totals)
    - [Summary Totals Device Under Test](#summary-totals-device-under-test)
    - [Summary Totals Per Category](#summary-totals-per-category)
  - [Test Results](#test-results)

## 📉 Test Results Summary <a id="test-results-summary"></a>

### 🔢 Summary Totals <a id="summary-totals"></a>

| Total Tests | ✅&nbsp;Success | ⏭️&nbsp;Skipped | ❌&nbsp;Failure | ❗&nbsp;Error |
| :- | :- | :- | :- | :- |
| 368 | 236 | 32 | 88 | 0 |

### 🔌 Summary Totals Device Under Test <a id="summary-totals-device-under-test"></a>

| Device | Total Tests | ✅&nbsp;Success | ⏭️&nbsp;Skipped | ❌&nbsp;Failure | ❗&nbsp;Error | Categories Skipped | Categories Failed |
| :- | :- | :- | :- | :- | :- | :- | :- |
| **dc1-leaf1a** | 26 | 16 | 4 | 5 | 0 | MLAG, VXLAN | BGP, Connectivity, Interfaces, Logging |
| **dc1-leaf1b** | 26 | 16 | 4 | 5 | 0 | MLAG, VXLAN | BGP, Connectivity, Interfaces, Logging |
| **dc1-leaf1c** | 20 | 16 | 0 | 3 | 0 | - | Interfaces, Logging |
| **dc1-leaf2a** | 26 | 15 | 4 | 6 | 0 | MLAG, VXLAN | BGP, Connectivity, Interfaces, Logging |
| **dc1-leaf2b** | 26 | 15 | 4 | 6 | 0 | MLAG, VXLAN | BGP, Connectivity, Interfaces, Logging |
| **dc1-leaf2c** | 20 | 15 | 0 | 4 | 0 | - | Configuration, Interfaces, Logging |
| **dc1-spine1** | 20 | 14 | 0 | 6 | 0 | - | BGP, Configuration, Connectivity, Interfaces, Logging |
| **dc1-spine2** | 20 | 15 | 0 | 5 | 0 | - | BGP, Connectivity, Interfaces, Logging |
| **dc2-leaf1a** | 26 | 14 | 4 | 7 | 0 | MLAG, VXLAN | BGP, Configuration, Connectivity, Interfaces, Logging |
| **dc2-leaf1b** | 26 | 15 | 4 | 6 | 0 | MLAG, VXLAN | BGP, Connectivity, Interfaces, Logging |
| **dc2-leaf1c** | 20 | 14 | 0 | 5 | 0 | - | Configuration, Connectivity, Interfaces, Logging |
| **dc2-leaf2a** | 26 | 14 | 4 | 7 | 0 | MLAG, VXLAN | BGP, Configuration, Connectivity, Interfaces, Logging |
| **dc2-leaf2b** | 26 | 15 | 4 | 6 | 0 | MLAG, VXLAN | BGP, Connectivity, Interfaces, Logging |
| **dc2-leaf2c** | 20 | 15 | 0 | 4 | 0 | - | Connectivity, Interfaces, Logging |
| **dc2-spine1** | 20 | 13 | 0 | 7 | 0 | - | BGP, Configuration, Connectivity, Interfaces, Logging |
| **dc2-spine2** | 20 | 14 | 0 | 6 | 0 | - | BGP, Connectivity, Interfaces, Logging |

### 🗂️ Summary Totals Per Category <a id="summary-totals-per-category"></a>

| Test Category | Total Tests | ✅&nbsp;Success | ⏭️&nbsp;Skipped | ❌&nbsp;Failure | ❗&nbsp;Error |
| :- | :- | :- | :- | :- | :- |
| **BGP** | 12 | 0 | 0 | 12 | 0 |
| **Configuration** | 32 | 26 | 0 | 6 | 0 |
| **Connectivity** | 28 | 6 | 0 | 22 | 0 |
| **Interfaces** | 104 | 60 | 0 | 32 | 0 |
| **Logging** | 16 | 0 | 0 | 16 | 0 |
| **MLAG** | 24 | 0 | 24 | 0 | 0 |
| **Routing** | 16 | 16 | 0 | 0 | 0 |
| **STP** | 16 | 16 | 0 | 0 | 0 |
| **System** | 112 | 112 | 0 | 0 | 0 |
| **VXLAN** | 8 | 0 | 8 | 0 | 0 |

## 🧪 Test Results <a id="test-results"></a>

| Device | Categories | Test | Description | Result | Messages |
| :- | :- | :- | :- | :- | :- |
| dc1-leaf1a | BGP | VerifyBGPPeerSession | Verifies the session state of BGP peers. | ❌&nbsp;Failure | 'show bgp neighbors vrf all' failed on dc1-leaf1a: BGP inactive |
| dc1-leaf1a | Connectivity | VerifyReachability | Verifies point-to-point reachability between Ethernet interfaces. | ❌&nbsp;Failure | Destination 10.255.255.0 (dc1-spine1_Ethernet1) from 10.255.255.1 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address'<br>Destination 10.255.255.2 (dc1-spine2_Ethernet1) from 10.255.255.3 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address' |
| dc1-leaf1a | Interfaces | VerifyInterfaceDiscards | Verifies that the interfaces packet discard counters are equal to zero. | ❌&nbsp;Failure | Interface: Management1 - Non-zero discard counter(s): inDiscards: 53966 |
| dc1-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | ❌&nbsp;Failure | Interface: Loopback0 - Not configured<br>Interface: Loopback1 - Not configured<br>Interface: Loopback10 - Not configured<br>Interface: Loopback11 - Not configured<br>Interface: Port-Channel3 - Not configured<br>Interface: Port-Channel5 - Not configured<br>Interface: Port-Channel8 - Not configured<br>Interface: Vlan11 - Not configured<br>Interface: Vlan12 - Not configured<br>Interface: Vlan21 - Not configured<br>Interface: Vlan22 - Not configured<br>Interface: Vlan3009 - Not configured<br>Interface: Vlan3010 - Not configured<br>Interface: Vlan4093 - Not configured<br>Interface: Vlan4094 - Not configured<br>Interface: Vxlan1 - Not configured |
| dc1-leaf1a | Logging | VerifyLoggingErrors | Verifies there are no syslog messages with a severity of ERRORS or higher. | ❌&nbsp;Failure | Device has reported syslog messages with a severity of ERRORS or higher:<br>Jul 15 12:27:54 dc1-leaf1a NorCalInit: %HARDWARE-0-SYSTEM_IDENTIFICATION_FAILED: Failed to identify this system<br> <br> |
| dc1-leaf1b | BGP | VerifyBGPPeerSession | Verifies the session state of BGP peers. | ❌&nbsp;Failure | 'show bgp neighbors vrf all' failed on dc1-leaf1b: BGP inactive |
| dc1-leaf1b | Connectivity | VerifyReachability | Verifies point-to-point reachability between Ethernet interfaces. | ❌&nbsp;Failure | Destination 10.255.255.4 (dc1-spine1_Ethernet2) from 10.255.255.5 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address'<br>Destination 10.255.255.6 (dc1-spine2_Ethernet2) from 10.255.255.7 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address' |
| dc1-leaf1b | Interfaces | VerifyInterfaceDiscards | Verifies that the interfaces packet discard counters are equal to zero. | ❌&nbsp;Failure | Interface: Management1 - Non-zero discard counter(s): inDiscards: 53966 |
| dc1-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | ❌&nbsp;Failure | Interface: Loopback0 - Not configured<br>Interface: Loopback1 - Not configured<br>Interface: Loopback10 - Not configured<br>Interface: Loopback11 - Not configured<br>Interface: Port-Channel3 - Not configured<br>Interface: Port-Channel5 - Not configured<br>Interface: Port-Channel8 - Not configured<br>Interface: Vlan11 - Not configured<br>Interface: Vlan12 - Not configured<br>Interface: Vlan21 - Not configured<br>Interface: Vlan22 - Not configured<br>Interface: Vlan3009 - Not configured<br>Interface: Vlan3010 - Not configured<br>Interface: Vlan4093 - Not configured<br>Interface: Vlan4094 - Not configured<br>Interface: Vxlan1 - Not configured |
| dc1-leaf1b | Logging | VerifyLoggingErrors | Verifies there are no syslog messages with a severity of ERRORS or higher. | ❌&nbsp;Failure | Device has reported syslog messages with a severity of ERRORS or higher:<br>Jul 15 12:27:54 dc1-leaf1b NorCalInit: %HARDWARE-0-SYSTEM_IDENTIFICATION_FAILED: Failed to identify this system<br> <br> |
| dc1-leaf1c | Interfaces | VerifyInterfaceDiscards | Verifies that the interfaces packet discard counters are equal to zero. | ❌&nbsp;Failure | Interface: Management1 - Non-zero discard counter(s): inDiscards: 53924 |
| dc1-leaf1c | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | ❌&nbsp;Failure | Interface: Port-Channel1 - Not configured |
| dc1-leaf1c | Logging | VerifyLoggingErrors | Verifies there are no syslog messages with a severity of ERRORS or higher. | ❌&nbsp;Failure | Device has reported syslog messages with a severity of ERRORS or higher:<br>Jul 15 12:28:47 dc1-leaf1c NorCalInit: %HARDWARE-0-SYSTEM_IDENTIFICATION_FAILED: Failed to identify this system<br> <br> |
| dc1-leaf2a | BGP | VerifyBGPPeerSession | Verifies the session state of BGP peers. | ❌&nbsp;Failure | 'show bgp neighbors vrf all' failed on dc1-leaf2a: BGP inactive |
| dc1-leaf2a | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | ❌&nbsp;Failure | Port: Ethernet6 Neighbor: dc2-leaf2a Neighbor Port: Ethernet6 - Wrong LLDP neighbors: dc1-leaf2a.avd.lab/Ethernet6 |
| dc1-leaf2a | Connectivity | VerifyReachability | Verifies point-to-point reachability between Ethernet interfaces. | ❌&nbsp;Failure | Destination 10.255.255.8 (dc1-spine1_Ethernet3) from 10.255.255.9 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address'<br>Destination 10.255.255.10 (dc1-spine2_Ethernet3) from 10.255.255.11 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address'<br>Destination 172.16.100.1 (dc2-leaf2a_Ethernet6) from 172.16.100.0 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address' |
| dc1-leaf2a | Interfaces | VerifyInterfaceDiscards | Verifies that the interfaces packet discard counters are equal to zero. | ❌&nbsp;Failure | Interface: Management1 - Non-zero discard counter(s): inDiscards: 53966 |
| dc1-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | ❌&nbsp;Failure | Interface: Loopback0 - Not configured<br>Interface: Loopback1 - Not configured<br>Interface: Loopback10 - Not configured<br>Interface: Loopback11 - Not configured<br>Interface: Port-Channel3 - Not configured<br>Interface: Port-Channel5 - Not configured<br>Interface: Port-Channel8 - Not configured<br>Interface: Vlan11 - Not configured<br>Interface: Vlan12 - Not configured<br>Interface: Vlan21 - Not configured<br>Interface: Vlan22 - Not configured<br>Interface: Vlan3009 - Not configured<br>Interface: Vlan3010 - Not configured<br>Interface: Vlan4093 - Not configured<br>Interface: Vlan4094 - Not configured<br>Interface: Vxlan1 - Not configured |
| dc1-leaf2a | Logging | VerifyLoggingErrors | Verifies there are no syslog messages with a severity of ERRORS or higher. | ❌&nbsp;Failure | Device has reported syslog messages with a severity of ERRORS or higher:<br>Jul 15 12:27:54 dc1-leaf2a NorCalInit: %HARDWARE-0-SYSTEM_IDENTIFICATION_FAILED: Failed to identify this system<br> <br> |
| dc1-leaf2b | BGP | VerifyBGPPeerSession | Verifies the session state of BGP peers. | ❌&nbsp;Failure | 'show bgp neighbors vrf all' failed on dc1-leaf2b: BGP inactive |
| dc1-leaf2b | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | ❌&nbsp;Failure | Port: Ethernet6 Neighbor: dc2-leaf2b Neighbor Port: Ethernet6 - Wrong LLDP neighbors: dc1-leaf2b.avd.lab/Ethernet6 |
| dc1-leaf2b | Connectivity | VerifyReachability | Verifies point-to-point reachability between Ethernet interfaces. | ❌&nbsp;Failure | Destination 10.255.255.12 (dc1-spine1_Ethernet4) from 10.255.255.13 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address'<br>Destination 10.255.255.14 (dc1-spine2_Ethernet4) from 10.255.255.15 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address'<br>Destination 172.16.100.3 (dc2-leaf2b_Ethernet6) from 172.16.100.2 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address' |
| dc1-leaf2b | Interfaces | VerifyInterfaceDiscards | Verifies that the interfaces packet discard counters are equal to zero. | ❌&nbsp;Failure | Interface: Management1 - Non-zero discard counter(s): inDiscards: 53966 |
| dc1-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | ❌&nbsp;Failure | Interface: Loopback0 - Not configured<br>Interface: Loopback1 - Not configured<br>Interface: Loopback10 - Not configured<br>Interface: Loopback11 - Not configured<br>Interface: Port-Channel3 - Not configured<br>Interface: Port-Channel5 - Not configured<br>Interface: Port-Channel8 - Not configured<br>Interface: Vlan11 - Not configured<br>Interface: Vlan12 - Not configured<br>Interface: Vlan21 - Not configured<br>Interface: Vlan22 - Not configured<br>Interface: Vlan3009 - Not configured<br>Interface: Vlan3010 - Not configured<br>Interface: Vlan4093 - Not configured<br>Interface: Vlan4094 - Not configured<br>Interface: Vxlan1 - Not configured |
| dc1-leaf2b | Logging | VerifyLoggingErrors | Verifies there are no syslog messages with a severity of ERRORS or higher. | ❌&nbsp;Failure | Device has reported syslog messages with a severity of ERRORS or higher:<br>Jul 15 12:27:54 dc1-leaf2b NorCalInit: %HARDWARE-0-SYSTEM_IDENTIFICATION_FAILED: Failed to identify this system<br> <br> |
| dc1-leaf2c | Configuration | VerifyRunningConfigDiffs | Verifies there is no difference between the running-config and the startup-config. | ❌&nbsp;Failure | --- flash:/startup-config<br>+++ system:/running-config<br>@@ -51,4 +51,11 @@<br> ntp server vrf MGMT 1.pool.ntp.org<br> ntp server vrf MGMT 2.pool.ntp.org<br> !<br>+router multicast<br>+   ipv4<br>+      software-forwarding kernel<br>+   !<br>+   ipv6<br>+      software-forwarding kernel<br>+!<br> end<br> |
| dc1-leaf2c | Interfaces | VerifyInterfaceDiscards | Verifies that the interfaces packet discard counters are equal to zero. | ❌&nbsp;Failure | Interface: Management1 - Non-zero discard counter(s): inDiscards: 53963 |
| dc1-leaf2c | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | ❌&nbsp;Failure | Interface: Port-Channel1 - Not configured |
| dc1-leaf2c | Logging | VerifyLoggingErrors | Verifies there are no syslog messages with a severity of ERRORS or higher. | ❌&nbsp;Failure | Device has reported syslog messages with a severity of ERRORS or higher:<br>Jul 15 12:27:51 dc1-leaf2c NorCalInit: %HARDWARE-0-SYSTEM_IDENTIFICATION_FAILED: Failed to identify this system<br> <br> |
| dc1-spine1 | BGP | VerifyBGPPeerSession | Verifies the session state of BGP peers. | ❌&nbsp;Failure | 'show bgp neighbors vrf all' failed on dc1-spine1: BGP inactive |
| dc1-spine1 | Configuration | VerifyRunningConfigDiffs | Verifies there is no difference between the running-config and the startup-config. | ❌&nbsp;Failure | --- flash:/startup-config<br>+++ system:/running-config<br>@@ -53,4 +53,11 @@<br> ntp server vrf MGMT 1.pool.ntp.org<br> ntp server vrf MGMT 2.pool.ntp.org<br> !<br>+router multicast<br>+   ipv4<br>+      software-forwarding kernel<br>+   !<br>+   ipv6<br>+      software-forwarding kernel<br>+!<br> end<br> |
| dc1-spine1 | Connectivity | VerifyReachability | Verifies point-to-point reachability between Ethernet interfaces. | ❌&nbsp;Failure | Destination 10.255.255.1 (dc1-leaf1a_Ethernet1) from 10.255.255.0 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address'<br>Destination 10.255.255.5 (dc1-leaf1b_Ethernet1) from 10.255.255.4 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address'<br>Destination 10.255.255.9 (dc1-leaf2a_Ethernet1) from 10.255.255.8 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address'<br>Destination 10.255.255.13 (dc1-leaf2b_Ethernet1) from 10.255.255.12 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address' |
| dc1-spine1 | Interfaces | VerifyInterfaceDiscards | Verifies that the interfaces packet discard counters are equal to zero. | ❌&nbsp;Failure | Interface: Management1 - Non-zero discard counter(s): inDiscards: 53923 |
| dc1-spine1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | ❌&nbsp;Failure | Interface: Loopback0 - Not configured |
| dc1-spine1 | Logging | VerifyLoggingErrors | Verifies there are no syslog messages with a severity of ERRORS or higher. | ❌&nbsp;Failure | Device has reported syslog messages with a severity of ERRORS or higher:<br>Jul 15 12:28:45 dc1-spine1 NorCalInit: %HARDWARE-0-SYSTEM_IDENTIFICATION_FAILED: Failed to identify this system<br> <br> |
| dc1-spine2 | BGP | VerifyBGPPeerSession | Verifies the session state of BGP peers. | ❌&nbsp;Failure | 'show bgp neighbors vrf all' failed on dc1-spine2: BGP inactive |
| dc1-spine2 | Connectivity | VerifyReachability | Verifies point-to-point reachability between Ethernet interfaces. | ❌&nbsp;Failure | Destination 10.255.255.3 (dc1-leaf1a_Ethernet2) from 10.255.255.2 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address'<br>Destination 10.255.255.7 (dc1-leaf1b_Ethernet2) from 10.255.255.6 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address'<br>Destination 10.255.255.11 (dc1-leaf2a_Ethernet2) from 10.255.255.10 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address'<br>Destination 10.255.255.15 (dc1-leaf2b_Ethernet2) from 10.255.255.14 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address' |
| dc1-spine2 | Interfaces | VerifyInterfaceDiscards | Verifies that the interfaces packet discard counters are equal to zero. | ❌&nbsp;Failure | Interface: Management1 - Non-zero discard counter(s): inDiscards: 53965 |
| dc1-spine2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | ❌&nbsp;Failure | Interface: Loopback0 - Not configured |
| dc1-spine2 | Logging | VerifyLoggingErrors | Verifies there are no syslog messages with a severity of ERRORS or higher. | ❌&nbsp;Failure | Device has reported syslog messages with a severity of ERRORS or higher:<br>Jul 15 12:27:53 dc1-spine2 NorCalInit: %HARDWARE-0-SYSTEM_IDENTIFICATION_FAILED: Failed to identify this system<br> <br> |
| dc2-leaf1a | BGP | VerifyBGPPeerSession | Verifies the session state of BGP peers. | ❌&nbsp;Failure | 'show bgp neighbors vrf all' failed on dc2-leaf1a: BGP inactive |
| dc2-leaf1a | Configuration | VerifyRunningConfigDiffs | Verifies there is no difference between the running-config and the startup-config. | ❌&nbsp;Failure | --- flash:/startup-config<br>+++ system:/running-config<br>@@ -1,4 +1,4 @@<br>-! device: dc2-leaf1a (cEOSLab, EOS-4.35.1F-45295350.4351F.1 (engineering build))<br>+! device: dc1-leaf1a (cEOSLab, EOS-4.35.1F-45295350.4351F.1 (engineering build))<br> !<br> no aaa root<br> !<br>@@ -57,4 +57,11 @@<br> ntp server vrf MGMT 1.pool.ntp.org<br> ntp server vrf MGMT 2.pool.ntp.org<br> !<br>+router multicast<br>+   ipv4<br>+      software-forwarding kernel<br>+   !<br>+   ipv6<br>+      software-forwarding kernel<br>+!<br> end<br> |
| dc2-leaf1a | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | ❌&nbsp;Failure | Port: Ethernet1 Neighbor: dc2-spine1 Neighbor Port: Ethernet1 - Wrong LLDP neighbors: dc1-spine1.avd.lab/Ethernet1<br>Port: Ethernet2 Neighbor: dc2-spine2 Neighbor Port: Ethernet1 - Wrong LLDP neighbors: dc1-spine2.avd.lab/Ethernet1<br>Port: Ethernet3 Neighbor: dc2-leaf1b Neighbor Port: Ethernet3 - Wrong LLDP neighbors: dc1-leaf1b.avd.lab/Ethernet3<br>Port: Ethernet4 Neighbor: dc2-leaf1b Neighbor Port: Ethernet4 - Wrong LLDP neighbors: dc1-leaf1b.avd.lab/Ethernet4<br>Port: Ethernet8 Neighbor: dc2-leaf1c Neighbor Port: Ethernet1 - Wrong LLDP neighbors: dc1-leaf1c.avd.lab/Ethernet1 |
| dc2-leaf1a | Connectivity | VerifyReachability | Verifies point-to-point reachability between Ethernet interfaces. | ❌&nbsp;Failure | Destination 10.255.255.64 (dc2-spine1_Ethernet1) from 10.255.255.65 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address'<br>Destination 10.255.255.66 (dc2-spine2_Ethernet1) from 10.255.255.67 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address' |
| dc2-leaf1a | Interfaces | VerifyInterfaceDiscards | Verifies that the interfaces packet discard counters are equal to zero. | ❌&nbsp;Failure | Interface: Management1 - Non-zero discard counter(s): inDiscards: 53940 |
| dc2-leaf1a | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | ❌&nbsp;Failure | Interface: Loopback0 - Not configured<br>Interface: Loopback1 - Not configured<br>Interface: Loopback10 - Not configured<br>Interface: Loopback11 - Not configured<br>Interface: Port-Channel3 - Not configured<br>Interface: Port-Channel5 - Not configured<br>Interface: Port-Channel8 - Not configured<br>Interface: Vlan11 - Not configured<br>Interface: Vlan12 - Not configured<br>Interface: Vlan21 - Not configured<br>Interface: Vlan22 - Not configured<br>Interface: Vlan3009 - Not configured<br>Interface: Vlan3010 - Not configured<br>Interface: Vlan4093 - Not configured<br>Interface: Vlan4094 - Not configured<br>Interface: Vxlan1 - Not configured |
| dc2-leaf1a | Logging | VerifyLoggingErrors | Verifies there are no syslog messages with a severity of ERRORS or higher. | ❌&nbsp;Failure | Device has reported syslog messages with a severity of ERRORS or higher:<br>Jul 15 12:28:40 dc2-leaf1a NorCalInit: %HARDWARE-0-SYSTEM_IDENTIFICATION_FAILED: Failed to identify this system<br> <br> |
| dc2-leaf1b | BGP | VerifyBGPPeerSession | Verifies the session state of BGP peers. | ❌&nbsp;Failure | 'show bgp neighbors vrf all' failed on dc2-leaf1b: BGP inactive |
| dc2-leaf1b | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | ❌&nbsp;Failure | Port: Ethernet1 Neighbor: dc2-spine1 Neighbor Port: Ethernet2 - Wrong LLDP neighbors: dc1-spine1.avd.lab/Ethernet2<br>Port: Ethernet2 Neighbor: dc2-spine2 Neighbor Port: Ethernet2 - Wrong LLDP neighbors: dc1-spine2.avd.lab/Ethernet2<br>Port: Ethernet3 Neighbor: dc2-leaf1a Neighbor Port: Ethernet3 - Wrong LLDP neighbors: dc1-leaf1a.avd.lab/Ethernet3<br>Port: Ethernet4 Neighbor: dc2-leaf1a Neighbor Port: Ethernet4 - Wrong LLDP neighbors: dc1-leaf1a.avd.lab/Ethernet4<br>Port: Ethernet8 Neighbor: dc2-leaf1c Neighbor Port: Ethernet2 - Wrong LLDP neighbors: dc1-leaf1c.avd.lab/Ethernet2 |
| dc2-leaf1b | Connectivity | VerifyReachability | Verifies point-to-point reachability between Ethernet interfaces. | ❌&nbsp;Failure | Destination 10.255.255.68 (dc2-spine1_Ethernet2) from 10.255.255.69 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address'<br>Destination 10.255.255.70 (dc2-spine2_Ethernet2) from 10.255.255.71 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address' |
| dc2-leaf1b | Interfaces | VerifyInterfaceDiscards | Verifies that the interfaces packet discard counters are equal to zero. | ❌&nbsp;Failure | Interface: Management1 - Non-zero discard counter(s): inDiscards: 53924 |
| dc2-leaf1b | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | ❌&nbsp;Failure | Interface: Loopback0 - Not configured<br>Interface: Loopback1 - Not configured<br>Interface: Loopback10 - Not configured<br>Interface: Loopback11 - Not configured<br>Interface: Port-Channel3 - Not configured<br>Interface: Port-Channel5 - Not configured<br>Interface: Port-Channel8 - Not configured<br>Interface: Vlan11 - Not configured<br>Interface: Vlan12 - Not configured<br>Interface: Vlan21 - Not configured<br>Interface: Vlan22 - Not configured<br>Interface: Vlan3009 - Not configured<br>Interface: Vlan3010 - Not configured<br>Interface: Vlan4093 - Not configured<br>Interface: Vlan4094 - Not configured<br>Interface: Vxlan1 - Not configured |
| dc2-leaf1b | Logging | VerifyLoggingErrors | Verifies there are no syslog messages with a severity of ERRORS or higher. | ❌&nbsp;Failure | Device has reported syslog messages with a severity of ERRORS or higher:<br>Jul 15 12:28:47 dc2-leaf1b NorCalInit: %HARDWARE-0-SYSTEM_IDENTIFICATION_FAILED: Failed to identify this system<br> <br> |
| dc2-leaf1c | Configuration | VerifyRunningConfigDiffs | Verifies there is no difference between the running-config and the startup-config. | ❌&nbsp;Failure | --- flash:/startup-config<br>+++ system:/running-config<br>@@ -1,4 +1,4 @@<br>-! device: dc2-leaf1c (cEOSLab, EOS-4.35.1F-45295350.4351F.1 (engineering build))<br>+! device: dc1-leaf1c (cEOSLab, EOS-4.35.1F-45295350.4351F.1 (engineering build))<br> !<br> no aaa root<br> !<br>@@ -51,4 +51,11 @@<br> ntp server vrf MGMT 1.pool.ntp.org<br> ntp server vrf MGMT 2.pool.ntp.org<br> !<br>+router multicast<br>+   ipv4<br>+      software-forwarding kernel<br>+   !<br>+   ipv6<br>+      software-forwarding kernel<br>+!<br> end<br> |
| dc2-leaf1c | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | ❌&nbsp;Failure | Port: Ethernet1 Neighbor: dc2-leaf1a Neighbor Port: Ethernet8 - Wrong LLDP neighbors: dc1-leaf1a.avd.lab/Ethernet8<br>Port: Ethernet2 Neighbor: dc2-leaf1b Neighbor Port: Ethernet8 - Wrong LLDP neighbors: dc1-leaf1b.avd.lab/Ethernet8 |
| dc2-leaf1c | Interfaces | VerifyInterfaceDiscards | Verifies that the interfaces packet discard counters are equal to zero. | ❌&nbsp;Failure | Interface: Management1 - Non-zero discard counter(s): inDiscards: 53923 |
| dc2-leaf1c | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | ❌&nbsp;Failure | Interface: Port-Channel1 - Not configured |
| dc2-leaf1c | Logging | VerifyLoggingErrors | Verifies there are no syslog messages with a severity of ERRORS or higher. | ❌&nbsp;Failure | Device has reported syslog messages with a severity of ERRORS or higher:<br>Jul 15 12:28:45 dc2-leaf1c NorCalInit: %HARDWARE-0-SYSTEM_IDENTIFICATION_FAILED: Failed to identify this system<br> <br> |
| dc2-leaf2a | BGP | VerifyBGPPeerSession | Verifies the session state of BGP peers. | ❌&nbsp;Failure | 'show bgp neighbors vrf all' failed on dc2-leaf2a: BGP inactive |
| dc2-leaf2a | Configuration | VerifyRunningConfigDiffs | Verifies there is no difference between the running-config and the startup-config. | ❌&nbsp;Failure | --- flash:/startup-config<br>+++ system:/running-config<br>@@ -1,4 +1,4 @@<br>-! device: dc2-leaf2a (cEOSLab, EOS-4.35.1F-45295350.4351F.1 (engineering build))<br>+! device: dc1-leaf2a (cEOSLab, EOS-4.35.1F-45295350.4351F.1 (engineering build))<br> !<br> no aaa root<br> !<br>@@ -59,4 +59,11 @@<br> ntp server vrf MGMT 1.pool.ntp.org<br> ntp server vrf MGMT 2.pool.ntp.org<br> !<br>+router multicast<br>+   ipv4<br>+      software-forwarding kernel<br>+   !<br>+   ipv6<br>+      software-forwarding kernel<br>+!<br> end<br> |
| dc2-leaf2a | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | ❌&nbsp;Failure | Port: Ethernet1 Neighbor: dc2-spine1 Neighbor Port: Ethernet3 - Wrong LLDP neighbors: dc1-spine1.avd.lab/Ethernet3<br>Port: Ethernet2 Neighbor: dc2-spine2 Neighbor Port: Ethernet3 - Wrong LLDP neighbors: dc1-spine2.avd.lab/Ethernet3<br>Port: Ethernet3 Neighbor: dc2-leaf2b Neighbor Port: Ethernet3 - Wrong LLDP neighbors: dc1-leaf2b.avd.lab/Ethernet3<br>Port: Ethernet4 Neighbor: dc2-leaf2b Neighbor Port: Ethernet4 - Wrong LLDP neighbors: dc1-leaf2b.avd.lab/Ethernet4<br>Port: Ethernet8 Neighbor: dc2-leaf2c Neighbor Port: Ethernet1 - Wrong LLDP neighbors: dc1-leaf2c.avd.lab/Ethernet1 |
| dc2-leaf2a | Connectivity | VerifyReachability | Verifies point-to-point reachability between Ethernet interfaces. | ❌&nbsp;Failure | Destination 10.255.255.72 (dc2-spine1_Ethernet3) from 10.255.255.73 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address'<br>Destination 10.255.255.74 (dc2-spine2_Ethernet3) from 10.255.255.75 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address'<br>Destination 172.16.100.0 (dc1-leaf2a_Ethernet6) from 172.16.100.1 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address' |
| dc2-leaf2a | Interfaces | VerifyInterfaceDiscards | Verifies that the interfaces packet discard counters are equal to zero. | ❌&nbsp;Failure | Interface: Management1 - Non-zero discard counter(s): inDiscards: 53967 |
| dc2-leaf2a | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | ❌&nbsp;Failure | Interface: Loopback0 - Not configured<br>Interface: Loopback1 - Not configured<br>Interface: Loopback10 - Not configured<br>Interface: Loopback11 - Not configured<br>Interface: Port-Channel3 - Not configured<br>Interface: Port-Channel5 - Not configured<br>Interface: Port-Channel8 - Not configured<br>Interface: Vlan11 - Not configured<br>Interface: Vlan12 - Not configured<br>Interface: Vlan21 - Not configured<br>Interface: Vlan22 - Not configured<br>Interface: Vlan3009 - Not configured<br>Interface: Vlan3010 - Not configured<br>Interface: Vlan4093 - Not configured<br>Interface: Vlan4094 - Not configured<br>Interface: Vxlan1 - Not configured |
| dc2-leaf2a | Logging | VerifyLoggingErrors | Verifies there are no syslog messages with a severity of ERRORS or higher. | ❌&nbsp;Failure | Device has reported syslog messages with a severity of ERRORS or higher:<br>Jul 15 12:27:55 dc2-leaf2a NorCalInit: %HARDWARE-0-SYSTEM_IDENTIFICATION_FAILED: Failed to identify this system<br> <br> |
| dc2-leaf2b | BGP | VerifyBGPPeerSession | Verifies the session state of BGP peers. | ❌&nbsp;Failure | 'show bgp neighbors vrf all' failed on dc2-leaf2b: BGP inactive |
| dc2-leaf2b | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | ❌&nbsp;Failure | Port: Ethernet1 Neighbor: dc2-spine1 Neighbor Port: Ethernet4 - Wrong LLDP neighbors: dc1-spine1.avd.lab/Ethernet4<br>Port: Ethernet2 Neighbor: dc2-spine2 Neighbor Port: Ethernet4 - Wrong LLDP neighbors: dc1-spine2.avd.lab/Ethernet4<br>Port: Ethernet3 Neighbor: dc2-leaf2a Neighbor Port: Ethernet3 - Wrong LLDP neighbors: dc1-leaf2a.avd.lab/Ethernet3<br>Port: Ethernet4 Neighbor: dc2-leaf2a Neighbor Port: Ethernet4 - Wrong LLDP neighbors: dc1-leaf2a.avd.lab/Ethernet4<br>Port: Ethernet8 Neighbor: dc2-leaf2c Neighbor Port: Ethernet2 - Wrong LLDP neighbors: dc1-leaf2c.avd.lab/Ethernet2 |
| dc2-leaf2b | Connectivity | VerifyReachability | Verifies point-to-point reachability between Ethernet interfaces. | ❌&nbsp;Failure | Destination 10.255.255.76 (dc2-spine1_Ethernet4) from 10.255.255.77 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address'<br>Destination 10.255.255.78 (dc2-spine2_Ethernet4) from 10.255.255.79 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address'<br>Destination 172.16.100.2 (dc1-leaf2b_Ethernet6) from 172.16.100.3 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address' |
| dc2-leaf2b | Interfaces | VerifyInterfaceDiscards | Verifies that the interfaces packet discard counters are equal to zero. | ❌&nbsp;Failure | Interface: Management1 - Non-zero discard counter(s): inDiscards: 53965 |
| dc2-leaf2b | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | ❌&nbsp;Failure | Interface: Loopback0 - Not configured<br>Interface: Loopback1 - Not configured<br>Interface: Loopback10 - Not configured<br>Interface: Loopback11 - Not configured<br>Interface: Port-Channel3 - Not configured<br>Interface: Port-Channel5 - Not configured<br>Interface: Port-Channel8 - Not configured<br>Interface: Vlan11 - Not configured<br>Interface: Vlan12 - Not configured<br>Interface: Vlan21 - Not configured<br>Interface: Vlan22 - Not configured<br>Interface: Vlan3009 - Not configured<br>Interface: Vlan3010 - Not configured<br>Interface: Vlan4093 - Not configured<br>Interface: Vlan4094 - Not configured<br>Interface: Vxlan1 - Not configured |
| dc2-leaf2b | Logging | VerifyLoggingErrors | Verifies there are no syslog messages with a severity of ERRORS or higher. | ❌&nbsp;Failure | Device has reported syslog messages with a severity of ERRORS or higher:<br>Jul 15 12:27:53 dc2-leaf2b NorCalInit: %HARDWARE-0-SYSTEM_IDENTIFICATION_FAILED: Failed to identify this system<br> <br> |
| dc2-leaf2c | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | ❌&nbsp;Failure | Port: Ethernet1 Neighbor: dc2-leaf2a Neighbor Port: Ethernet8 - Wrong LLDP neighbors: dc1-leaf2a.avd.lab/Ethernet8<br>Port: Ethernet2 Neighbor: dc2-leaf2b Neighbor Port: Ethernet8 - Wrong LLDP neighbors: dc1-leaf2b.avd.lab/Ethernet8 |
| dc2-leaf2c | Interfaces | VerifyInterfaceDiscards | Verifies that the interfaces packet discard counters are equal to zero. | ❌&nbsp;Failure | Interface: Management1 - Non-zero discard counter(s): inDiscards: 53923 |
| dc2-leaf2c | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | ❌&nbsp;Failure | Interface: Port-Channel1 - Not configured |
| dc2-leaf2c | Logging | VerifyLoggingErrors | Verifies there are no syslog messages with a severity of ERRORS or higher. | ❌&nbsp;Failure | Device has reported syslog messages with a severity of ERRORS or higher:<br>Jul 15 12:28:46 dc2-leaf2c NorCalInit: %HARDWARE-0-SYSTEM_IDENTIFICATION_FAILED: Failed to identify this system<br> <br> |
| dc2-spine1 | BGP | VerifyBGPPeerSession | Verifies the session state of BGP peers. | ❌&nbsp;Failure | 'show bgp neighbors vrf all' failed on dc2-spine1: BGP inactive |
| dc2-spine1 | Configuration | VerifyRunningConfigDiffs | Verifies there is no difference between the running-config and the startup-config. | ❌&nbsp;Failure | --- flash:/startup-config<br>+++ system:/running-config<br>@@ -1,4 +1,4 @@<br>-! device: dc2-spine1 (cEOSLab, EOS-4.35.1F-45295350.4351F.1 (engineering build))<br>+! device: dc1-spine1 (cEOSLab, EOS-4.35.1F-45295350.4351F.1 (engineering build))<br> !<br> no aaa root<br> !<br>@@ -53,4 +53,11 @@<br> ntp server vrf MGMT 1.pool.ntp.org<br> ntp server vrf MGMT 2.pool.ntp.org<br> !<br>+router multicast<br>+   ipv4<br>+      software-forwarding kernel<br>+   !<br>+   ipv6<br>+      software-forwarding kernel<br>+!<br> end<br> |
| dc2-spine1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | ❌&nbsp;Failure | Port: Ethernet1 Neighbor: dc2-leaf1a Neighbor Port: Ethernet1 - Wrong LLDP neighbors: dc1-leaf1a.avd.lab/Ethernet1<br>Port: Ethernet2 Neighbor: dc2-leaf1b Neighbor Port: Ethernet1 - Wrong LLDP neighbors: dc1-leaf1b.avd.lab/Ethernet1<br>Port: Ethernet3 Neighbor: dc2-leaf2a Neighbor Port: Ethernet1 - Wrong LLDP neighbors: dc1-leaf2a.avd.lab/Ethernet1<br>Port: Ethernet4 Neighbor: dc2-leaf2b Neighbor Port: Ethernet1 - Wrong LLDP neighbors: dc1-leaf2b.avd.lab/Ethernet1 |
| dc2-spine1 | Connectivity | VerifyReachability | Verifies point-to-point reachability between Ethernet interfaces. | ❌&nbsp;Failure | Destination 10.255.255.65 (dc2-leaf1a_Ethernet1) from 10.255.255.64 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address'<br>Destination 10.255.255.69 (dc2-leaf1b_Ethernet1) from 10.255.255.68 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address'<br>Destination 10.255.255.73 (dc2-leaf2a_Ethernet1) from 10.255.255.72 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address'<br>Destination 10.255.255.77 (dc2-leaf2b_Ethernet1) from 10.255.255.76 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address' |
| dc2-spine1 | Interfaces | VerifyInterfaceDiscards | Verifies that the interfaces packet discard counters are equal to zero. | ❌&nbsp;Failure | Interface: Management1 - Non-zero discard counter(s): inDiscards: 53932 |
| dc2-spine1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | ❌&nbsp;Failure | Interface: Loopback0 - Not configured |
| dc2-spine1 | Logging | VerifyLoggingErrors | Verifies there are no syslog messages with a severity of ERRORS or higher. | ❌&nbsp;Failure | Device has reported syslog messages with a severity of ERRORS or higher:<br>Jul 15 12:28:42 dc2-spine1 NorCalInit: %HARDWARE-0-SYSTEM_IDENTIFICATION_FAILED: Failed to identify this system<br> <br> |
| dc2-spine2 | BGP | VerifyBGPPeerSession | Verifies the session state of BGP peers. | ❌&nbsp;Failure | 'show bgp neighbors vrf all' failed on dc2-spine2: BGP inactive |
| dc2-spine2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | ❌&nbsp;Failure | Port: Ethernet1 Neighbor: dc2-leaf1a Neighbor Port: Ethernet2 - Wrong LLDP neighbors: dc1-leaf1a.avd.lab/Ethernet2<br>Port: Ethernet2 Neighbor: dc2-leaf1b Neighbor Port: Ethernet2 - Wrong LLDP neighbors: dc1-leaf1b.avd.lab/Ethernet2<br>Port: Ethernet3 Neighbor: dc2-leaf2a Neighbor Port: Ethernet2 - Wrong LLDP neighbors: dc1-leaf2a.avd.lab/Ethernet2<br>Port: Ethernet4 Neighbor: dc2-leaf2b Neighbor Port: Ethernet2 - Wrong LLDP neighbors: dc1-leaf2b.avd.lab/Ethernet2 |
| dc2-spine2 | Connectivity | VerifyReachability | Verifies point-to-point reachability between Ethernet interfaces. | ❌&nbsp;Failure | Destination 10.255.255.67 (dc2-leaf1a_Ethernet2) from 10.255.255.66 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address'<br>Destination 10.255.255.71 (dc2-leaf1b_Ethernet2) from 10.255.255.70 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address'<br>Destination 10.255.255.75 (dc2-leaf2a_Ethernet2) from 10.255.255.74 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address'<br>Destination 10.255.255.79 (dc2-leaf2b_Ethernet2) from 10.255.255.78 in VRF default - Error when executing ping: 'ping: bind: Cannot assign requested address' |
| dc2-spine2 | Interfaces | VerifyInterfaceDiscards | Verifies that the interfaces packet discard counters are equal to zero. | ❌&nbsp;Failure | Interface: Management1 - Non-zero discard counter(s): inDiscards: 53924 |
| dc2-spine2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | ❌&nbsp;Failure | Interface: Loopback0 - Not configured |
| dc2-spine2 | Logging | VerifyLoggingErrors | Verifies there are no syslog messages with a severity of ERRORS or higher. | ❌&nbsp;Failure | Device has reported syslog messages with a severity of ERRORS or higher:<br>Jul 15 12:28:46 dc2-spine2 NorCalInit: %HARDWARE-0-SYSTEM_IDENTIFICATION_FAILED: Failed to identify this system<br> <br> |
| dc1-leaf1a | MLAG | VerifyMlagConfigSanity | Verifies there are no MLAG config-sanity inconsistencies. | ⏭️&nbsp;Skipped | MLAG is disabled |
| dc1-leaf1a | MLAG | VerifyMlagInterfaces | Verifies there are no inactive or active-partial MLAG ports. | ⏭️&nbsp;Skipped | MLAG is disabled |
| dc1-leaf1a | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | ⏭️&nbsp;Skipped | MLAG is disabled |
| dc1-leaf1a | VXLAN | VerifyVxlanConfigSanity | Verifies there are no VXLAN config-sanity inconsistencies. | ⏭️&nbsp;Skipped | VXLAN is not configured |
| dc1-leaf1b | MLAG | VerifyMlagConfigSanity | Verifies there are no MLAG config-sanity inconsistencies. | ⏭️&nbsp;Skipped | MLAG is disabled |
| dc1-leaf1b | MLAG | VerifyMlagInterfaces | Verifies there are no inactive or active-partial MLAG ports. | ⏭️&nbsp;Skipped | MLAG is disabled |
| dc1-leaf1b | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | ⏭️&nbsp;Skipped | MLAG is disabled |
| dc1-leaf1b | VXLAN | VerifyVxlanConfigSanity | Verifies there are no VXLAN config-sanity inconsistencies. | ⏭️&nbsp;Skipped | VXLAN is not configured |
| dc1-leaf2a | MLAG | VerifyMlagConfigSanity | Verifies there are no MLAG config-sanity inconsistencies. | ⏭️&nbsp;Skipped | MLAG is disabled |
| dc1-leaf2a | MLAG | VerifyMlagInterfaces | Verifies there are no inactive or active-partial MLAG ports. | ⏭️&nbsp;Skipped | MLAG is disabled |
| dc1-leaf2a | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | ⏭️&nbsp;Skipped | MLAG is disabled |
| dc1-leaf2a | VXLAN | VerifyVxlanConfigSanity | Verifies there are no VXLAN config-sanity inconsistencies. | ⏭️&nbsp;Skipped | VXLAN is not configured |
| dc1-leaf2b | MLAG | VerifyMlagConfigSanity | Verifies there are no MLAG config-sanity inconsistencies. | ⏭️&nbsp;Skipped | MLAG is disabled |
| dc1-leaf2b | MLAG | VerifyMlagInterfaces | Verifies there are no inactive or active-partial MLAG ports. | ⏭️&nbsp;Skipped | MLAG is disabled |
| dc1-leaf2b | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | ⏭️&nbsp;Skipped | MLAG is disabled |
| dc1-leaf2b | VXLAN | VerifyVxlanConfigSanity | Verifies there are no VXLAN config-sanity inconsistencies. | ⏭️&nbsp;Skipped | VXLAN is not configured |
| dc2-leaf1a | MLAG | VerifyMlagConfigSanity | Verifies there are no MLAG config-sanity inconsistencies. | ⏭️&nbsp;Skipped | MLAG is disabled |
| dc2-leaf1a | MLAG | VerifyMlagInterfaces | Verifies there are no inactive or active-partial MLAG ports. | ⏭️&nbsp;Skipped | MLAG is disabled |
| dc2-leaf1a | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | ⏭️&nbsp;Skipped | MLAG is disabled |
| dc2-leaf1a | VXLAN | VerifyVxlanConfigSanity | Verifies there are no VXLAN config-sanity inconsistencies. | ⏭️&nbsp;Skipped | VXLAN is not configured |
| dc2-leaf1b | MLAG | VerifyMlagConfigSanity | Verifies there are no MLAG config-sanity inconsistencies. | ⏭️&nbsp;Skipped | MLAG is disabled |
| dc2-leaf1b | MLAG | VerifyMlagInterfaces | Verifies there are no inactive or active-partial MLAG ports. | ⏭️&nbsp;Skipped | MLAG is disabled |
| dc2-leaf1b | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | ⏭️&nbsp;Skipped | MLAG is disabled |
| dc2-leaf1b | VXLAN | VerifyVxlanConfigSanity | Verifies there are no VXLAN config-sanity inconsistencies. | ⏭️&nbsp;Skipped | VXLAN is not configured |
| dc2-leaf2a | MLAG | VerifyMlagConfigSanity | Verifies there are no MLAG config-sanity inconsistencies. | ⏭️&nbsp;Skipped | MLAG is disabled |
| dc2-leaf2a | MLAG | VerifyMlagInterfaces | Verifies there are no inactive or active-partial MLAG ports. | ⏭️&nbsp;Skipped | MLAG is disabled |
| dc2-leaf2a | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | ⏭️&nbsp;Skipped | MLAG is disabled |
| dc2-leaf2a | VXLAN | VerifyVxlanConfigSanity | Verifies there are no VXLAN config-sanity inconsistencies. | ⏭️&nbsp;Skipped | VXLAN is not configured |
| dc2-leaf2b | MLAG | VerifyMlagConfigSanity | Verifies there are no MLAG config-sanity inconsistencies. | ⏭️&nbsp;Skipped | MLAG is disabled |
| dc2-leaf2b | MLAG | VerifyMlagInterfaces | Verifies there are no inactive or active-partial MLAG ports. | ⏭️&nbsp;Skipped | MLAG is disabled |
| dc2-leaf2b | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | ⏭️&nbsp;Skipped | MLAG is disabled |
| dc2-leaf2b | VXLAN | VerifyVxlanConfigSanity | Verifies there are no VXLAN config-sanity inconsistencies. | ⏭️&nbsp;Skipped | VXLAN is not configured |
| dc1-leaf1a | Configuration | VerifyRunningConfigDiffs | Verifies there is no difference between the running-config and the startup-config. | ✅&nbsp;Success | - |
| dc1-leaf1a | Configuration | VerifyZeroTouch | Verifies ZeroTouch is disabled. | ✅&nbsp;Success | - |
| dc1-leaf1a | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | ✅&nbsp;Success | - |
| dc1-leaf1a | Interfaces | VerifyIllegalLACP | Verifies there are no illegal LACP packets in port channels. | ✅&nbsp;Success | - |
| dc1-leaf1a | Interfaces | VerifyInterfaceErrDisabled | Verifies there are no interfaces in the errdisabled state. | ✅&nbsp;Success | - |
| dc1-leaf1a | Interfaces | VerifyInterfaceErrors | Verifies that the interfaces error counters are equal to zero. | ✅&nbsp;Success | - |
| dc1-leaf1a | Interfaces | VerifyInterfaceUtilization | Verifies that the utilization of interfaces is below a certain threshold. | ✅&nbsp;Success | - |
| dc1-leaf1a | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | ✅&nbsp;Success | - |
| dc1-leaf1a | STP | VerifySTPCounters | Verifies there is no errors in STP BPDU packets. | ✅&nbsp;Success | - |
| dc1-leaf1a | System | VerifyAgentLogs | Verifies there are no agent crash reports. | ✅&nbsp;Success | - |
| dc1-leaf1a | System | VerifyCoredump | Verifies there are no core dump files. | ✅&nbsp;Success | - |
| dc1-leaf1a | System | VerifyFileSystemUtilization | Verifies that no partition is utilizing more than 75% of its disk space. | ✅&nbsp;Success | - |
| dc1-leaf1a | System | VerifyMaintenance | Verifies that the device is not currently under or entering maintenance. | ✅&nbsp;Success | - |
| dc1-leaf1a | System | VerifyMemoryUtilization | Verifies whether the memory utilization is below 75%. | ✅&nbsp;Success | - |
| dc1-leaf1a | System | VerifyNTP | Verifies if NTP is synchronised. | ✅&nbsp;Success | - |
| dc1-leaf1a | System | VerifyReloadCause | Verifies the last reload cause of the device. | ✅&nbsp;Success | - |
| dc1-leaf1b | Configuration | VerifyRunningConfigDiffs | Verifies there is no difference between the running-config and the startup-config. | ✅&nbsp;Success | - |
| dc1-leaf1b | Configuration | VerifyZeroTouch | Verifies ZeroTouch is disabled. | ✅&nbsp;Success | - |
| dc1-leaf1b | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | ✅&nbsp;Success | - |
| dc1-leaf1b | Interfaces | VerifyIllegalLACP | Verifies there are no illegal LACP packets in port channels. | ✅&nbsp;Success | - |
| dc1-leaf1b | Interfaces | VerifyInterfaceErrDisabled | Verifies there are no interfaces in the errdisabled state. | ✅&nbsp;Success | - |
| dc1-leaf1b | Interfaces | VerifyInterfaceErrors | Verifies that the interfaces error counters are equal to zero. | ✅&nbsp;Success | - |
| dc1-leaf1b | Interfaces | VerifyInterfaceUtilization | Verifies that the utilization of interfaces is below a certain threshold. | ✅&nbsp;Success | - |
| dc1-leaf1b | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | ✅&nbsp;Success | - |
| dc1-leaf1b | STP | VerifySTPCounters | Verifies there is no errors in STP BPDU packets. | ✅&nbsp;Success | - |
| dc1-leaf1b | System | VerifyAgentLogs | Verifies there are no agent crash reports. | ✅&nbsp;Success | - |
| dc1-leaf1b | System | VerifyCoredump | Verifies there are no core dump files. | ✅&nbsp;Success | - |
| dc1-leaf1b | System | VerifyFileSystemUtilization | Verifies that no partition is utilizing more than 75% of its disk space. | ✅&nbsp;Success | - |
| dc1-leaf1b | System | VerifyMaintenance | Verifies that the device is not currently under or entering maintenance. | ✅&nbsp;Success | - |
| dc1-leaf1b | System | VerifyMemoryUtilization | Verifies whether the memory utilization is below 75%. | ✅&nbsp;Success | - |
| dc1-leaf1b | System | VerifyNTP | Verifies if NTP is synchronised. | ✅&nbsp;Success | - |
| dc1-leaf1b | System | VerifyReloadCause | Verifies the last reload cause of the device. | ✅&nbsp;Success | - |
| dc1-leaf1c | Configuration | VerifyRunningConfigDiffs | Verifies there is no difference between the running-config and the startup-config. | ✅&nbsp;Success | - |
| dc1-leaf1c | Configuration | VerifyZeroTouch | Verifies ZeroTouch is disabled. | ✅&nbsp;Success | - |
| dc1-leaf1c | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | ✅&nbsp;Success | - |
| dc1-leaf1c | Interfaces | VerifyIllegalLACP | Verifies there are no illegal LACP packets in port channels. | ✅&nbsp;Success | - |
| dc1-leaf1c | Interfaces | VerifyInterfaceErrDisabled | Verifies there are no interfaces in the errdisabled state. | ✅&nbsp;Success | - |
| dc1-leaf1c | Interfaces | VerifyInterfaceErrors | Verifies that the interfaces error counters are equal to zero. | ✅&nbsp;Success | - |
| dc1-leaf1c | Interfaces | VerifyInterfaceUtilization | Verifies that the utilization of interfaces is below a certain threshold. | ✅&nbsp;Success | - |
| dc1-leaf1c | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | ✅&nbsp;Success | - |
| dc1-leaf1c | STP | VerifySTPCounters | Verifies there is no errors in STP BPDU packets. | ✅&nbsp;Success | - |
| dc1-leaf1c | System | VerifyAgentLogs | Verifies there are no agent crash reports. | ✅&nbsp;Success | - |
| dc1-leaf1c | System | VerifyCoredump | Verifies there are no core dump files. | ✅&nbsp;Success | - |
| dc1-leaf1c | System | VerifyFileSystemUtilization | Verifies that no partition is utilizing more than 75% of its disk space. | ✅&nbsp;Success | - |
| dc1-leaf1c | System | VerifyMaintenance | Verifies that the device is not currently under or entering maintenance. | ✅&nbsp;Success | - |
| dc1-leaf1c | System | VerifyMemoryUtilization | Verifies whether the memory utilization is below 75%. | ✅&nbsp;Success | - |
| dc1-leaf1c | System | VerifyNTP | Verifies if NTP is synchronised. | ✅&nbsp;Success | - |
| dc1-leaf1c | System | VerifyReloadCause | Verifies the last reload cause of the device. | ✅&nbsp;Success | - |
| dc1-leaf2a | Configuration | VerifyRunningConfigDiffs | Verifies there is no difference between the running-config and the startup-config. | ✅&nbsp;Success | - |
| dc1-leaf2a | Configuration | VerifyZeroTouch | Verifies ZeroTouch is disabled. | ✅&nbsp;Success | - |
| dc1-leaf2a | Interfaces | VerifyIllegalLACP | Verifies there are no illegal LACP packets in port channels. | ✅&nbsp;Success | - |
| dc1-leaf2a | Interfaces | VerifyInterfaceErrDisabled | Verifies there are no interfaces in the errdisabled state. | ✅&nbsp;Success | - |
| dc1-leaf2a | Interfaces | VerifyInterfaceErrors | Verifies that the interfaces error counters are equal to zero. | ✅&nbsp;Success | - |
| dc1-leaf2a | Interfaces | VerifyInterfaceUtilization | Verifies that the utilization of interfaces is below a certain threshold. | ✅&nbsp;Success | - |
| dc1-leaf2a | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | ✅&nbsp;Success | - |
| dc1-leaf2a | STP | VerifySTPCounters | Verifies there is no errors in STP BPDU packets. | ✅&nbsp;Success | - |
| dc1-leaf2a | System | VerifyAgentLogs | Verifies there are no agent crash reports. | ✅&nbsp;Success | - |
| dc1-leaf2a | System | VerifyCoredump | Verifies there are no core dump files. | ✅&nbsp;Success | - |
| dc1-leaf2a | System | VerifyFileSystemUtilization | Verifies that no partition is utilizing more than 75% of its disk space. | ✅&nbsp;Success | - |
| dc1-leaf2a | System | VerifyMaintenance | Verifies that the device is not currently under or entering maintenance. | ✅&nbsp;Success | - |
| dc1-leaf2a | System | VerifyMemoryUtilization | Verifies whether the memory utilization is below 75%. | ✅&nbsp;Success | - |
| dc1-leaf2a | System | VerifyNTP | Verifies if NTP is synchronised. | ✅&nbsp;Success | - |
| dc1-leaf2a | System | VerifyReloadCause | Verifies the last reload cause of the device. | ✅&nbsp;Success | - |
| dc1-leaf2b | Configuration | VerifyRunningConfigDiffs | Verifies there is no difference between the running-config and the startup-config. | ✅&nbsp;Success | - |
| dc1-leaf2b | Configuration | VerifyZeroTouch | Verifies ZeroTouch is disabled. | ✅&nbsp;Success | - |
| dc1-leaf2b | Interfaces | VerifyIllegalLACP | Verifies there are no illegal LACP packets in port channels. | ✅&nbsp;Success | - |
| dc1-leaf2b | Interfaces | VerifyInterfaceErrDisabled | Verifies there are no interfaces in the errdisabled state. | ✅&nbsp;Success | - |
| dc1-leaf2b | Interfaces | VerifyInterfaceErrors | Verifies that the interfaces error counters are equal to zero. | ✅&nbsp;Success | - |
| dc1-leaf2b | Interfaces | VerifyInterfaceUtilization | Verifies that the utilization of interfaces is below a certain threshold. | ✅&nbsp;Success | - |
| dc1-leaf2b | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | ✅&nbsp;Success | - |
| dc1-leaf2b | STP | VerifySTPCounters | Verifies there is no errors in STP BPDU packets. | ✅&nbsp;Success | - |
| dc1-leaf2b | System | VerifyAgentLogs | Verifies there are no agent crash reports. | ✅&nbsp;Success | - |
| dc1-leaf2b | System | VerifyCoredump | Verifies there are no core dump files. | ✅&nbsp;Success | - |
| dc1-leaf2b | System | VerifyFileSystemUtilization | Verifies that no partition is utilizing more than 75% of its disk space. | ✅&nbsp;Success | - |
| dc1-leaf2b | System | VerifyMaintenance | Verifies that the device is not currently under or entering maintenance. | ✅&nbsp;Success | - |
| dc1-leaf2b | System | VerifyMemoryUtilization | Verifies whether the memory utilization is below 75%. | ✅&nbsp;Success | - |
| dc1-leaf2b | System | VerifyNTP | Verifies if NTP is synchronised. | ✅&nbsp;Success | - |
| dc1-leaf2b | System | VerifyReloadCause | Verifies the last reload cause of the device. | ✅&nbsp;Success | - |
| dc1-leaf2c | Configuration | VerifyZeroTouch | Verifies ZeroTouch is disabled. | ✅&nbsp;Success | - |
| dc1-leaf2c | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | ✅&nbsp;Success | - |
| dc1-leaf2c | Interfaces | VerifyIllegalLACP | Verifies there are no illegal LACP packets in port channels. | ✅&nbsp;Success | - |
| dc1-leaf2c | Interfaces | VerifyInterfaceErrDisabled | Verifies there are no interfaces in the errdisabled state. | ✅&nbsp;Success | - |
| dc1-leaf2c | Interfaces | VerifyInterfaceErrors | Verifies that the interfaces error counters are equal to zero. | ✅&nbsp;Success | - |
| dc1-leaf2c | Interfaces | VerifyInterfaceUtilization | Verifies that the utilization of interfaces is below a certain threshold. | ✅&nbsp;Success | - |
| dc1-leaf2c | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | ✅&nbsp;Success | - |
| dc1-leaf2c | STP | VerifySTPCounters | Verifies there is no errors in STP BPDU packets. | ✅&nbsp;Success | - |
| dc1-leaf2c | System | VerifyAgentLogs | Verifies there are no agent crash reports. | ✅&nbsp;Success | - |
| dc1-leaf2c | System | VerifyCoredump | Verifies there are no core dump files. | ✅&nbsp;Success | - |
| dc1-leaf2c | System | VerifyFileSystemUtilization | Verifies that no partition is utilizing more than 75% of its disk space. | ✅&nbsp;Success | - |
| dc1-leaf2c | System | VerifyMaintenance | Verifies that the device is not currently under or entering maintenance. | ✅&nbsp;Success | - |
| dc1-leaf2c | System | VerifyMemoryUtilization | Verifies whether the memory utilization is below 75%. | ✅&nbsp;Success | - |
| dc1-leaf2c | System | VerifyNTP | Verifies if NTP is synchronised. | ✅&nbsp;Success | - |
| dc1-leaf2c | System | VerifyReloadCause | Verifies the last reload cause of the device. | ✅&nbsp;Success | - |
| dc1-spine1 | Configuration | VerifyZeroTouch | Verifies ZeroTouch is disabled. | ✅&nbsp;Success | - |
| dc1-spine1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | ✅&nbsp;Success | - |
| dc1-spine1 | Interfaces | VerifyInterfaceErrDisabled | Verifies there are no interfaces in the errdisabled state. | ✅&nbsp;Success | - |
| dc1-spine1 | Interfaces | VerifyInterfaceErrors | Verifies that the interfaces error counters are equal to zero. | ✅&nbsp;Success | - |
| dc1-spine1 | Interfaces | VerifyInterfaceUtilization | Verifies that the utilization of interfaces is below a certain threshold. | ✅&nbsp;Success | - |
| dc1-spine1 | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | ✅&nbsp;Success | - |
| dc1-spine1 | STP | VerifySTPCounters | Verifies there is no errors in STP BPDU packets. | ✅&nbsp;Success | - |
| dc1-spine1 | System | VerifyAgentLogs | Verifies there are no agent crash reports. | ✅&nbsp;Success | - |
| dc1-spine1 | System | VerifyCoredump | Verifies there are no core dump files. | ✅&nbsp;Success | - |
| dc1-spine1 | System | VerifyFileSystemUtilization | Verifies that no partition is utilizing more than 75% of its disk space. | ✅&nbsp;Success | - |
| dc1-spine1 | System | VerifyMaintenance | Verifies that the device is not currently under or entering maintenance. | ✅&nbsp;Success | - |
| dc1-spine1 | System | VerifyMemoryUtilization | Verifies whether the memory utilization is below 75%. | ✅&nbsp;Success | - |
| dc1-spine1 | System | VerifyNTP | Verifies if NTP is synchronised. | ✅&nbsp;Success | - |
| dc1-spine1 | System | VerifyReloadCause | Verifies the last reload cause of the device. | ✅&nbsp;Success | - |
| dc1-spine2 | Configuration | VerifyRunningConfigDiffs | Verifies there is no difference between the running-config and the startup-config. | ✅&nbsp;Success | - |
| dc1-spine2 | Configuration | VerifyZeroTouch | Verifies ZeroTouch is disabled. | ✅&nbsp;Success | - |
| dc1-spine2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | ✅&nbsp;Success | - |
| dc1-spine2 | Interfaces | VerifyInterfaceErrDisabled | Verifies there are no interfaces in the errdisabled state. | ✅&nbsp;Success | - |
| dc1-spine2 | Interfaces | VerifyInterfaceErrors | Verifies that the interfaces error counters are equal to zero. | ✅&nbsp;Success | - |
| dc1-spine2 | Interfaces | VerifyInterfaceUtilization | Verifies that the utilization of interfaces is below a certain threshold. | ✅&nbsp;Success | - |
| dc1-spine2 | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | ✅&nbsp;Success | - |
| dc1-spine2 | STP | VerifySTPCounters | Verifies there is no errors in STP BPDU packets. | ✅&nbsp;Success | - |
| dc1-spine2 | System | VerifyAgentLogs | Verifies there are no agent crash reports. | ✅&nbsp;Success | - |
| dc1-spine2 | System | VerifyCoredump | Verifies there are no core dump files. | ✅&nbsp;Success | - |
| dc1-spine2 | System | VerifyFileSystemUtilization | Verifies that no partition is utilizing more than 75% of its disk space. | ✅&nbsp;Success | - |
| dc1-spine2 | System | VerifyMaintenance | Verifies that the device is not currently under or entering maintenance. | ✅&nbsp;Success | - |
| dc1-spine2 | System | VerifyMemoryUtilization | Verifies whether the memory utilization is below 75%. | ✅&nbsp;Success | - |
| dc1-spine2 | System | VerifyNTP | Verifies if NTP is synchronised. | ✅&nbsp;Success | - |
| dc1-spine2 | System | VerifyReloadCause | Verifies the last reload cause of the device. | ✅&nbsp;Success | - |
| dc2-leaf1a | Configuration | VerifyZeroTouch | Verifies ZeroTouch is disabled. | ✅&nbsp;Success | - |
| dc2-leaf1a | Interfaces | VerifyIllegalLACP | Verifies there are no illegal LACP packets in port channels. | ✅&nbsp;Success | - |
| dc2-leaf1a | Interfaces | VerifyInterfaceErrDisabled | Verifies there are no interfaces in the errdisabled state. | ✅&nbsp;Success | - |
| dc2-leaf1a | Interfaces | VerifyInterfaceErrors | Verifies that the interfaces error counters are equal to zero. | ✅&nbsp;Success | - |
| dc2-leaf1a | Interfaces | VerifyInterfaceUtilization | Verifies that the utilization of interfaces is below a certain threshold. | ✅&nbsp;Success | - |
| dc2-leaf1a | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | ✅&nbsp;Success | - |
| dc2-leaf1a | STP | VerifySTPCounters | Verifies there is no errors in STP BPDU packets. | ✅&nbsp;Success | - |
| dc2-leaf1a | System | VerifyAgentLogs | Verifies there are no agent crash reports. | ✅&nbsp;Success | - |
| dc2-leaf1a | System | VerifyCoredump | Verifies there are no core dump files. | ✅&nbsp;Success | - |
| dc2-leaf1a | System | VerifyFileSystemUtilization | Verifies that no partition is utilizing more than 75% of its disk space. | ✅&nbsp;Success | - |
| dc2-leaf1a | System | VerifyMaintenance | Verifies that the device is not currently under or entering maintenance. | ✅&nbsp;Success | - |
| dc2-leaf1a | System | VerifyMemoryUtilization | Verifies whether the memory utilization is below 75%. | ✅&nbsp;Success | - |
| dc2-leaf1a | System | VerifyNTP | Verifies if NTP is synchronised. | ✅&nbsp;Success | - |
| dc2-leaf1a | System | VerifyReloadCause | Verifies the last reload cause of the device. | ✅&nbsp;Success | - |
| dc2-leaf1b | Configuration | VerifyRunningConfigDiffs | Verifies there is no difference between the running-config and the startup-config. | ✅&nbsp;Success | - |
| dc2-leaf1b | Configuration | VerifyZeroTouch | Verifies ZeroTouch is disabled. | ✅&nbsp;Success | - |
| dc2-leaf1b | Interfaces | VerifyIllegalLACP | Verifies there are no illegal LACP packets in port channels. | ✅&nbsp;Success | - |
| dc2-leaf1b | Interfaces | VerifyInterfaceErrDisabled | Verifies there are no interfaces in the errdisabled state. | ✅&nbsp;Success | - |
| dc2-leaf1b | Interfaces | VerifyInterfaceErrors | Verifies that the interfaces error counters are equal to zero. | ✅&nbsp;Success | - |
| dc2-leaf1b | Interfaces | VerifyInterfaceUtilization | Verifies that the utilization of interfaces is below a certain threshold. | ✅&nbsp;Success | - |
| dc2-leaf1b | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | ✅&nbsp;Success | - |
| dc2-leaf1b | STP | VerifySTPCounters | Verifies there is no errors in STP BPDU packets. | ✅&nbsp;Success | - |
| dc2-leaf1b | System | VerifyAgentLogs | Verifies there are no agent crash reports. | ✅&nbsp;Success | - |
| dc2-leaf1b | System | VerifyCoredump | Verifies there are no core dump files. | ✅&nbsp;Success | - |
| dc2-leaf1b | System | VerifyFileSystemUtilization | Verifies that no partition is utilizing more than 75% of its disk space. | ✅&nbsp;Success | - |
| dc2-leaf1b | System | VerifyMaintenance | Verifies that the device is not currently under or entering maintenance. | ✅&nbsp;Success | - |
| dc2-leaf1b | System | VerifyMemoryUtilization | Verifies whether the memory utilization is below 75%. | ✅&nbsp;Success | - |
| dc2-leaf1b | System | VerifyNTP | Verifies if NTP is synchronised. | ✅&nbsp;Success | - |
| dc2-leaf1b | System | VerifyReloadCause | Verifies the last reload cause of the device. | ✅&nbsp;Success | - |
| dc2-leaf1c | Configuration | VerifyZeroTouch | Verifies ZeroTouch is disabled. | ✅&nbsp;Success | - |
| dc2-leaf1c | Interfaces | VerifyIllegalLACP | Verifies there are no illegal LACP packets in port channels. | ✅&nbsp;Success | - |
| dc2-leaf1c | Interfaces | VerifyInterfaceErrDisabled | Verifies there are no interfaces in the errdisabled state. | ✅&nbsp;Success | - |
| dc2-leaf1c | Interfaces | VerifyInterfaceErrors | Verifies that the interfaces error counters are equal to zero. | ✅&nbsp;Success | - |
| dc2-leaf1c | Interfaces | VerifyInterfaceUtilization | Verifies that the utilization of interfaces is below a certain threshold. | ✅&nbsp;Success | - |
| dc2-leaf1c | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | ✅&nbsp;Success | - |
| dc2-leaf1c | STP | VerifySTPCounters | Verifies there is no errors in STP BPDU packets. | ✅&nbsp;Success | - |
| dc2-leaf1c | System | VerifyAgentLogs | Verifies there are no agent crash reports. | ✅&nbsp;Success | - |
| dc2-leaf1c | System | VerifyCoredump | Verifies there are no core dump files. | ✅&nbsp;Success | - |
| dc2-leaf1c | System | VerifyFileSystemUtilization | Verifies that no partition is utilizing more than 75% of its disk space. | ✅&nbsp;Success | - |
| dc2-leaf1c | System | VerifyMaintenance | Verifies that the device is not currently under or entering maintenance. | ✅&nbsp;Success | - |
| dc2-leaf1c | System | VerifyMemoryUtilization | Verifies whether the memory utilization is below 75%. | ✅&nbsp;Success | - |
| dc2-leaf1c | System | VerifyNTP | Verifies if NTP is synchronised. | ✅&nbsp;Success | - |
| dc2-leaf1c | System | VerifyReloadCause | Verifies the last reload cause of the device. | ✅&nbsp;Success | - |
| dc2-leaf2a | Configuration | VerifyZeroTouch | Verifies ZeroTouch is disabled. | ✅&nbsp;Success | - |
| dc2-leaf2a | Interfaces | VerifyIllegalLACP | Verifies there are no illegal LACP packets in port channels. | ✅&nbsp;Success | - |
| dc2-leaf2a | Interfaces | VerifyInterfaceErrDisabled | Verifies there are no interfaces in the errdisabled state. | ✅&nbsp;Success | - |
| dc2-leaf2a | Interfaces | VerifyInterfaceErrors | Verifies that the interfaces error counters are equal to zero. | ✅&nbsp;Success | - |
| dc2-leaf2a | Interfaces | VerifyInterfaceUtilization | Verifies that the utilization of interfaces is below a certain threshold. | ✅&nbsp;Success | - |
| dc2-leaf2a | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | ✅&nbsp;Success | - |
| dc2-leaf2a | STP | VerifySTPCounters | Verifies there is no errors in STP BPDU packets. | ✅&nbsp;Success | - |
| dc2-leaf2a | System | VerifyAgentLogs | Verifies there are no agent crash reports. | ✅&nbsp;Success | - |
| dc2-leaf2a | System | VerifyCoredump | Verifies there are no core dump files. | ✅&nbsp;Success | - |
| dc2-leaf2a | System | VerifyFileSystemUtilization | Verifies that no partition is utilizing more than 75% of its disk space. | ✅&nbsp;Success | - |
| dc2-leaf2a | System | VerifyMaintenance | Verifies that the device is not currently under or entering maintenance. | ✅&nbsp;Success | - |
| dc2-leaf2a | System | VerifyMemoryUtilization | Verifies whether the memory utilization is below 75%. | ✅&nbsp;Success | - |
| dc2-leaf2a | System | VerifyNTP | Verifies if NTP is synchronised. | ✅&nbsp;Success | - |
| dc2-leaf2a | System | VerifyReloadCause | Verifies the last reload cause of the device. | ✅&nbsp;Success | - |
| dc2-leaf2b | Configuration | VerifyRunningConfigDiffs | Verifies there is no difference between the running-config and the startup-config. | ✅&nbsp;Success | - |
| dc2-leaf2b | Configuration | VerifyZeroTouch | Verifies ZeroTouch is disabled. | ✅&nbsp;Success | - |
| dc2-leaf2b | Interfaces | VerifyIllegalLACP | Verifies there are no illegal LACP packets in port channels. | ✅&nbsp;Success | - |
| dc2-leaf2b | Interfaces | VerifyInterfaceErrDisabled | Verifies there are no interfaces in the errdisabled state. | ✅&nbsp;Success | - |
| dc2-leaf2b | Interfaces | VerifyInterfaceErrors | Verifies that the interfaces error counters are equal to zero. | ✅&nbsp;Success | - |
| dc2-leaf2b | Interfaces | VerifyInterfaceUtilization | Verifies that the utilization of interfaces is below a certain threshold. | ✅&nbsp;Success | - |
| dc2-leaf2b | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | ✅&nbsp;Success | - |
| dc2-leaf2b | STP | VerifySTPCounters | Verifies there is no errors in STP BPDU packets. | ✅&nbsp;Success | - |
| dc2-leaf2b | System | VerifyAgentLogs | Verifies there are no agent crash reports. | ✅&nbsp;Success | - |
| dc2-leaf2b | System | VerifyCoredump | Verifies there are no core dump files. | ✅&nbsp;Success | - |
| dc2-leaf2b | System | VerifyFileSystemUtilization | Verifies that no partition is utilizing more than 75% of its disk space. | ✅&nbsp;Success | - |
| dc2-leaf2b | System | VerifyMaintenance | Verifies that the device is not currently under or entering maintenance. | ✅&nbsp;Success | - |
| dc2-leaf2b | System | VerifyMemoryUtilization | Verifies whether the memory utilization is below 75%. | ✅&nbsp;Success | - |
| dc2-leaf2b | System | VerifyNTP | Verifies if NTP is synchronised. | ✅&nbsp;Success | - |
| dc2-leaf2b | System | VerifyReloadCause | Verifies the last reload cause of the device. | ✅&nbsp;Success | - |
| dc2-leaf2c | Configuration | VerifyRunningConfigDiffs | Verifies there is no difference between the running-config and the startup-config. | ✅&nbsp;Success | - |
| dc2-leaf2c | Configuration | VerifyZeroTouch | Verifies ZeroTouch is disabled. | ✅&nbsp;Success | - |
| dc2-leaf2c | Interfaces | VerifyIllegalLACP | Verifies there are no illegal LACP packets in port channels. | ✅&nbsp;Success | - |
| dc2-leaf2c | Interfaces | VerifyInterfaceErrDisabled | Verifies there are no interfaces in the errdisabled state. | ✅&nbsp;Success | - |
| dc2-leaf2c | Interfaces | VerifyInterfaceErrors | Verifies that the interfaces error counters are equal to zero. | ✅&nbsp;Success | - |
| dc2-leaf2c | Interfaces | VerifyInterfaceUtilization | Verifies that the utilization of interfaces is below a certain threshold. | ✅&nbsp;Success | - |
| dc2-leaf2c | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | ✅&nbsp;Success | - |
| dc2-leaf2c | STP | VerifySTPCounters | Verifies there is no errors in STP BPDU packets. | ✅&nbsp;Success | - |
| dc2-leaf2c | System | VerifyAgentLogs | Verifies there are no agent crash reports. | ✅&nbsp;Success | - |
| dc2-leaf2c | System | VerifyCoredump | Verifies there are no core dump files. | ✅&nbsp;Success | - |
| dc2-leaf2c | System | VerifyFileSystemUtilization | Verifies that no partition is utilizing more than 75% of its disk space. | ✅&nbsp;Success | - |
| dc2-leaf2c | System | VerifyMaintenance | Verifies that the device is not currently under or entering maintenance. | ✅&nbsp;Success | - |
| dc2-leaf2c | System | VerifyMemoryUtilization | Verifies whether the memory utilization is below 75%. | ✅&nbsp;Success | - |
| dc2-leaf2c | System | VerifyNTP | Verifies if NTP is synchronised. | ✅&nbsp;Success | - |
| dc2-leaf2c | System | VerifyReloadCause | Verifies the last reload cause of the device. | ✅&nbsp;Success | - |
| dc2-spine1 | Configuration | VerifyZeroTouch | Verifies ZeroTouch is disabled. | ✅&nbsp;Success | - |
| dc2-spine1 | Interfaces | VerifyInterfaceErrDisabled | Verifies there are no interfaces in the errdisabled state. | ✅&nbsp;Success | - |
| dc2-spine1 | Interfaces | VerifyInterfaceErrors | Verifies that the interfaces error counters are equal to zero. | ✅&nbsp;Success | - |
| dc2-spine1 | Interfaces | VerifyInterfaceUtilization | Verifies that the utilization of interfaces is below a certain threshold. | ✅&nbsp;Success | - |
| dc2-spine1 | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | ✅&nbsp;Success | - |
| dc2-spine1 | STP | VerifySTPCounters | Verifies there is no errors in STP BPDU packets. | ✅&nbsp;Success | - |
| dc2-spine1 | System | VerifyAgentLogs | Verifies there are no agent crash reports. | ✅&nbsp;Success | - |
| dc2-spine1 | System | VerifyCoredump | Verifies there are no core dump files. | ✅&nbsp;Success | - |
| dc2-spine1 | System | VerifyFileSystemUtilization | Verifies that no partition is utilizing more than 75% of its disk space. | ✅&nbsp;Success | - |
| dc2-spine1 | System | VerifyMaintenance | Verifies that the device is not currently under or entering maintenance. | ✅&nbsp;Success | - |
| dc2-spine1 | System | VerifyMemoryUtilization | Verifies whether the memory utilization is below 75%. | ✅&nbsp;Success | - |
| dc2-spine1 | System | VerifyNTP | Verifies if NTP is synchronised. | ✅&nbsp;Success | - |
| dc2-spine1 | System | VerifyReloadCause | Verifies the last reload cause of the device. | ✅&nbsp;Success | - |
| dc2-spine2 | Configuration | VerifyRunningConfigDiffs | Verifies there is no difference between the running-config and the startup-config. | ✅&nbsp;Success | - |
| dc2-spine2 | Configuration | VerifyZeroTouch | Verifies ZeroTouch is disabled. | ✅&nbsp;Success | - |
| dc2-spine2 | Interfaces | VerifyInterfaceErrDisabled | Verifies there are no interfaces in the errdisabled state. | ✅&nbsp;Success | - |
| dc2-spine2 | Interfaces | VerifyInterfaceErrors | Verifies that the interfaces error counters are equal to zero. | ✅&nbsp;Success | - |
| dc2-spine2 | Interfaces | VerifyInterfaceUtilization | Verifies that the utilization of interfaces is below a certain threshold. | ✅&nbsp;Success | - |
| dc2-spine2 | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | ✅&nbsp;Success | - |
| dc2-spine2 | STP | VerifySTPCounters | Verifies there is no errors in STP BPDU packets. | ✅&nbsp;Success | - |
| dc2-spine2 | System | VerifyAgentLogs | Verifies there are no agent crash reports. | ✅&nbsp;Success | - |
| dc2-spine2 | System | VerifyCoredump | Verifies there are no core dump files. | ✅&nbsp;Success | - |
| dc2-spine2 | System | VerifyFileSystemUtilization | Verifies that no partition is utilizing more than 75% of its disk space. | ✅&nbsp;Success | - |
| dc2-spine2 | System | VerifyMaintenance | Verifies that the device is not currently under or entering maintenance. | ✅&nbsp;Success | - |
| dc2-spine2 | System | VerifyMemoryUtilization | Verifies whether the memory utilization is below 75%. | ✅&nbsp;Success | - |
| dc2-spine2 | System | VerifyNTP | Verifies if NTP is synchronised. | ✅&nbsp;Success | - |
| dc2-spine2 | System | VerifyReloadCause | Verifies the last reload cause of the device. | ✅&nbsp;Success | - |
| dc1-leaf1a | Interfaces | VerifyPortChannels | Verifies there are no inactive ports in port channels. | Unset | - |
| dc1-leaf1b | Interfaces | VerifyPortChannels | Verifies there are no inactive ports in port channels. | Unset | - |
| dc1-leaf1c | Interfaces | VerifyPortChannels | Verifies there are no inactive ports in port channels. | Unset | - |
| dc1-leaf2a | Interfaces | VerifyPortChannels | Verifies there are no inactive ports in port channels. | Unset | - |
| dc1-leaf2b | Interfaces | VerifyPortChannels | Verifies there are no inactive ports in port channels. | Unset | - |
| dc1-leaf2c | Interfaces | VerifyPortChannels | Verifies there are no inactive ports in port channels. | Unset | - |
| dc2-leaf1a | Interfaces | VerifyPortChannels | Verifies there are no inactive ports in port channels. | Unset | - |
| dc2-leaf1b | Interfaces | VerifyPortChannels | Verifies there are no inactive ports in port channels. | Unset | - |
| dc2-leaf1c | Interfaces | VerifyPortChannels | Verifies there are no inactive ports in port channels. | Unset | - |
| dc2-leaf2a | Interfaces | VerifyPortChannels | Verifies there are no inactive ports in port channels. | Unset | - |
| dc2-leaf2b | Interfaces | VerifyPortChannels | Verifies there are no inactive ports in port channels. | Unset | - |
| dc2-leaf2c | Interfaces | VerifyPortChannels | Verifies there are no inactive ports in port channels. | Unset | - |
