<p align="center">
  <img width="3252" height="1016" alt="image" src="https://github.com/user-attachments/assets/abc4655d-f2bc-43c2-ac1d-9e0a179b4552" />

</p>

# VLAN Segmented Network Design and Setup

## Project Overview

This project shows the setup of a VLAN-segmented network in a live church production environment. I set this up to increase performance and reliability during services and everyday use.

I used a UDM Pro and USW Pro Switches, configured VLANs and DHCP Scopes within those VLANs, and optimized port settings.

---

## Environments Used

- UniFi Dream Machine Pro (UDM Pro)
- UniFi Managed Pro Switches (USW)
- VLAN-Segmented Network
- DHCP, Multicast Support for Audio Systems

---

## Step 1: Planning the Network

Before I installed the system, I designed the network to separate different types of traffic to improve performance and reliability.

### VLAN Plan:
- Default	-	192.168.0.1/22 - VLAN 1
- sACN	-	10.0.0.1/8 - VLAN 10
- Control	-	192.168.20.1/24 - VLAN 20
- KVMs	-	192.168.30.1/24 - VLAN 30
- Dante	-	192.168.40.1/24 - VLAN 40
- NDI	-	192.168.60.1/24 - VLAN 60
- WiFi	-	192.168.100.1/22 - VLAN 100

This makes sure that high-bandwidth and latency-sensitive systems do not interfere with each other.

We werent ablke ti 

---

## Step 2: Creating VLAN Networks in UniFi

VLANs were created in the UniFi controller, each with its own subnet and DHCP scope.

[VLAN Configuration]<img width="1337" height="583" alt="Screenshot 2026-03-20 at 10 26 28 AM" src="https://github.com/user-attachments/assets/394aaf7d-09a4-4a93-a534-a807ee97534f" />


Each VLAN was assigned:
- A unique VLAN ID
- A subnet
- DHCP configuration

---

## Step 3: Configuring Network Segmentation

Each VLAN was configured to isolate traffic where necessary, preventing unnecessary communication between systems.

For example:
- Dante Audio VLAN was isolated to prevent interference
- Control systems were separated from general network traffic

<img width="384" height="922" alt="Screenshot 2026-03-20 at 10 28 33 AM" src="https://github.com/user-attachments/assets/829dcc5f-c051-44b3-9f81-6be9c70797ca" />
<img width="384" height="922" alt="Screenshot 2026-03-20 at 10 28 46 AM" src="https://github.com/user-attachments/assets/328d79a8-a87e-4123-b230-2d46dab4ba2c" />


---

## Step 4: Configuring Switch Ports

Switch ports were configured based on the type of device connected.

For Dante-enabled devices:
- Ports were assigned to VLAN 40
- Pro AV profile was used to prioritize traffic
- Multicast settings were enabled

<img width="384" height="922" alt="Screenshot 2026-03-20 at 10 29 22 AM" src="https://github.com/user-attachments/assets/7b8a8f06-ec87-4efa-9fde-a82aff52e6a9" />


---

## Step 5: Optimizing for Audio (Dante Network)

A dedicated VLAN was used for Dante audio to improve latency and stability.

- IGMP Snooping enabled for multicast optimization
- DHCP configured for consistent IP management
- Network isolation applied

---

## Step 6: Network Topology Overview

The diagram below shows how the network infrastructure is organized across the production environment. A Ubiquiti Dream Machine Pro (UDM Pro) connects to multiple switches, providing network access to areas such as the production booth, stage, and office systems.

VLANs are used to separate traffic between systems, such as audio (Dante), control devices, video/streaming, and general network use. This helps keep the network stable and prevents one system from affecting another.

[Network Topology]<img width="3308" height="1566" alt="image" src="https://github.com/user-attachments/assets/9395fd58-e675-44b9-860a-5fbce1620c99" />


### Operational Notes

One production-stage switch may appear offline in the topology. This switch is powered by a stage rack that is only turned on during live services or production use. When the rack is powered off, the switch is also powered off, as expected in this environment.

Spanning Tree Protocol (STP) is used across the network to maintain stability and prevent switching loops.

---

## Results

- Improved network stability
- Reduced interference between systems
- Reliable performance during live services

---

## What I Learned

- How to design and set up VLAN segmentation
- Importance of multicast handling (IGMP Snooping)
- Configuring switch ports based on device requirements
- Troubleshooting real-world network issues
