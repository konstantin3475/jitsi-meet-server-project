# Operations Guide

## Restart Services

```bash
sudo systemctl restart nginx
sudo systemctl restart prosody
sudo systemctl restart jitsi-videobridge2
```

## Views Logs

```bash
journalctl -u nginx
journalctl -u prosody
journalctl -u jitsi-videobridge2
```

## Update Jitsi Meet

```bash
sudo apt update
sudo apt upgrade
```

## Renew Certificates

```bash
sudo /usr/share/jitsi-meet/scripts/install-letsencrypt-cert.sh
```
