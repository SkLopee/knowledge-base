# Ubuntu Server — Bootstrap

**Version : Ubuntu 26.04.1 LTS**

## Étape 1 : Configuration clavier

```bash
sudo dpkg-reconfigure keyboard-configuration
sudo systemctl restart keyboard-setup
sudo apt update && sudo apt install -y openssh-server
```

ip a

## Étape 2 : Configuration CC

```bash
sudo timedatectl set-timezone Europe/Paris
sudo timedatectl set-ntp true
sudo apt install -y curl wget vim nano  net-tools dnsutils
```

## Étape 3 : Check

timedatectl

```bash
df
ip a
ping -c 1 8.8.8.8
ping -c 1 google.com
```
