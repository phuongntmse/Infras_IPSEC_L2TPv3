#Build architecture + export to png
1. sudo bash build_architecture
2. python3 network_graph.py > graph.dot
3. dot -Tpng graph.dot -o graph.png
#LAN
1. sudo bash build_architecture
2. sudo bash config_VLAN
3. run DHCP server (support_cmd)
4. run P3, P4 as dhcpclient to get IP address (support_cmd)
#TUNNEL_IP_L2TPV3
1. sudo bash build_architecture
2. sudo bash config_L2TPv3_IP
3. run DHCP server (support_cmd)
4. run P1, P2, P3, P4 as dhcpclient to get IP address (support_cmd)
#TUNNEL_UDP_L2TPV3
1. sudo bash build_architecture
2. sudo bash config_L2TPv3_UDP
3. run DHCP server (support_cmd)
4. run P1, P2, P3, P4 as dhcpclient to get IP address (support_cmd)
#TUNNEL GRE
1. sudo bash build_architecture
2. sudo bash config_GRE
3. run DHCP server (support_cmd)
4. run P1, P2, P3, P4 as dhcpclient to get IP address (support_cmd)
#IPSec in L2TPV3 mode IP
1. sudo bash build_architecture
2. sudo bash config_L2TPv3_IP
3. sudo bass config_L2TPv3_IP_IPSec
4. run DHCP server (support_cmd)
5. run P1, P2, P3, P4 as dhcpclient to get IP address (support_cmd)
#ACCESS INTERNET
1. sudo bash build_architecture
2. sudo bash config_L2TPv3_IP
3. run DHCP server (support_cmd)
4. run P1, P2, P3, P4 as dhcpclient to get IP address (support_cmd)
5. sudo bash config_Internet_Access
#PROHIBIT TRAFFIC
1. sudo bash build_architecture
2. sudo bash config_L2TPv3_IP
	3.1 sudo bash config_iptables_prohibit_traffic
	3.2 sudo bash config_policy_routing_prohibit_traffic
4. run DHCP server (support_cmd)
5. run P1, P2, P3, P4 as dhcpclient to get IP address (support_cmd)
