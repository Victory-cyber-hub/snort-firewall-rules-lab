# 08 — Troubleshooting

## Mininet Does Not Start

Verify that the CyberOps Workstation has sufficient resources. The supplied lab notes that a memory error may require increasing the VM memory.

## Snort Stops

The supplied lab instructs you to rerun:

```bash
./lab.support.files/scripts/start_snort.sh
```

if Snort stops and the shell prompt returns.

## No Alert Appears

Check:

```bash
tail -f /var/log/snort/alert
```

Confirm that the test traffic is being generated from H5 while Snort is running on R1.

## Firewall Rule Not Visible

Run:

```bash
iptables -L -v
```

and inspect the `FORWARD` chain.

## Mininet Cleanup

After exiting Mininet:

```bash
sudo mn -c
```

This clears processes created by Mininet.
