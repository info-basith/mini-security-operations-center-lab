# Mini Security Operations Center (SOC) Lab

# 

# A practical, isolated Security Operations Center (SOC) laboratory designed to develop hands-on skills in network security monitoring, attack detection, log analysis, incident investigation, security hardening, and defensive security operations.

# 

# The laboratory is built using VMware Workstation and a small virtualized corporate-style network consisting of Kali Linux, Ubuntu Server, and a planned Windows endpoint.

# 

# \---

# 

# 1\. Project Overview

# 

# This project demonstrates the design and implementation of a small, isolated SOC environment for studying how security events can be generated, detected, investigated, documented, and mitigated in a controlled laboratory.

# 

# The project follows a practical defensive-security workflow:

# 

# Lab Design

# &#x20;   ↓

# Network Configuration

# &#x20;   ↓

# Baseline Establishment

# &#x20;   ↓

# Controlled Security Events

# &#x20;   ↓

# Detection

# &#x20;   ↓

# Evidence Collection

# &#x20;   ↓

# Incident Investigation

# &#x20;   ↓

# Response

# &#x20;   ↓

# Security Hardening

# &#x20;   ↓

# Retesting

# &#x20;   ↓

# Continuous Improvement

# 

# The long-term goal is to expand the laboratory toward SIEM, detection engineering, threat hunting, security automation, and security-focused machine learning.

# 

# \---

# 

# 2\. Project Objectives

# 

# The main objectives are to:

# 

# \* Build an isolated SOC laboratory using virtual machines.

# \* Understand practical network segmentation.

# \* Establish a baseline for normal network and system activity.

# \* Generate controlled security events inside the lab.

# \* Detect suspicious network and authentication activity.

# \* Analyze network traffic and system logs.

# \* Investigate incidents using timestamps, IP addresses, ports, protocols, and authentication events.

# \* Build incident timelines.

# \* Document evidence and investigation findings.

# \* Apply security hardening measures.

# \* Repeat selected tests to evaluate security improvements.

# \* Develop practical SOC analyst skills.

# \* Produce professional documentation suitable for a cybersecurity portfolio.

# 

# \---

# 

# 3\. Current Lab Architecture

# 

# The current laboratory contains:



|System|Role|Network|
|-|-|-|
|Kali Linux|Security testing / SOC analyst workstation|Internet + isolated SOC network|
|Ubuntu Server|Linux monitored server|Isolated SOC network|
|Windows Endpoint|Planned monitored endpoint|Isolated SOC network|





# Network Design

# 

# VMnet8

# 

# \* VMware NAT network.

# \* Provides Internet connectivity to Kali.

# \* Kali obtains its Internet-side address using DHCP.

# 

# VMnet2

# 

# \* VMware Host-only network.

# \* Subnet: `10.10.10.0/24`.

# \* DHCP disabled.

# \* Used as the isolated SOC laboratory network.

# 

# 4\. Hardware Environment

# 

# The laboratory is designed to operate within the available laptop resources.

# 

# Host System

# 

# \* CPU: Intel Core i7-7600U

# \* Generation: 7th Gen

# \* RAM: 16 GB

# \* Storage: 512 GB

# \* Host OS: Windows 11

# \* Hypervisor: VMware Workstation

# 

# Because the host has 16 GB RAM, the laboratory is being developed incrementally rather than running many virtual machines simultaneously.

# 

# The initial environment prioritizes:

# 

# 1\. Kali Linux

# 2\. Ubuntu Server

# 3\. Windows endpoint

# 4\. Monitoring and logging components

# 5\. SIEM components where hardware resources permit

# 

# Resource usage will be monitored as the laboratory grows.

# 

# 5\. SOC Workflow

# 

# The project is designed around the following SOC workflow:

# 

# Phase 1 — Lab Preparation

# 

# \* Virtualization environment

# \* Network segmentation

# \* Virtual machine deployment

# \* IP addressing

# \* Connectivity verification

# 

# Phase 2 — Baseline

# 

# \* Normal network traffic

# \* Normal authentication activity

# \* Running services

# \* Open ports

# \* System logs

# \* Expected user activity

# 

# Phase 3 — Security Events

# 

# Controlled laboratory events may include:

# 

# \* Network reconnaissance

# \* Port scanning

# \* Authentication failures

# \* Suspicious login activity

# \* Service enumeration

# \* Other controlled defensive-security scenarios

# 

# All testing will be performed against laboratory systems.

# 

# Phase 4 — Detection

# 

# Evidence will be collected using tools such as:

# 

# \* Nmap

# \* Wireshark

# \* Linux logging mechanisms

# \* Windows Event Viewer

# \* tcpdump

# \* Additional detection tools as the lab develops

# 

# Phase 5 — Investigation

# 

# Each incident will be investigated using:

# 

# \* Source IP

# \* Destination IP

# \* Source and destination ports

# \* Protocol

# \* Timestamp

# \* Authentication events

# \* Service information

# \* Network packets

# \* System logs

# \* Other relevant indicators

# 

# Phase 6 — Incident Documentation

# 

# Each significant investigation will produce:

# 

# \* Incident summary

# \* Timeline

# \* Indicators of compromise or suspicious activity

# \* Evidence

# \* Analysis

# \* Impact assessment

# \* Recommended response

# \* Lessons learned

# 

# Phase 7 — Hardening

# 

# Selected security controls will be implemented and tested again to determine whether suspicious activity is reduced, detected differently, or blocked.

# 

# \---

# 

# 6. Tools

# 

# Currently Used

# 

# \* VMware Workstation

# \* Kali Linux

# \* Ubuntu Server

# \* Nmap

# \* Wireshark

# \* Linux networking tools

# \* Linux logging mechanisms

# 

# Planned

# 

# \* Windows Event Viewer

# \* tcpdump

# \* SIEM platform

# \* Detection rules

# \* Threat-hunting tools

# \* Security automation scripts

# 

# 7. Repository Structure



# mini-security-operations-center-lab/

# │

# ├── README.md

# ├── .gitignore

# │

# ├── 01-Lab-Foundation/

# │   └── architecture/

# │

# ├── 02-Network-Configuration/

# │

# ├── 03-Baseline/

# │

# ├── 04-Detection-Scenarios/

# │

# ├── 05-Evidence/

# │

# ├── 06-Incident-Reports/

# │

# ├── 07-Hardening/

# │

# ├── 08-Detection-Rules/

# │

# ├── 09-Scripts/

# │

# ├── 10-SIEM/

# │

# ├── 11-Threat-Hunting/

# │

# └── 12-Project-Report/

# 

# Each section will be populated as the laboratory progresses.

# 

# 8\. Project Status

# 

# Completed

# 

# \* \[x] VMware laboratory environment selected

# \* \[x] Kali Linux configured

# \* \[x] Ubuntu Server deployed

# \* \[x] VMnet8 NAT network configured for Kali Internet access

# \* \[x] VMnet2 isolated Host-only network created

# \* \[x] Kali connected to VMnet2

# \* \[x] Kali assigned static SOC IP `10.10.10.10/24`

# \* \[x] Ubuntu connected to VMnet2

# \* \[x] Ubuntu assigned static SOC IP `10.10.10.20/24`

# \* \[x] Ubuntu configured without a default Internet route

# \* \[x] Persistent network configuration established

# \* \[x] Initial network architecture established

# 

# In Progress

# 

# \* \[ ] Verify complete reboot persistence

# \* \[ ] Document network baseline

# \* \[ ] Document normal system activity

# \* \[ ] Deploy required monitored services

# \* \[ ] Create first controlled detection scenario

# 

# Planned

# 

# \* \[ ] Windows endpoint

# \* \[ ] Authentication monitoring

# \* \[ ] Network reconnaissance detection

# \* \[ ] Incident investigation workflow

# \* \[ ] Incident reports

# \* \[ ] Security hardening

# \* \[ ] Detection rules

# \* \[ ] SIEM integration

# \* \[ ] Threat hunting

# \* \[ ] Security automation

# \* \[ ] Advanced SOC capabilities

# 

# \---

# 

# 9\. Evidence and Documentation

# 

# The repository will contain sanitized and relevant project evidence, including:

# 

# \* Network diagrams

# \* Configuration documentation

# \* Command output where useful

# \* Screenshots

# \* Detection results

# \* Investigation timelines

# \* Incident reports

# \* Detection rules

# \* Hardening results

# 

# Sensitive information such as credentials, private keys, tokens, and personal data will not be committed to the repository.

# 

# \---



# 10\. Learning Outcomes

# 

# By completing this project, the objective is to develop practical understanding of:

# 

# \* Networking

# \* Linux administration

# \* Windows security monitoring

# \* Network traffic analysis

# \* Log analysis

# \* Detection engineering

# \* Incident response

# \* Threat hunting

# \* Security hardening

# \* SIEM concepts

# \* Security automation

# \* SOC operational workflows

# 

# \---

# 

# 11\. Project Philosophy

# 

# This project focuses on understanding the complete defensive-security process rather than simply running security tools.

# 

# The key question for each exercise is:

# 

# > What happened, how do we know it happened, how can we detect it, how should we investigate it, and how can we improve the environment afterward?

# 

# The project therefore emphasizes evidence-based investigation, documentation, repeatable procedures, and measurable improvements.

# 

# \---

# 

# 12\. Disclaimer

# 

# This laboratory is designed for authorized cybersecurity education and defensive-security practice.

# 

# All security testing will be performed against systems intentionally created and controlled for this laboratory.

# 

# No unauthorized systems or networks are targeted.

# 

# \---

# 

# 13\. Author

# 

# Abdul Basith

# 

# Cybersecurity / SOC Learning Project

# 

# This repository documents the development of the laboratory, practical exercises, investigations, detection work, and lessons learned throughout the project.

# 

# \---

# 

# License

# 

# This project is intended primarily as an educational cybersecurity portfolio and laboratory documentation project.



