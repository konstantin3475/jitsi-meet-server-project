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

sudo apt update
sudo apt upgrade -y

## 4. Install Required Packages

sudo apt install curl gnupg2 apt-transport-https -y

## 5. Install Jitsi Meet

Installation steps depend on the Linux distribution and package source used.

## 6. SSL Certificate

Use Let's Encrypt to secure the installation with HTTPS.

## 7. Firewall Ports

Typical ports:

80 TCP
443 TCP
10000 UDP
3478 UDP
5349 TCP
