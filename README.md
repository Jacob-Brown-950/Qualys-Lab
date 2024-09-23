# Vulnerability Management Lab

## Objective

The goal of this project is to set up a vulnerability management lab using Qualys Community Edition. This home lab is designed to simulate a Windows 10 environment where outdated software is intentionally installed to create vulnerability flags. By doing this, I aim to gain practical experience in identifying and remediating vulnerabilities, a critical skill for my career as an entry-level IT technician.

### Skills Learned

- Understanding of vulnerability management processes.
- Practical experience with Qualys for vulnerability scanning.
- Knowledge of configuring virtual machines and networking.
- Experience in identifying and remediating software vulnerabilities.
- Insight into the importance of regular software updates and patches.

### Tools Used

- **Qualys Community Edition**: For vulnerability scanning.
- **Oracle VirtualBox**: To simulate a Windows 10 machine.
- **Outdated Software**: VLC Media Player (version 1.1.1) and Firefox (version 1.4.0) to create vulnerabilities.

## Table of Contents

1. [Introduction](#introduction)
2. [Setting Up the Windows 10 VM](#setting-up-the-windows-10-vm)
3. [Creating Vulnerabilities](#creating-vulnerabilities)
4. [Qualys Virtual Scanner Setup](#qualys-virtual-scanner-setup)
5. [Running the Scans](#running-the-scans)
6. [Remediation](#remediation)
7. [Conclusion](#conclusion)

## Introduction

This guide outlines the steps taken to set up a vulnerability management lab. The focus is on using Qualys Community Edition to scan a Windows 10 virtual machine with intentionally outdated software.

## Setting Up the Windows 10 VM

1. **Download Oracle VirtualBox**:
   - Visit the [Oracle VirtualBox website](https://www.virtualbox.org/) and download the latest version for your operating system.
   - Follow the installation instructions provided on the site.

2. **Obtain a Windows 10 ISO File**:
   - You can download a Windows 10 ISO from the [Microsoft website](https://www.microsoft.com/en-us/software-download/windows10). 
   - Choose the edition and language you prefer, and follow the prompts to download.

3. **Create a Windows 10 VM** in Oracle VirtualBox:
   - Open VirtualBox and click "New" to create a new VM.
   - Set the name, type, and version (Windows 10).
   - Allocate memory (at least 4 GB recommended).
   - Create a virtual hard disk and set its size (20 GB is a good starting point).

4. **Set the VM to a Static IP Address**:
   - Go to the network settings of your VM and choose "Bridged Adapter" for network connectivity.
   - Set a static IP address within your local network settings to avoid issues with DHCP during scanning.

## Creating Vulnerabilities

To simulate vulnerabilities, I intentionally downloaded outdated versions of software:

1. **VLC Media Player (version 1.1.1)**:
   - Visit the [VLC Releases](https://download.videolan.org/pub/videolan/vlc/1.1.1/) page.
   - Download the appropriate installer for Windows and install it in your VM.

2. **Firefox Browser (version 1.4.0)**:
   - Navigate to the [Mozilla Firefox Releases](https://ftp.mozilla.org/pub/firefox/releases/1.0.4/) directory.
   - Download the Windows installer for version 1.4.0 and install it in your VM.

## Qualys Virtual Scanner Setup

1. **Download and Set Up Qualys Community Edition**:
   - Go to the [Qualys Community Edition page](https://www.qualys.com/community-edition/) and sign up for an account.
   - Follow the prompts to create your account and download the virtual scanner.

2. **Import the Virtual Scanner into VirtualBox**:
   - After downloading the Qualys scanner, open VirtualBox and select "Import Appliance."
   - Choose the Qualys scanner file and follow the instructions to import it.

3. **Configure an IP Range in Qualys**:
   - Log into your Qualys account.
   - Go to the "Scans" section and create a new scan by specifying the IP range that includes your Windows 10 VM.

4. **Disable the Windows Firewall Temporarily**:
   - To allow the scans to run effectively, you may need to disable the Windows Firewall on your VM:
     - Go to Control Panel > System and Security > Windows Defender Firewall > Turn Windows Defender Firewall on or off.

## Running the Scans

I performed the following scans:

1. **Unauthenticated Scan**: Identified open ports but provided limited information.
2. **Authenticated Scan**: Detected vulnerabilities in the outdated applications.

### Scan Results

- **Not Authenticated Scan**: [View PDF](https://github.com/yourusername/yourrepo/raw/main/unauthenticated_scan.pdf)
- **Authenticated Scan**: [View PDF](https://github.com/yourusername/yourrepo/raw/main/authenticated_scan.pdf)

## Remediation

After identifying the vulnerabilities, I removed the outdated software and ran another authenticated scan to verify remediation:

- **Authenticated Scan After Software Removal**: [View PDF](https://github.com/yourusername/yourrepo/raw/main/authenticated_scan_after_removal.pdf)

### Patching Windows Update Vulnerabilities

I also noticed vulnerabilities due to missing Windows security updates. After installing the necessary patches, I ran a final scan:

- **Final Scan After Windows Updates**: [View PDF](https://github.com/yourusername/yourrepo/raw/main/final_scan.pdf)

## Conclusion

Through this project, I successfully identified and remediated several vulnerabilities. It emphasizes the importance of keeping both applications and operating systems up to date to minimize security risks. This hands-on experience is invaluable as I continue to build my skills in vulnerability management.
