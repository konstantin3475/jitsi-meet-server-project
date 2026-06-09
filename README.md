# jitsi-meet-server-project
Documentation of a self-hosted Jitsi Meet server deployment on Linux.

## Overview

This repository documents my experience deploying and maintaining a self-hosted Jitsi Meet environment.

## Project Goals

- Deploy a secure video conferencing platform
- Configure SSL certificates
- Manage DNS and domain settings
- Troubleshoot connectivity issues
- Evaluate recording and streaming options

## Technologies

- Linux
- Jitsi Meet
- Nginx
- Prosody
- Coturn
- Let's Encrypt

## Skills Demonstrated

- Linux System Administration
- Server Deployment
- DNS Management
- SSL Configuration
- Troubleshooting
- Technical Documentation

## Lessons Learned

This project improved my understanding of Linux server administration, real-time communication platforms, SSL management and system troubleshooting.

## Architecture

Internet
    |
    v
DNS
    |
    v
Nginx
    |
    v
Jitsi Meet
    |
    +-- Prosody
    |
    +-- JVB
    |
    +-- Coturn
D --> E
D --> F

E --> G
F --> G
