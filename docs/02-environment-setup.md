# 02 — Environment Setup

## Configure DHCP

Run:

```bash
sudo ./lab.support.files/scripts/configure_as_dhcp.sh
```

The supplied lab instructs the student to provide the `analyst` password when requested.

## Verify Network

```bash
ifconfig
```

The lab also provides a connectivity test:

```bash
ping www.cisco.com
```

Stop with `Ctrl+C`.

## Screenshot

Save the relevant evidence in:

```text
screenshots/01-environment/
```
