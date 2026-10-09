# Snort and Firewall Rules Lab

## Cybersecurity Practical Lab Documentation

This repository documents the **Snort and Firewall Rules** practical lab performed in an authorized CyberOps/Mininet lab environment.

The lab demonstrates a defensive workflow involving:

- Virtual network preparation
- Mininet topology deployment
- Snort IDS monitoring
- Simulated suspicious HTTP traffic
- IDS alert analysis
- Packet capture with `tcpdump`
- Firewall rule inspection with `iptables`
- Blocking traffic based on an IDS finding
- Verification of the firewall response
- Mininet cleanup

> **Authorized lab use only:** Perform these activities only in a controlled environment that you own or are explicitly authorized to test.

---

## Lab Objectives

1. Prepare the virtual environment.
2. Configure and verify network connectivity.
3. Start the Mininet topology.
4. Start Snort in IDS mode.
5. Monitor the Snort alert log.
6. Generate test traffic from H5 toward the simulated server.
7. Observe the IDS alert.
8. Capture the network transaction with `tcpdump`.
9. Verify the PCAP was created.
10. Inspect the R1 firewall rules.
11. Add a `FORWARD` DROP rule.
12. Verify the malicious-server connection is blocked.
13. Terminate and clean up Mininet.

The supplied Cisco lab identifies the same three major sections: **Preparing the Virtual Environment**, **Firewall and IDS Logs**, and **Terminate and Clear Mininet Process**.

---

## Repository Structure

```text
snort-firewall-rules-lab/
│
├── README.md
├── LICENSE
├── .gitignore
│
├── COMMANDS.md
├── EVIDENCE-CHECKLIST.md
│
├── docs/
│   ├── 01-lab-overview.md
│   ├── 02-environment-setup.md
│   ├── 03-mininet-and-snort.md
│   ├── 04-traffic-and-ids-alert.md
│   ├── 05-packet-capture.md
│   ├── 06-firewall-rules.md
│   ├── 07-verification-and-cleanup.md
│   └── 08-troubleshooting.md
│
├── commands/
│   └── commands-reference.md
│
├── evidence/
│   ├── EVIDENCE-LOG.md
│   └── README.md
│
└── screenshots/
    ├── 01-environment/
    ├── 02-snort-ids/
    ├── 03-traffic-capture/
    ├── 04-firewall/
    └── 05-verification/
```

---

## Tools Used

| Tool | Purpose |
|---|---|
| CyberOps Workstation | Lab workstation |
| Mininet | Virtual network topology |
| Snort | Intrusion Detection System |
| iptables | Linux firewall |
| tcpdump | Packet capture |
| wget | Generate HTTP test traffic |
| netstat | Verify listening services |

---

## Lab Workflow

```text
Prepare Environment
        ↓
Start Mininet
        ↓
Start Snort
        ↓
Start Simulated Web Server
        ↓
Generate HTTP Traffic
        ↓
Snort Detects Traffic
        ↓
Record IDS Alert
        ↓
Capture Packets
        ↓
Inspect Firewall
        ↓
Add DROP Rule
        ↓
Repeat Connection Test
        ↓
Verify Traffic Is Blocked
        ↓
Clean Up Mininet
```

---

## Documentation

Detailed documentation is located in the [`docs/`](docs/) directory.

Start here:

- [Lab Overview](docs/01-lab-overview.md)
- [Environment Setup](docs/02-environment-setup.md)
- [Mininet and Snort](docs/03-mininet-and-snort.md)
- [Traffic and IDS Alert](docs/04-traffic-and-ids-alert.md)
- [Packet Capture](docs/05-packet-capture.md)
- [Firewall Rules](docs/06-firewall-rules.md)
- [Verification and Cleanup](docs/07-verification-and-cleanup.md)
- [Troubleshooting](docs/08-troubleshooting.md)

---

## Commands

All lab commands are collected in:

**[COMMANDS.md](COMMANDS.md)**

A more detailed command reference is available at:

**[commands/commands-reference.md](commands/commands-reference.md)**

---

## Evidence

Use:

**[EVIDENCE-CHECKLIST.md](EVIDENCE-CHECKLIST.md)**

to track every screenshot and verification item.

Then record the actual evidence in:

**[evidence/EVIDENCE-LOG.md](evidence/EVIDENCE-LOG.md)**

Screenshots should be stored under:

```text
screenshots/
```

---

## Portfolio Evidence

Recommended screenshots include:

- Network configuration
- Successful Mininet startup
- Snort initialization
- H10 listening on TCP 6666
- Snort alert monitoring
- Successful initial HTTP download
- Snort alert
- tcpdump capture
- PCAP verification
- iptables before the rule
- DROP rule added
- iptables after the rule
- Blocked/timed-out connection
- Mininet cleanup

Use meaningful filenames such as:

```text
02-01-start-snort.png
02-06-snort-alert.png
04-01-iptables-before.png
04-03-iptables-after.png
05-01-blocked-download.png
```

---

## Security Note

The original exercise uses a simulated malicious-server scenario. Do not publish credentials, private keys, unnecessary malware binaries, or sensitive personal information.

The repository `.gitignore` excludes executable files and PCAP files by default.

---

## Questions and Answers

Document your responses to the lab questions in your GitHub repository as part of your portfolio evidence.

Focus on:

- What the Snort alert means
- Source and destination information
- TCP ports
- Why the `FORWARD` chain is used
- How the PCAP can support investigation
- Why the firewall rule blocks the subsequent connection

---

## Final Portfolio Checklist

- [ ] Lab completed
- [ ] Commands documented
- [ ] Documentation completed
- [ ] Evidence checklist completed
- [ ] Screenshots added
- [ ] Evidence log completed
- [ ] Sensitive information removed
- [ ] `.gitignore` verified
- [ ] README reviewed
- [ ] LICENSE included
- [ ] Repository pushed to GitHub
