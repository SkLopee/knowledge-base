## Étape 1 : A la mano

sudo dpkg-reconfigure keyboard-configuration

sudo systemctl restart keyboard-setup

sudo apt update && sudo apt install -y openssh-server

ip a

## Étape 2 : CC

sudo timedatectl set-timezone Europe/Paris

sudo timedatectl set-ntp true

sudo apt install -y curl wget vim nano  net-tools dnsutils

## Étape 3 : Check

timedatectl
