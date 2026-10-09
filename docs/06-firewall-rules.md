# 06 — Firewall Rules

## Inspect Existing Rules

On R1:

```bash
iptables -L -v
```

Document the active chains.

The supplied lab identifies:

```text
INPUT
FORWARD
OUTPUT
```

## Why FORWARD?

The lab explains that traffic originating elsewhere and passing through the firewall is handled by the `FORWARD` chain.

## Add the DROP Rule

```bash
iptables -I FORWARD -p tcp -d 209.165.202.133 --dport 6666 -j DROP
```

## Verify

```bash
iptables -L -v
```

Look for the new DROP rule in the `FORWARD` chain.

## Evidence

Save before/after firewall screenshots under:

```text
screenshots/04-firewall/
```
