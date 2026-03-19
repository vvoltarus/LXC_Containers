# LXC Containers Lab

This project demonstrates the deployment and management of Linux containers using **LXC (Linux Containers)** on a Ubuntu host system.

The lab focuses on building lightweight virtualized environments, configuring networking, and managing container lifecycle.

---

## Overview

The objective of this lab is to understand how system-level virtualization works using LXC and how containers can be used to simulate isolated environments.

Key components:

* LXC container creation and management
* container networking configuration
* DHCP reservation for predictable IP addressing
* container auto-start configuration
* basic system administration inside containers

---

## Architecture

The lab consists of a host machine running LXC and one or more containers connected to the same network.

* Host: Ubuntu Server (LXC host)
* Containers: isolated Linux environments
* Network: bridged networking with assigned IP addresses

---

## Features

* lightweight container deployment
* isolated environments without full virtualization
* persistent container configuration
* predictable networking using DHCP reservation
* automated container startup

---

## Key Commands

Create container:

```bash id="c1x8p4"
lxc-create -n container1 -t download
```

Start container:

```bash id="d9f3m1"
lxc-start -n container1
```

Access container:

```bash id="z7k2q8"
lxc-attach -n container1
```

List containers:

```bash id="y3j8w2"
lxc-ls -f
```

---

## Verification

Check container status:

```bash id="p8q2r1"
lxc-info -n container1
```

Verify assigned IP:

```bash id="m4t9s7"
ip a
```

Ensure container autostart is configured correctly.

---

## Skills Demonstrated

* Linux system administration
* container-based virtualization
* network configuration
* service management
* infrastructure isolation concepts

---

## Project Status

✔ Completed
This lab demonstrates practical understanding of LXC containers and basic container networking.
