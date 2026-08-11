# PNetLab v6 Installer

A shell script to install/upgrade **PNETLab v6** on **Ubuntu 20.04**. All PNETLab dependency packages are bundled and pulled from this repo instead of the original upstream host, so the whole install runs from one place.

## Requirements

- Fresh **Ubuntu 20.04** (Focal) server or VM
- Root access
- At least 100 GB free disk space recommended

## Quick Install (one line)

Run this as root on a clean Ubuntu 20.04 machine:

```bash
bash <(curl -fsSL https://raw.githubusercontent.com/DistriByteX/PNetLab/refs/heads/main/install_pnetlab_v6.sh)
```

If `curl` isn't available, use `wget` instead:

```bash
bash <(wget -qO- https://raw.githubusercontent.com/DistriByteX/PNetLab/refs/heads/main/install_pnetlab_v6.sh)
```

## Manual Install

If you'd rather download and inspect the script before running it:

```bash
wget https://raw.githubusercontent.com/DistriByteX/PNetLab/refs/heads/main/install_pnetlab_v6.sh
chmod +x install_pnetlab_v6.sh
sudo ./install_pnetlab_v6.sh
```

## Default credentials

```
Username: root
Password: pnet
```

**Reboot after the first install** to load the new kernel and finish setup.

## Install ishare2

[ishare2](https://github.com/ishare2-org/ishare2-cli) is a CLI tool you can install alongside PNETLab. Pick one:

Using `wget`:

```bash
wget -O /usr/sbin/ishare2 https://raw.githubusercontent.com/ishare2-org/ishare2-cli/main/ishare2 && chmod +x /usr/sbin/ishare2 && ishare2
```

Using `curl`:

```bash
curl -O /usr/sbin/ishare2 https://raw.githubusercontent.com/ishare2-org/ishare2-cli/main/ishare2 && chmod +x /usr/sbin/ishare2 && ishare2
```
