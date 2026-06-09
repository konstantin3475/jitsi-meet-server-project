# Troubleshooting Guide

This document describes common problems that may occur during the installation and operation of a self-hosted Jitsi Meet server and provides possible solutions.

## Problem: HTTPS Certificate Not Working

### Symptoms

* Browser shows a security warning
* HTTPS connection fails
* Invalid certificate message

### Possible Causes

* DNS record not configured correctly
* Domain not pointing to the correct server
* Let's Encrypt validation failed

### Solution

Verify DNS settings and rerun the certificate installation script.

```bash
sudo /usr/share/jitsi-meet/scripts/install-letsencrypt-cert.sh
```

## Problem: Users Cannot Join Meetings

### Symptoms

* Participants cannot connect
* Audio or video unavailable
* Connection timeout

### Possible Causes

* Firewall ports blocked
* Incorrect NAT configuration
* Coturn not running

### Solution

Verify that the required ports are open:

```text
80 TCP
443 TCP
10000 UDP
3478 UDP
5349 TCP
```

Check Coturn service status:

```bash
systemctl status coturn
```

## Problem: Jitsi Web Interface Not Available

### Symptoms

* Website cannot be reached
* HTTP 502 or 503 errors

### Possible Causes

* Nginx service stopped
* Configuration error
* DNS issue

### Solution

Check Nginx status:

```bash
systemctl status nginx
```

Restart service if required:

```bash
sudo systemctl restart nginx
```

## Problem: Video Bridge Not Working

### Symptoms

* Users join but audio/video fails
* Participants disconnect frequently

### Solution

Check Jitsi Video Bridge:

```bash
systemctl status jitsi-videobridge2
```

Review system logs:

```bash
journalctl -u jitsi-videobridge2
```

## Useful Diagnostic Commands

```bash
systemctl status nginx
systemctl status prosody
systemctl status jitsi-videobridge2
systemctl status coturn
```
