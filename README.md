# Metasploitable Penetration Testing Lab

## Overview
This lab demonstrates a penetration testing workflow using Kali Linux against the vulnerable Metasploitable2 machine.

## Tools Used
- Kali Linux
- Nmap
- Metasploit Framework

## Steps Performed

### 1. Target Identification
The target IP address was identified using `ifconfig`.

### 2. Network Scanning
An Nmap scan was performed to discover open ports and services.

Example command:
nmap -sV -A <target-ip> 
nmap -sV -A 192.168.56.103

### 3. Vulnerability Discovery
The FTP service `vsftpd 2.3.4` was identified as vulnerable.

### 4. Exploitation
Using Metasploit module:

exploit/unix/ftp/vsftpd_234_backdoor

Steps:
- Start msfconsole
- Load exploit module
- Set RHOSTS
- Run exploit

### 5. Result
Shell access was successfully obtained on the target machine.

## Skills Learned
- Network scanning
- Service enumeration
- Vulnerability identification
- Exploitation using Metasploit
- Remote shell access
