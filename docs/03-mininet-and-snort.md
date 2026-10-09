# 03 — Mininet and Snort

## Start Mininet

```bash
sudo ./lab.support.files/scripts/cyberops_extended_topo_no_fw.py
```

Wait for:

```text
mininet>
```

## Open R1

```text
xterm R1
```

## Start Snort

On R1:

```bash
./lab.support.files/scripts/start_snort.sh
```

Snort should initialize its plugins, preprocessors, and rules and remain running.

## Open H5 and H10

```text
xterm H5
xterm H10
```

## Start H10 Server

```bash
./lab.support.files/scripts/mal_server_start.sh
```

Verify:

```bash
netstat -tunpa
```

The supplied lab demonstrates nginx listening on TCP port `6666`.

## Monitor Alerts

Open another R1 terminal:

```bash
tail -f /var/log/snort/alert
```
