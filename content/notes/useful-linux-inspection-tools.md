---
title: "Useful Linux System Inspection Commands"
date: 2026-11-18
tags: ["Linux", "CLI", "Fedora", "Commands"]
summary: "Quick reference for handy terminal commands to inspect system state, sockets, and hardware."
---

A quick reference for commands I frequently use to inspect hardware and Linux system state:

### Sockets & Network Connections

```bash
# List all listening TCP/UDP sockets with process names
ss -tulpn

# Monitor network interfaces in real time
ip -s link
```

### Memory & Hardware

```bash
# Memory usage in human-readable megabytes/gigabytes
free -h

# Hardware CPU topology and cache sizes
lscpu | grep -E "(Model name|CPU\(s\)|Thread|L1|L2|L3)"

# Inspect block devices and mount points
lsblk -f
```

### Process Resource Usage

```bash
# Top memory consuming processes
ps aux --sort=-%mem | head -n 10

# System calls of a running command
strace -c <command>
```
