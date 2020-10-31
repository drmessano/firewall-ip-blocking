# firewall-ip-blocking

To-Do: Aktualy write this section properly

Implemnentation:

IPTables / Mikrotik, paste into terminal

IPSet, paste into terminal and add rules to IPTables, such as:

```
iptables -A INPUT -m set --set non-arin -j DROP -m comment --comment "Non-ARIN IPs"
ip6tables -A INPUT -m set --set non-arin6 -j DROP -m comment --comment "Non-ARIN IPs"
```
