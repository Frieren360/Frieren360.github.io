+++
date = '2026-04-24T08:17:43+01:00'
title = 'UFW Cheat Sheet'
categories = ["Security", "Networking"]
tags = ["UFW", "Firewall", "Linux"]
+++
UFW (Uncomplicated Firewall) is a firewall utility for Linux to control iptables/nftables rules in a coherent way.

# Enable UFW
```sh
ufw enable
```

# Deny Incoming Traffic by Default

```sh
ufw default deny incoming
```

# Deny Outgoing Traffic by Default
```sh
ufw default deny outgoing
```

# Allow Incoming Traffic on Specific Port to All Interfaces from All Addresses
```sh
ufw allow in 25515
```

# Allow Incoming Traffic on Specific Port to All Interfaces from a Whole Network
```sh
ufw allow in from 192.168.1.0/24 to any port 25515
```

# Allow Incoming Traffic on Specific Port to All Interfaces from Specific IP Address
```sh
ufw allow in from 192.168.1.2 to any port 25515
```

# Allow Incoming Traffic on Specific Port to Specific interface from Specific IP Address
```sh
ip link
```

## Output
```text
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN mode DEFAULT group default qlen 1000
    [...]
2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP mode DEFAULT group default qlen 1000
    [...]
```
  
```sh
ufw allow in from 192.168.1.2 to eth0 port 25515
```

# Allow Outgoing Traffic to Specific Port on All Interfaces
```sh
ufw allow out 53
```

# Removing Firewall Rules
```sh
ufw status numbered
```

## Output

```text
Status: active

     To                         Action      From
     --                         ------      ----
[ 1] 25515                      ALLOW IN    Anywhere
```

```sh
ufw delete 1
```
