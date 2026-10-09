# Commands Reference

This file provides a categorized reference for the commands used in the lab.

## Network

```bash
ifconfig
ping www.cisco.com
```

## Mininet

```bash
sudo ./lab.support.files/scripts/cyberops_extended_topo_no_fw.py
```

```text
xterm R1
xterm H5
xterm H10
quit
```

## Snort

```bash
./lab.support.files/scripts/start_snort.sh
tail -f /var/log/snort/alert
```

## Server

```bash
./lab.support.files/scripts/mal_server_start.sh
netstat -tunpa
```

## Traffic

```bash
wget 209.165.202.133:6666/W32.Nimda.Amm.exe
```

## Packet Capture

```bash
tcpdump -i H5-eth0 -w nimda.download.pcap &
fg
```

## Firewall

```bash
iptables -L -v
```

```bash
iptables -I FORWARD -p tcp -d 209.165.202.133 --dport 6666 -j DROP
```

## Cleanup

```bash
sudo mn -c
```
