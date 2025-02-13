# Projects
# Network Security Homelab using VirtualBox, Wireshark, OPNSense, and Ubuntu

## Overview
This project aims to create a **Network Security Homelab** for learning and testing network security concepts using **VirtualBox**, **OPNSense**, **Wireshark**, and **Ubuntu**. The objective was to simulate network environments, capture network traffic, and analyze it for potential security vulnerabilities. Along the way, I encountered several challenges that allowed me to gain hands-on experience with network troubleshooting, firewall configurations, and network analysis.

## Technologies Used
- **VirtualBox**: Virtualization software used to create and manage the virtual machines (VMs).
- **OPNSense**: Open-source firewall/router software used to simulate network security features.
- **Wireshark**: Network protocol analyzer for capturing and analyzing network traffic.
- **Ubuntu**: Linux-based operating system used as a client to interact with the network.

## Objective
- **Build a functional homelab for network security**: Set up a simulated network environment using VirtualBox, OPNSense, Ubuntu, and Wireshark.
- **Capture and analyze network traffic**: Use Wireshark to capture packets and analyze network behavior.
- **Troubleshoot installation and configuration issues**: Resolve installation and configuration challenges with VirtualBox, OPNSense, and Ubuntu networking.

## Setup Guide

### 1. Install VirtualBox
   - Download and install VirtualBox from [VirtualBox Download](https://www.virtualbox.org/).
   - Choose the version appropriate for your operating system (Windows, macOS, or Linux).

### 2. Create Virtual Machines
   - **Ubuntu**: Create a new VM in VirtualBox with Ubuntu as the operating system. Allocate sufficient resources (e.g., 2GB RAM, 20GB storage).
   - **OPNSense**: Create a VM for OPNSense using the downloaded pfSense ISO. Allocate at least 1GB of RAM and configure network adapters as required.

### 3. Configure Networking in VirtualBox
   - Set the **Ubuntu VM** to use a **InternalNetwork*** for communication with pfSense.
   - Set the **OPNSense VM** to use **InternalNetwork** to allow it to act as the gateway for the network.

### 4. Install OPNSense on VirtualBox
   - Boot the OPNSense VM with the OPNSense ISO image.
   - Follow the installation prompts to complete the OPNSense setup. (In case OPNSense fails to reboot, refer to troubleshooting steps below.)
   - Using command to decompress the .bz2 file (on MAC) using the teminal:
     <img width="300" alt="Terminal" src="https://github.com/user-attachments/assets/821bdd04-75df-4b61-9df7-3c3bfd50400e" />
     

### 5. Install Wireshark on Ubuntu
   - Install Wireshark in Ubuntu by running:
     sudo apt update (to update the software)
     sudo apt install wireshark (to install the software)
     
     <img width="450" alt="Installation of Wireshark within Ubuntu" src="https://github.com/user-attachments/assets/124a67b7-34ec-498e-aa12-46d0dd4c63ac" />
   - Run Wireshark to start capturing network traffic on the configured interfaces.

   - Desktop Environment:

    <img width="300" alt="Desktop Environment" src="https://github.com/user-attachments/assets/d688bf26-84a4-419d-a0eb-6bc0eae6c346" />


## Troubleshooting Steps

### Issue 1: OPNSense Installation Issues
- **Problem**: After downloading the OPNsense installation image, I encountered an issue where the downloaded file was in a compressed .bz2 format. This meant that the image file couldn’t be used directly for installation, as it needed to be decompressed first.
- **Solution**: 
   To resolve this, I used the macOS terminal to navigate to the directory where the installation image was saved. The following steps were taken:
1. Navigating to the Download Directory:
I opened the terminal and used the cd command to move into the "Downloads" folder where the 
OPNsense image was located. The command used was:
2. Decompressing the .bz2 File:
Once inside the correct directory, I ran the bunzip2 command to decompress the .bz2 file, which extracted the ISO image file needed for the installation:

This step successfully extracted the OPNsense installation image, allowing me to proceed with creating a bootable installation drive or using the image in a virtual environment.

### Issue 2: Network Configuration Issue in Ubuntu
- **Problem**: After configuring the network in VirtualBox, Ubuntu did not recognize changes when using `ifconfig` to view the inet of the pfsense machine.
- **Solution**: 
   - Verified that the network adapter in VirtualBox was correctly set up.
   - Restarted the network services in Ubuntu:

## What I Accomplished
- **Network Security Setup**: Successfully set up Ubuntu and pfSense (or OPNsense) to create a virtualized network environment.
- **Wireshark Traffic Analysis**: Captured and analyzed network traffic to identify potential security vulnerabilities or misconfigurations.
- **Network Troubleshooting**: Gained experience in solving common networking issues related to virtual machines and firewall configurations.

## 

