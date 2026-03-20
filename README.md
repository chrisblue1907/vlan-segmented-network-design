# VLAN Segmented Network Design (Church Environment)

## Project Summary
This project outlines the design and implementation of a VLAN-segmented network in a live church production environment. The goal was to separate network traffic for different systems such as audio (Dante), control, general internet access, and production equipment to improve performance and reliability.

## Technologies Used
- Ubiquiti Dream Machine Pro (UDM Pro)
- Managed Switches
- VLAN Configuration
- Network Segmentation

## Environment
- Church production environment
- Multiple switches across stage and control areas
- Devices including computers, audio systems, and streaming equipment

## Network Design Overview
The network was segmented using VLANs to separate traffic types:

- VLAN 10 – General Network
- VLAN 20 – Production / Streaming
- VLAN 30 – Audio (Dante)
- VLAN 40 – Control Systems

This separation helped prevent congestion and ensured critical systems remained stable.

## Implementation Steps
1. Configured VLANs in the UDM Pro
2. Assigned VLANs to switch ports
3. Connected devices based on function
4. Tested connectivity and isolation between networks
5. Troubleshot routing and communication issues

## Challenges & Troubleshooting
- Ensuring proper VLAN tagging across switches
- Resolving communication issues between devices on different VLANs
- Troubleshooting network drops and misconfigured ports

## Results
- Improved network stability
- Reduced interference between systems
- More organized and scalable network structure

## Future Improvements
- Implement better monitoring tools
- Document network topology visually
- Improve redundancy

## Screenshots / Media
(Add screenshots here)
