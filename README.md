# Tenacity – Unofficial APT Repository

Signed Debian package for **Tenacity**, automatically built from the [official source](https://codeberg.org/tenacityteam/tenacity) and updated daily.

> ⚠️ **Replaces Audacity.** Installing Tenacity will remove Audacity.

## Installation

```bash
curl -fsSL https://tiagocasalribeiro.github.io/tenacity-apt/KEY.gpg \
  | sudo tee /etc/apt/trusted.gpg.d/tenacity.asc

echo "deb [arch=amd64 signed-by=/etc/apt/trusted.gpg.d/tenacity.asc] \
  https://tiagocasalribeiro.github.io/tenacity-apt stable main" \
  | sudo tee /etc/apt/sources.list.d/tenacity.list

sudo apt update
sudo apt install tenacity
```

## Update

```bash
sudo apt update && sudo apt upgrade
```

## Uninstall

```bash
sudo apt remove tenacity
sudo rm /etc/apt/sources.list.d/tenacity.list \
        /etc/apt/trusted.gpg.d/tenacity.asc
sudo apt update
```

## Notes

- Requires **Debian trixie** (or compatible).
