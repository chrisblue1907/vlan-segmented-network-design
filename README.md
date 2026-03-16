<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="VLAN Network Banner" width="80%"/>
</p>

<h1>Designing and Implementing a VLAN-Segmented Network for a Live Production Environment</h1>

This project documents the design and implementation of a VLAN-segmented network in a live production environment. The goal of this project was to improve organization, traffic separation, and manageability by segmenting devices into logical groups based on their role in the production network.

The network was built using a Ubiquiti Dream Machine Pro and multiple managed switches, with VLANs used to separate systems such as production, control, audio, and other network-connected devices.

---

## Environments and Technologies Used

- Ubiquiti Dream Machine Pro (UDM Pro)
- Managed Network Switches
- UniFi Network Controller
- VLAN Segmentation
- Ethernet Infrastructure
- macOS
- Windows

---

## Operating Systems Used

- macOS
- Windows 10 / Windows 11

---

## Project Walkthrough

As the production environment expanded, it became important to better organize devices on the network. VLAN segmentation was implemented to separate systems by function and improve clarity, management, and troubleshooting.

This project focused on planning VLANs, assigning devices to the correct segments, and validating that the network behaved as intended after implementation.

---

## Step 1: Identify Device Groups and Network Requirements

The first step was determining which devices should be grouped together based on their role in the environment. Devices were reviewed and organized into logical categories to support more structured network management.

<p>
<img src="images/step1-device-groups.png" alt="Device Groups and Requirements" width="80%"/>
</p>

---

## Step 2: Plan the VLAN Structure

After identifying the device groups, VLANs were planned to separate different categories of traffic and devices across the network.

Examples of segmented device groups included production systems, control devices, and other network-connected endpoints.

<p>
<img src="images/step2-vlan-planning.png" alt="VLAN Planning" width="80%"/>
</p>

---

## Step 3: Configure VLANs Across the Network Infrastructure

The VLAN design was implemented using the UDM Pro and managed switches. Switch ports and connected devices were assigned based on the intended network segmentation.

<p>
<img src="images/step3-vlan-configuration.png" alt="VLAN Configuration" width="80%"/>
</p>

---

## Step 4: Validate Segmentation and Connectivity

After implementation, the network was tested to confirm that devices were assigned correctly, that expected communication was working, and that the segmented design improved organization and troubleshooting.

<p>
<img src="images/step4-vlan-validation.png" alt="VLAN Validation" width="80%"/>
</p>

---

## Outcome

This project demonstrates practical experience with network segmentation in a real-world environment. It highlights the value of organizing devices by function, improving manageability, and using structured network design to support reliability in production systems.

---

## Skills Demonstrated

- VLAN design and implementation
- Network segmentation
- Switch and router configuration awareness
- Infrastructure planning
- Connectivity validation
- Troubleshooting segmented networks
