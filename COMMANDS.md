# COMMANDS

## Snort and Firewall Rules Lab Command Sheet

> Run these commands only inside the authorized CyberOps/Mininet lab environment.

---

## 1. Configure DHCP

```bash
sudo ./lab.support.files/scripts/configure_as_dhcp.sh
```

---

## 2. Verify Network

```bash
ifconfig
```

Optional connectivity test from the supplied lab:

```bash
ping www.cisco.com
```

Stop with:

```text
Ctrl+C
```

---

## 3. Start Mininet

```bash
sudo ./lab.support.files/scripts/cyberops_extended_topo_no_fw.py
```

Expected prompt:

```text
mininet>
```

---

## 4. Open R1

From the Mininet prompt:

```text
xterm R1
```

---

## 5. Start Snort

On R1:

```bash
./lab.support.files/scripts/start_snort.sh
```

---

## 6. Open H5 and H10

From the Mininet prompt:

```text
xterm H5
xterm H10
```

---

## 7. Start the Simulated Web Server

On H10:

```bash
./lab.support.files/scripts/mal_server_start.sh
```

Verify:

```bash
netstat -tunpa
```

The supplied lab shows the server listening on TCP port `6666`.

---

## 8. Monitor Snort Alerts

On another R1 terminal:

```bash
tail -f /var/log/snort/alert
```

---

## 9. Generate Test Traffic

On H5:

```bash
wget 209.165.202.133:6666/W32.Nimda.Amm.exe
```

---

## 10. Start Packet Capture

On H5:

```bash
tcpdump -i H5-eth0 -w nimda.download.pcap &
```

Press ENTER to regain the shell.

---

## 11. Repeat the Test Download

```bash
wget 209.165.202.133:6666/W32.Nimda.Amm.exe
```

---

## 12. Stop tcpdump

```bash
fg
```

Then:

```text
Ctrl+C
```

---

## 13. Verify PCAP

```bash
ls -l
```

Look for:

```text
nimda.download.pcap
```

---

## 14. Inspect iptables

On R1:

```bash
iptables -L -v
```

---

## 15. Add the Firewall DROP Rule

```bash
iptables -I FORWARD -p tcp -d 209.165.202.133 --dport 6666 -j DROP
```

---

## 16. Verify the Rule

```bash
iptables -L -v
```

Look under:

```text
Chain FORWARD
```

for the DROP rule targeting the destination and TCP port.

---

## 17. Test the Firewall

On H5:

```bash
wget 209.165.202.133:6666/W32.Nimda.Amm.exe
```

The supplied lab demonstrates a connection timeout after the rule is applied.

Cancel repeated retries if necessary:

```text
Ctrl+C
```

---

## 18. Exit Mininet

From the main Mininet terminal:

```text
quit
```

---

## 19. Clean Up Mininet

```bash
sudo mn -c
```
