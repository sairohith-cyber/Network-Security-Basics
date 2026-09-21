# Week 3 Cybersecurity Assessment

## Overview

This repository contains my practical work for Week 3 of the Cybersecurity Internship.

The project focuses on basic network security assessment using Nmap and
Wireshark in an authorized VirtualBox lab environment.

## Objectives

- Discover active hosts on the lab network
- Identify open ports and services
- Perform advanced Nmap scans
- Capture and analyze network traffic
- Identify security findings
- Perform basic vulnerability/risk assessment
- Apply security hardening
- Compare the network state before and after hardening

## Lab Environment

| Component | Details 
|---|---|
| Assessment Machine | Kali Linux |
| Target | Windows |
| Target IP | 192.168.233.1 |
| Network | 192.168.233.0/24 |
| Network Type | VirtualBox Host-Only |

## Tools Used

- Nmap
- Wireshark
- Kali Linux
- Windows Firewall
- VirtualBox

## Nmap Assessment

The Nmap assessment included:

- Host discovery
- Basic TCP scan
- Service/version detection
- OS detection
- TCP SYN scan
- Limited UDP scan
- Nmap vulnerability scripts

### Main Services Identified

| Port | Protocol | Service |
|---|---|---|
| 135 | TCP | MSRPC |
| 139 | TCP | NetBIOS-SSN |
| 445 | TCP | Microsoft-DS / SMB |

## Wireshark Analysis

Wireshark was used to analyze:

- TCP
- UDP
- DNS
- ICMP
- ARP
- TCP SYN traffic
- TCP RST traffic

The packet analysis helped explain the network activity observed during
the Nmap scans.

## Security Findings

The main findings were:

1. SMB exposure on TCP/445
2. NetBIOS exposure on TCP/139
3. RPC exposure on TCP/135
4. Multiple Windows services exposed
5. Additional reachable high-numbered ports

## Security Hardening

Windows Firewall rules were configured to restrict:

- TCP/135
- TCP/139
- TCP/445

Before and after Nmap results are included in the `04-Hardening`
directory.

