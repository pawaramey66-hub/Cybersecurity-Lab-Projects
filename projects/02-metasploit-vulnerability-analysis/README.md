
 Project 2: Remote Code Execution & Multi-Stage Troubleshooting via Metasploit

 🛠️ Tools Used
* VMware Workstation Pro
* Metasploit Framework (msfconsole)
* Kali Linux 2026 (Attacker)
* Windows 7 Ultimate x86 (Target)

 📋 Objective
To simulate a cyber attack using the MS17-010 (EternalBlue/EternalRomance) vulnerability on a target system, analyze intermediate authentication failures, and secure root/SYSTEM access.

 🚀 Step-by-Step Pentesting Timeline & Troubleshooting
1. **Initial Vector**: Target identified as vulnerable to MS17-010 via Port 445 (SMB).
2. **Phase 1 (Failure Analysis - Architecture)**: Tried `exploit/windows/smb/ms17_010_eternalblue`. Exploit failed because the target system was 32-bit (x86), while the module strictly demanded 64-bit architecture.
3. **Phase 2 (Failure Analysis - Authentication)**: Switched to `exploit/windows/smb/ms17_010_psexec` with a 32-bit payload. Attempted Guest authentication, which failed with a `STATUS_ACCOUNT_DISABLED` error.
4. **Phase 3 (Bypass & Success)**: Provided active local administrator credentials (`Administrator` / `1234`). Executed the exploit.
5. **Result**: Successfully triggered a write-what-where primitive, bypassed system protections, and spawned a **Meterpreter session with NT AUTHORITY\SYSTEM privileges**.

 📸 Exploitation Proof
<img width="1577" height="609" alt="Screenshot 2026-08-07 233335" src="https://github.com/user-attachments/assets/72801a95-4503-49aa-a689-885012e5dba1" />
