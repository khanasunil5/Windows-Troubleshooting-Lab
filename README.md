# Windows Troubleshooting Lab (Domain Environment)

## Overview
This project is a hands-on **Windows troubleshooting and Service Desk simulation** built in a controlled virtualised domain environment.  
The lab focuses on diagnosing and resolving **realistic end-user and system issues** commonly encountered in **IT Support, Service Desk, and IT Technician roles**.

All issues were intentionally reproduced, investigated, resolved, and documented using standard IT tools and best practices, with supporting evidence captured throughout.

---

## Lab Architecture

**Domain:** lab.local  
**Network Type:** Host-only (isolated internal network)

### Machines
- **Domain Controller:** DC01  
- **Client Machine:** CLIENT01  

### IP Scheme
- **DC01:** 192.168.100.10 (Static IP)

Using a host-only network ensures full communication between the domain controller and client machine while remaining isolated from external networks. This closely simulates an internal corporate environment.

---

## Technologies Used
- VMware Workstation
- Windows Server 2019 (Domain Controller)
- Windows 11 (Client)
- Active Directory Domain Services (AD DS)
- DNS
- Event Viewer
- Services.msc
- Windows Registry
- NTFS & Share Permissions
- Windows Update components
- Print Spooler service

---

## Virtual Machine Setup

Both systems were created as virtual machines using **VMware Workstation**.  
Configurations were chosen to balance performance with the host system’s **8 GB RAM**, while maintaining a realistic enterprise-style setup.

---

### Domain Controller (DC01)

- **Operating System:** Windows Server 2019 (Desktop Experience)
- **Memory:** 2 GB RAM
- **CPU:** 1 processor, 2 cores
- **Storage:** 60 GB (single virtual disk)
- **Network:** Host-only
- **IP Address:** 192.168.100.10 (Static)

The static IP ensures domain and DNS stability, which is critical in Active Directory environments.

---

### Client Machine (CLIENT01)

- **Operating System:** Windows 11
- **Memory:** 2 GB RAM
- **CPU:** 1 processor, 2 cores
- **Storage:** 40 GB
- **Network:** Host-only

CLIENT01 is joined to the lab.local domain and used to simulate real end-user issues and troubleshooting scenarios.

---

## Virtualisation & Performance Optimisation

As the host machine has **8 GB of RAM**, the lab was configured with stability and performance in mind:

- Domain Controller and client VM were only run simultaneously when required
- Unused VMs were paused or shut down
- Windows visual effects were disabled within the VMs
- VMware memory usage was carefully managed

This mirrors real-world IT environments where systems must be operated within resource constraints.

---

## Domain Controller Configuration

- Installed Windows Server 2019 (Desktop Experience)
- Renamed server to **DC01**
- Configured a static IP address
- Installed **Active Directory Domain Services** and **DNS**
- Promoted server to a Domain Controller
- Created the **lab.local** domain

Domain services were verified before client testing began.

---

## Client Configuration

- Installed Windows 11
- Joined CLIENT01 to the **lab.local** domain
- Verified domain authentication using Active Directory user accounts

---

## Completed Troubleshooting Scenarios

This lab documents the following Service Desk–style tickets:

- Corrupted Windows user profile (temporary profile issue)
- Internal network connectivity issue caused by DNS misconfiguration
- Windows Search service disabled
- Printer failure due to Print Spooler service configuration
- Windows Updates failing due to stopped services
- Shared folder access denied caused by NTFS permission issues

Each scenario includes:
- User-reported symptoms
- Investigation steps
- Root cause analysis
- Resolution
- Verification
- Supporting screenshots and evidence

---

## Project Structure

windows-troubleshooting-lab/
│
├── tickets/ # Service Desk-style ticket write-ups
├── knowledge-base/ # Reusable troubleshooting guides
├── evidence/ # Screenshots and command output
└── lab-environment/ # Architecture and configuration details

---

## Skills Demonstrated

- Windows desktop troubleshooting
- Active Directory user and profile management
- DNS diagnosis and resolution
- Windows services and dependencies
- Printer and Print Spooler troubleshooting
- Windows Update repair
- NTFS and share permission analysis
- Event Viewer log analysis
- Professional IT documentation and ticketing workflow

---

## Purpose of This Lab

This project was created to demonstrate **job-ready IT Support skills** through practical troubleshooting, structured documentation, and realistic problem-solving scenarios commonly faced in entry-level IT roles.


