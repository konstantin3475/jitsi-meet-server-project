# Jitsi Meet Installation Guide

This document describes the basic installation process for a self-hosted Jitsi Meet server on Linux.

## 1. Server Requirements

- Linux server
- Public IPv4 address
- Domain or subdomain
- Root or sudo access
- Open firewall ports

## 2. DNS Setup

Create an A record pointing your domain or subdomain to the server IP address.

Example:

meet.example.com -> SERVER_IP_ADDRESS

## 3. Update the Server

```bash
sudo apt update
sudo apt upgrade -y
```

## 4. Install Required Packages

```bash
sudo apt install curl gnupg2 apt-transport-https -y
```

## 5. Install Jitsi Meet

Installation steps depend on the Linux distribution and package source used.

During installation, enter the fully qualified domain name of the server.

Example:

```text
meet.example.com
```
Add the Jitsi package repository and install Jitsi Meet.

```bash
sudo apt install jitsi-meet -y
```

During installation, enter the fully qualified domain name of the server.

Example:

```text
meet.example.com
```


## 6. SSL Certificate

Use Let's Encrypt to secure the installation with HTTPS.
Jitsi Meet can request a Let's Encrypt certificate automatically.

```bash
sudo /usr/share/jitsi-meet/scripts/install-letsencrypt-cert.sh
```

## 7. Firewall Ports

Typical ports:

```text
80 TCP
443 TCP
10000 UDP
3478 UDP
5349 TCP
```

## 8. Check Services

After installation, check that the main services are running.

```bash
systemctl status nginx
systemctl status prosody
systemctl status jitsi-videobridge2
```
Add Jitsi installation and service checks
