# Threat Detection & Incident Investigation Lab

## Project Overview

This project demonstrates a controlled network security investigation performed in an isolated VirtualBox Host-Only environment.

Kali Linux was used as the security analysis machine and Metasploitable 2 was used as the intentionally vulnerable target.

The investigation focused on network reconnaissance, packet analysis, HTTP traffic analysis, IOC identification, and incident documentation.

## Lab Environment

| Component        | Details              |
| ---------------- | -------------------- |
| Security Machine | Kali Linux           |
| Target Machine   | Metasploitable 2     |
| Network          | VirtualBox Host-Only |
| Kali IP          | 192.168.56.103       |
| Target IP        | 192.168.56.102       |

## Tools Used

* **Nmap** — Network reconnaissance and service/version enumeration
* **Wireshark** — Packet capture and network traffic analysis
* **Kali Linux** — Security investigation environment
* **Metasploitable 2** — Intentionally vulnerable lab target

## Investigation Workflow

### 1. Network Reconnaissance

Nmap was used to identify exposed services and service versions on the target.

```bash
nmap -sV 192.168.56.102
```

### 2. Packet Capture

Wireshark was used to capture and inspect network traffic generated during the investigation.

### 3. TCP Analysis

TCP SYN packets were analyzed to identify network reconnaissance activity.

### 4. HTTP Analysis

HTTP communication involving TCP port 80 was captured and analyzed.

### 5. IOC Identification

The following network indicators were documented:

* Source IP: `192.168.56.103`
* Destination IP: `192.168.56.102`
* Protocols: TCP, HTTP
* Observed Activity: Network reconnaissance

### 6. Incident Documentation

The investigation was documented using:

* IOC analysis
* Incident timeline
* Final investigation findings
* Incident report

## Key Findings

* Network reconnaissance activity was identified through Nmap-generated traffic.
* TCP SYN packets were observed in Wireshark.
* HTTP traffic involving TCP port 80 was identified.
* Packet-level evidence was collected between the source and target systems.
* The investigation demonstrated a basic SOC-style network investigation workflow.

## Evidence

The project contains screenshots demonstrating:

1. Nmap service scan
2. Nmap findings
3. Wireshark traffic capture
4. TCP packet analysis
5. HTTP traffic analysis
6. HTTP request analysis
7. SYN scan analysis
8. IOC analysis
9. Incident timeline
10. Final investigation findings
11. Incident report

## Security Scope

All activities were performed in an isolated Host-Only VirtualBox cybersecurity laboratory.

No external systems were targeted.

## Skills Demonstrated

* Network Reconnaissance
* Nmap
* Wireshark
* TCP Traffic Analysis
* HTTP Traffic Analysis
* IOC Identification
* Incident
