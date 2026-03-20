# VLAN Segmented Network Design (Church Environment)

## Project Overview
(you already have this)

---

## Step 1: Planning the Network

Before implementation, the network was designed to separate different types of traffic to improve performance and reliability.

### VLAN Plan:
- VLAN 1 – Default
- VLAN 20 – Control
- VLAN 40 – Dante Audio
- VLAN 60 – NDI
- VLAN 100 – WiFi

This segmentation ensures that high-bandwidth and latency-sensitive systems do not interfere with each other.

---

## Step 2: Creating VLAN Networks in UniFi

VLANs were created in the UniFi controller with their own subnets and DHCP scopes.

![VLAN Configuration](your-image-link)

Each VLAN was assigned:
- A unique VLAN ID
- A subnet
- DHCP configuration

---

## Step 3: Configuring Network Segmentation

Each VLAN was configured to isolate traffic where necessary to prevent unnecessary communication between systems.

For example:
- Dante Audio VLAN was isolated to prevent interference
- Control systems were separated from general network traffic

![VLAN Settings](your-image-link)

---

## Step 4: Configuring Switch Ports

Switch ports were configured based on the type of device connected.

For Dante-enabled devices:
- Ports were assigned to VLAN 40
- Pro AV profile was used to prioritize traffic
- Multicast settings were enabled

![Switch Port Configuration](your-image-link)

---

## Step 5: Optimizing for Audio (Dante Network)

A dedicated VLAN was used for Dante audio to ensure low latency and stability.

- IGMP Snooping enabled for multicast optimization
- DHCP configured for consistent IP management
- Network isolation applied

![Dante Network Settings](your-image-link)

---

## Step 6: Network Topology Overview

The full network includes a UDM Pro connected to multiple switches distributing traffic across production, office, and stage environments.

![Network Topology](your-image-link)

---

## Results

- Improved network stability
- Reduced interference between systems
- Reliable performance during live services

---

## What I Learned

- How to design and implement VLAN segmentation
- Importance of multicast handling (IGMP Snooping)
- Configuring switch ports based on device requirements
- Troubleshooting real-world network issues
