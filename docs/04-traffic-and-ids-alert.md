# 04 — Traffic and IDS Alert

## Generate Test Traffic

On H5:

```bash
wget 209.165.202.133:6666/W32.Nimda.Amm.exe
```

Record the result from your own run.

## Analyze the Alert

The Snort alert should provide useful indicators such as:

- Timestamp
- Source IPv4 address
- Source port
- Destination IPv4 address
- Destination port
- Alert message
- Priority

## Evidence

Save the screenshot of the Snort alert under:

```text
screenshots/02-snort-ids/
```

Use the actual values from your lab rather than copying example timestamps.
