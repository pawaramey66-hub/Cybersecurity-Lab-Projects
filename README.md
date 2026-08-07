# Project 1: Basic Network Mapping and Vulnerability Discovery

🛠️ Tools Used
* VirtualBox
* Kali Linux (Attacker Machine)
* Metasploitable2 / Windows 10 VM (Target Machine)
* Nmap

📋 Objective
To scan a target machine within a private virtual lab network to discover active hosts, open ports, and running services.

🚀 Steps Performed
1. **Network Discovery**: Ran `sudo netdiscover -r 192.168.56.0/24` to find the target's IP address.
2. **Port Scanning**: Executed a stealth scan using Nmap: `nmap -sS -sV -O <Target_IP>`
3. **Analysis**: Identified open ports like 21 (FTP), 22 (SSH), and 80 (HTTP) along with their software versions.

📸 Lab Screenshots
*(Ithe tumcha Kali terminal cha scan screenshot select karun directly web page var drag-and-drop / paste kara)*

🧠 Key Learnings
* Understood how Nmap's SYN stealth scan works.
* Learned how outdated service versions create vulnerabilities for potential exploits.
