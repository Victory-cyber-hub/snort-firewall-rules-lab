# EVIDENCE CHECKLIST

Use this checklist while performing the lab. Every checked item should have supporting evidence where practical.

## Environment

- [ ] CyberOps Workstation started
- [ ] Network configured
- [ ] IP address verified
- [ ] Connectivity tested
- [ ] Screenshot saved

## Mininet

- [ ] Mininet topology started
- [ ] `mininet>` prompt visible
- [ ] R1 terminal opened
- [ ] H5 terminal opened
- [ ] H10 terminal opened
- [ ] Screenshot saved

## Snort IDS

- [ ] Snort started successfully
- [ ] Snort configuration loaded
- [ ] Snort alert log monitored
- [ ] Screenshot of Snort startup saved
- [ ] Screenshot of alert monitoring saved

## Simulated Server

- [ ] H10 server started
- [ ] `netstat -tunpa` executed
- [ ] TCP 6666 listening state verified
- [ ] Screenshot saved

## Initial Traffic

- [ ] H5 generated HTTP request
- [ ] Download response documented
- [ ] File transfer result documented
- [ ] Screenshot saved

## IDS Alert

- [ ] Snort alert generated
- [ ] Timestamp recorded
- [ ] Source IP recorded
- [ ] Source port recorded
- [ ] Destination IP recorded
- [ ] Destination port recorded
- [ ] Alert message recorded
- [ ] Screenshot saved

## Packet Capture

- [ ] tcpdump started
- [ ] Download repeated while capture was active
- [ ] tcpdump stopped
- [ ] PCAP verified with `ls -l`
- [ ] Screenshot saved

## Firewall

- [ ] `iptables -L -v` captured before modification
- [ ] Existing chains documented
- [ ] FORWARD chain identified
- [ ] DROP rule added
- [ ] `iptables -L -v` captured after modification
- [ ] Screenshot saved

## Verification

- [ ] Download attempted after firewall rule
- [ ] Connection failed/timed out
- [ ] Result documented
- [ ] Screenshot saved

## Cleanup

- [ ] Mininet exited
- [ ] `sudo mn -c` executed
- [ ] Cleanup evidence captured

## GitHub Quality

- [ ] README completed
- [ ] COMMANDS completed
- [ ] Documentation completed
- [ ] Evidence log completed
- [ ] Screenshots organized
- [ ] Sensitive information removed
- [ ] `.gitignore` checked
- [ ] LICENSE present
- [ ] Git status reviewed
