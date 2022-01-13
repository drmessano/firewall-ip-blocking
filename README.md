# firewall-ip-blocking

Implementation:

IPTables, paste into terminal

IPSet, paste into terminal and add rules to IPTables, such as:

iptables -A INPUT -m set --set non-arin -j DROP -m comment --comment "Non-ARIN IPs"
ip6tables -A INPUT -m set --set non-arin6 -j DROP -m comment --comment "Non-ARIN IPs"

Mikrotik, paste address list into terminal and add the following firewall rules:

/ip firewall raw
add action=drop chain=prerouting comment=non-arin in-interface=ether1 src-address-list=non-arin

/ipv6 firewall raw
add action=drop chain=prerouting comment=non-arin in-interface=ether1 src-address-list=non-arin
