# Ubuntu Server — Bootstrap

**Version : Ubuntu 26.04.1 LTS**

## Étape 1 : Configuration clavier

```bash
sudo dpkg-reconfigure keyboard-configuration
sudo systemctl restart keyboard-setup
sudo apt update && sudo apt install -y openssh-server
```

## Étape 2 : Configuration CC

```bash
sudo timedatectl set-timezone Europe/Paris
sudo timedatectl set-ntp true
sudo apt install -y curl wget vim nano  net-tools dnsutils
```

## Étape 3 : Check

```bash
BLUE='\033[1;34m'; RESET='\033[0m';
printf "\n${BLUE}===== HEURE =====${RESET}\n"; date '+%Y-%m-%d %H:%M:%S %Z'
printf "\n${BLUE}===== DISQUE =====${RESET}\n"; df -h / | tail -1
printf "\n${BLUE}===== RESEAU =====${RESET}\n"; ip a | grep 'inet '
printf "\n${BLUE}===== INTERNET =====${RESET}\n"; ping -c 1 8.8.8.8 | tail -2 | head -1
printf "\n${BLUE}===== DNS =====${RESET}\n"; ping -c 1 google.com | tail -2 | head -1
```
