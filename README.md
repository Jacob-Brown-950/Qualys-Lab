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

1. **Create a Windows 10 VM** in Oracle VirtualBox using an ISO file.
2. **Set the VM to a static IP address** to avoid issues with DHCP during scanning.

## Creating Vulnerabilities

To simulate vulnerabilities, I intentionally downloaded outdated versions of software:

- **VLC Media Player (version 1.1.1)**: [VLC Releases](https://download.videolan.org/pub/videolan/vlc/1.1.1/)
- **Firefox Browser (version 1.4.0)**: [Mozilla Firefox Releases](https://ftp.mozilla.org/pub/firefox/releases/1.0.4/)

These outdated applications serve as examples of common vulnerabilities in software.

## Qualys Virtual Scanner Setup

1. **Download and set up Qualys Community Edition** and import the virtual scanner into VirtualBox.
2. **Configure an IP range in Qualys** that includes the Windows 10 VM.
3. **Disable the Windows Firewall** temporarily to allow scans to run effectively.

## Running the Scans

I performed the following scans:

1. **Unauthenticated Scan**: Identified open ports but provided limited information.
2. **Authenticated Scan**: Detected vulnerabilities in the outdated applications.

### Scan Results

- **Not Authenticated Scan**: [PDF]
- **Authenticated Scan**: [PDF]

## Remediation

After identifying the vulnerabilities, I removed the outdated software and ran another authenticated scan to verify remediation:

- **Authenticated Scan After Software Removal**: [PDF]

### Patching Windows Update Vulnerabilities

I also noticed vulnerabilities due to missing Windows security updates. After installing the necessary patches, I ran a final scan:

- **Final Scan After Windows Updates**: [PDF]

## Conclusion

Through this project, I successfully identified and remediated several vulnerabilities. It emphasizes the importance of keeping both applications and operating systems up to date to minimize security risks. This hands-on experience is invaluable as I continue to build my skills in vulnerability management.

