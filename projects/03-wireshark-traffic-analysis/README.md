 Project 3: Network Traffic Analysis & Plain-Text Credential Sniffing via Wireshark

 🛠️ Tools Used
* VMware Workstation Pro
* Wireshark (Deep Packet Inspection Tool)
* Kali Linux Firefox Browser

 📋 Objective
To analyze live unencrypted HTTP traffic within a virtual network to detect data leakages, monitor active protocols, and inspect plain-text credential handling.

 🚀 Steps Performed
1. **Packet Capture**: Launched Wireshark with root privileges and initialized live sniffing on interface `eth0`.
2. **Traffic Generation**: Navigated to an unencrypted HTTP application platform and simulated an active login request.
3. **Filtering Traffic**: Applied targeted display filters `http.request.method == "POST"` to isolate data submission packets from routine background network noise.
4. **Deep Inspection**: Selected the captured HTTP POST packet and expanded the `HTML Form URL Encoded` layer to reveal the application payload parameters.

 📸 Sniffing Output Evidence
<img width="1600" height="917" alt="image" src="https://github.com/user-attachments/assets/47197666-be9f-4ff4-87e4-c274472a22be" />
