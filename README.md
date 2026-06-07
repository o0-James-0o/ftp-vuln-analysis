# Dictionary Attack: Exploiting Vulnerable FTP with Medusa


<p align="center">
  <img src="https://img.shields.io/badge/Kali%20Linux-557C94?style=for-the-badge&amp;logo=kalilinux&amp;logoColor=white" alt="Kali Linux">
  <img src="https://img.shields.io/badge/Metasploitable%202-8B0000?style=for-the-badge&amp;logo=linux&amp;logoColor=white" alt="Metasploitable 2">
  <img src="https://img.shields.io/badge/Nmap-005FAD?style=for-the-badge&amp;logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA2NCA2NCI%2BPHBhdGggZmlsbD0iIzlFRENGQSIgZD0iTTIgMzJDMTIgMTggMjMgMTIgMzQgMTJjMTMgMCAyMyA4IDI4IDIwLTggMTEtMTkgMTctMzIgMTdDMTggNDkgOSA0MiAyIDMyeiIvPjxwYXRoIGZpbGw9IiM1RUMxRUMiIGQ9Ik0yIDMyYzkgNSAxOSA4IDMwIDggMTIgMCAyMi0zIDMwLTgtOCAxMS0xOSAxNy0zMiAxN0MxOCA0OSA5IDQyIDIgMzJ6Ii8%2BPGNpcmNsZSBjeD0iMzQiIGN5PSIzMSIgcj0iMTIiIGZpbGw9IiMzQTgzQTgiLz48Y2lyY2xlIGN4PSIzNCIgY3k9IjMxIiByPSI1IiBmaWxsPSIjZmZmIi8%2BPGNpcmNsZSBjeD0iNDIiIGN5PSIyMiIgcj0iMyIgZmlsbD0iI2ZmZiIvPjwvc3ZnPg%3D%3D" alt="Nmap">
  <img src="https://img.shields.io/badge/Medusa-E95420?style=for-the-badge&amp;logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA2NCA2NCI%2BPGcgZmlsbD0ibm9uZSIgc3Ryb2tlPSIjZmZmIiBzdHJva2Utd2lkdGg9IjUiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCI%2BPHBhdGggZD0iTTIwIDI2Yy04LTItMTAtOS00LTE1TTI3IDIwYy00LTggMi0xNCA3LTE2TTM3IDIwYzQtOCAxMi04IDE1LTJNNDQgMjdjOSAwIDEyLTYgOS0xM00xOCAzNWMtOCAxLTEzLTMtMTItMTBNNDcgMzZjOCAzIDEzIDAgMTMtNyIvPjxwYXRoIGQ9Ik0yMiAyOWMwLTggMjAtOCAyMCAwdjExYzAgMTAtNiAxOC0xNCAxOHMtMTQtOC0xNC0xOHoiLz48cGF0aCBkPSJNMjEgMzZjMy04IDktNyAxMS0xIDMtNiAxMC03IDEzIDFNMjggNThjLTEgNC00IDYtOCA2Ii8%2BPC9nPjwvc3ZnPg%3D%3D" alt="Medusa">
  <img src="https://img.shields.io/badge/VirtualBox-183A61?style=for-the-badge&amp;logo=virtualbox&amp;logoColor=white" alt="VirtualBox">
  <img src="https://img.shields.io/badge/Protocols%2FPorts-0F766E?style=for-the-badge&amp;logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA2NCA2NCI%2BCjxnIGZpbGw9Im5vbmUiIHN0cm9rZT0iI2ZmZiIgc3Ryb2tlLXdpZHRoPSI1IiBzdHJva2UtbGluZWNhcD0icm91bmQiIHN0cm9rZS1saW5lam9pbj0icm91bmQiPgo8Y2lyY2xlIGN4PSIzMiIgY3k9IjI0IiByPSIyMCIvPgo8cGF0aCBkPSJNMTIgMjRoNDBNMzIgNHY0ME0xOCAxMGM4IDggMjAgOCAyOCAwTTE4IDM4YzgtOCAyMC04IDI4IDAiLz4KPHBhdGggZD0iTTI1IDQ1aDE0djZIMjV6TTE4IDUxaDI4djhIMTh6TTQgNTVoMTRNNDYgNTVoMTQiLz4KPC9nPgo8L3N2Zz4%3D&amp;logoColor=white" alt="Protocols/Ports">
</p>


> **Information Security lab** demonstrating, in an isolated and authorized environment, how a **Dictionary Attack** works against a vulnerable FTP service.

---

## 📌 Project Description

This repository presents a practical lab developed as a personal project to demonstrate knowledge in offensive security, service enumeration, and dictionary attacks.  
The goal was to demonstrate, in a controlled way, how an attacker can use username and password lists to test authentication combinations against an exposed service.

The demonstration was performed with:

- **Kali Linux** as the attacking machine;
- **Metasploitable 2** as the vulnerable target machine;
- **Nmap** for port and service enumeration;
- **Medusa** to execute the dictionary attack against the **FTP** service.

---

## 🛠️ Environment and Tools Used

### 🖥️ Environment

---

| Image | Resource | Description |
|:---:|---|---|
| <img src="https://api.iconify.design/simple-icons:virtualbox.svg?color=%23183A61" width="32" height="32"> | **Virtualization** | Oracle VirtualBox used to create, run, and isolate the lab virtual machines safely. |
| <img src="https://api.iconify.design/simple-icons:kalilinux.svg?color=%23557C94" width="32" height="32"> | **Attacking machine** | Kali Linux used as the offensive environment for enumeration, wordlist creation, and attack execution. |
| <img src="https://api.iconify.design/simple-icons:linux.svg?color=%238B0000" width="32" height="32"> | **Target machine** | Metasploitable 2 used as an intentionally vulnerable system for security practice in a lab environment. |
| <img src="https://api.iconify.design/tabler:network.svg?color=%230F766E" width="32" height="32"> | **Network** | Isolated virtual network between the VMs, allowing communication between attacker and target without external exposure. |
| <img src="https://api.iconify.design/mdi:server-network.svg?color=%230A66C2" width="32" height="32"> | **Exploited service** | FTP service identified during enumeration and used as the analysis point for the dictionary attack. |
| <img src="https://api.iconify.design/mdi:ethernet.svg?color=%23FACC15" width="32" height="32"> | **Exploited port** | Port **21/tcp**, associated with the FTP protocol, selected to demonstrate automated authentication attempts. |

### ⚙️ Tools

---

| Image | Tool | Purpose |
|:---:|---|---|
| <img src="https://api.iconify.design/mdi:radar.svg?color=%2300AEEF" width="32" height="32"> | **Nmap** | Tool used to identify open ports, active services, and running versions on the Metasploitable 2 target. |
| <img src="https://api.iconify.design/game-icons:medusa-head.svg?color=%23E95420" width="32" height="32"> | **Medusa** | Tool used to automate authentication tests with usernames and passwords defined in custom wordlists. |
| <img src="https://api.iconify.design/simple-icons:gnubash.svg?color=%234EAA25" width="32" height="32"> | **Bash** | Shell used to create, organize, and manipulate the username and password files used during the lab. |
| <img src="https://api.iconify.design/tabler:shield-lock.svg?color=%236D28D9" width="32" height="32"> | **Pentest** | Practical approach used to simulate an authorized, controlled intrusion test focused on technical learning. |

---

## 📁 Repository Structure

The project structure was organized to separate the main documentation, visual evidence, and wordlists used in the lab.

```text
medusa-dictionary-attack-lab/
├── README.md
├── docs/
│   └── images/
│       ├── 01-nmap-enumeration.png
│       ├── 02-nmap-enumeration-result.png
│       ├── 03-wordlist.png
│       ├── 04-medusa-command.png
│       └── 05-medusa-command-result.png
└── wordlists/
    ├── users.txt
    └── pass.txt
```

---

## 🚀 Step-by-Step Execution Guide

---

## 1. 🔎 Enumeration with Nmap

The first stage of the lab was to perform target reconnaissance in order to identify open ports, active services, and running versions.

---

<table>
  <tr>
  </tr>
  <tr>
    <td width="100%" align="center">
      <img src="docs/images/01-nmap-enumeration.png" alt="Nmap execution on Kali Linux" width="100%">
    </td>
  </tr>
</table>

### 🧩 Parameter Explanation

---

| Parameter | Function | Relevance in the lab |
|---|---|---|
| `-sV` | Detects the versions of services found during the scan. | Allows identification of specific technologies running on the target, such as `vsftpd 2.3.4`, helping analyze the attack surface. |
| `-p` | Manually defines which ports will be scanned by Nmap. | Directs enumeration to relevant ports, making the scan more objective and aligned with the lab scope. |
| `21,22,80,445,139` | Lists the selected ports for the scan. | Includes common services such as FTP, SSH, HTTP, and SMB, allowing comparison of different exposure points on the target. |
| `192.168.56.103` | Defines the IP address of the Metasploitable 2 target machine. | Represents the vulnerable host used in the controlled environment for the reconnaissance stage. |

### 📊 Identified Result

---

<table>
  <tr>
  </tr>
  <tr>
    <td width="100%" align="center">
      <img src="docs/images/02-nmap-enumeration-result.png" alt="Nmap enumeration result on Kali Linux" width="100%">
    </td>
  </tr>
</table>

### 🧠 Enumeration Analysis

---

The service selected for the lab was **FTP**, identified on port `21/tcp`.

<table width="100%">
  <tr>
    <th width="12%">Port</th>
    <th width="13%">Service</th>
    <th width="25%">Version</th>
    <th width="50%">Observation</th>
  </tr>
  <tr>
    <td><code>21/tcp</code></td>
    <td><strong>FTP</strong></td>
    <td><code>vsftpd 2.3.4</code></td>
    <td>Service selected for the dictionary attack test with Medusa.</td>
  </tr>
  <tr>
    <td><code>22/tcp</code></td>
    <td><strong>SSH</strong></td>
    <td><code>OpenSSH 4.7p1</code></td>
    <td>Remote access service identified during enumeration.</td>
  </tr>
  <tr>
    <td><code>80/tcp</code></td>
    <td><strong>HTTP</strong></td>
    <td><code>Apache httpd 2.2.8</code></td>
    <td>Active web server on the target, indicating HTTP application exposure.</td>
  </tr>
  <tr>
    <td><code>139/tcp</code></td>
    <td><strong>NetBIOS/SMB</strong></td>
    <td><code>Samba smbd 3.X - 4.X</code></td>
    <td>Service related to sharing and communication in Windows/Linux networks.</td>
  </tr>
  <tr>
    <td><code>445/tcp</code></td>
    <td><strong>SMB</strong></td>
    <td><code>Samba smbd 3.X - 4.X</code></td>
    <td>File-sharing service exposed on the target machine.</td>
  </tr>
</table>

> Enumeration is a critical stage in penetration testing because it helps identify which attack surfaces are exposed before any exploitation attempt.

---

## 2. 📚 Wordlist Creation

After identifying the FTP service, two simple lists were created for educational purposes:

- a list containing possible **usernames**;
- a list containing possible **passwords**.

---

<table>
  <tr>
  </tr>
  <tr>
    <td width="100%" align="center">
      <img src="docs/images/03-wordlist.png" alt="Creation of users.txt and pass.txt wordlists on Kali Linux" width="100%">
    </td>
  </tr>
</table>

### 📁 File Structure

#### `users.txt`

```text
user
msfadmin
admin
root
```

#### `pass.txt`

```text
123456
password
qwerty
msfadmin
```

### 📝 Technical Note

The `>` operator was used to redirect the output of the `echo` command into `.txt` files.

---

<table width="100%">
  <tr>
    <th width="18%">File</th>
    <th width="32%">Content</th>
    <th width="50%">Purpose</th>
  </tr>
  <tr>
    <td><code>users.txt</code></td>
    <td>Possible usernames</td>
    <td>List used by Medusa with the <code>-U</code> parameter to test usernames during the dictionary attack.</td>
  </tr>
  <tr>
    <td><code>pass.txt</code></td>
    <td>Possible passwords</td>
    <td>List used by Medusa with the <code>-P</code> parameter to test passwords associated with the provided users.</td>
  </tr>
</table>

> In a real defensive environment, common passwords such as `123456`, `password`, and `qwerty` should be blocked by password policies.

---

## 3. ⚡ Dictionary Attack with Medusa

With the FTP service identified and the wordlists created, the dictionary attack was executed using **Medusa**.

---

<table>
  <tr>
  </tr>
  <tr>
    <td width="100%" align="center">
      <img src="docs/images/04-medusa-command.png" alt="Medusa command execution against the FTP service" width="100%">
    </td>
  </tr>
</table>

### 🧩 Parameter Explanation

---

<table width="100%">
  <tr>
    <th width="20%">Parameter</th>
    <th width="35%">Function</th>
    <th width="45%">Relevance in the lab</th>
  </tr>
  <tr>
    <td style="white-space: nowrap;"><code>-h 192.168.56.103</code></td>
    <td>Defines the target host to be tested by the tool.</td>
    <td>Directs the attack to the Metasploitable 2 machine previously identified during enumeration.</td>
  </tr>
  <tr>
    <td style="white-space: nowrap;"><code>-U users.txt</code></td>
    <td>Defines the file containing the username list.</td>
    <td>Allows Medusa to test the usernames created in the lab custom wordlist.</td>
  </tr>
  <tr>
    <td style="white-space: nowrap;"><code>-P pass.txt</code></td>
    <td>Defines the file containing the password list.</td>
    <td>Allows testing common password combinations against the users defined in the <code>users.txt</code> file.</td>
  </tr>
  <tr>
    <td style="white-space: nowrap;"><code>-M ftp</code></td>
    <td>Defines the module/protocol used in the attack.</td>
    <td>Specifies that the test will be performed against the FTP service exposed on port <code>21/tcp</code>.</td>
  </tr>
  <tr>
    <td style="white-space: nowrap;"><code>-t 6</code></td>
    <td>Defines the number of parallel tasks executed by Medusa.</td>
    <td>Improves test efficiency by allowing multiple simultaneous attempts within the controlled environment.</td>
  </tr>
</table>

### 📊 Result Obtained

During execution, Medusa tested combinations between the provided usernames and passwords.  
The lab resulted in the identification of a valid credential:

---

<table>
  <tr>
  </tr>
  <tr>
    <td width="100%" align="center">
      <img src="docs/images/05-medusa-command-result.png" alt="Medusa attack result highlighting the discovered credential" width="100%">
    </td>
  </tr>
</table>

### 🔐 Credential Found in the Lab

---

<table width="100%">
  <tr>
    <th width="20%" align="center">&nbsp;Analyzed&nbsp;service&nbsp;</th>
    <th width="20%" align="center">&nbsp;Target&nbsp;address&nbsp;</th>
    <th width="20%" align="center">&nbsp;Username&nbsp;credential&nbsp;</th>
    <th width="20%" align="center">&nbsp;Matching&nbsp;password&nbsp;</th>
    <th width="20%" align="center">&nbsp;Final&nbsp;status&nbsp;</th>
  </tr>
  <tr>
    <td width="20%" align="center"><strong>FTP / Port 21</strong></td>
    <td width="20%" align="center"><code>192.168.56.103</code></td>
    <td width="20%" align="center"><code>msfadmin</code></td>
    <td width="20%" align="center"><code>msfadmin</code></td>
    <td width="20%" align="center"><strong>SUCCESS</strong></td>
  </tr>
</table>

> The discovered credential belongs to the vulnerable Metasploitable 2 environment and was used only for lab demonstration purposes.

---

## 🛡️ How to Mitigate This Type of Attack

Defending against dictionary attacks involves a combination of policies, technical controls, and continuous monitoring.

---

<table width="100%">
  <tr>
    <th width="8%" align="center">Icon</th>
    <th width="27%" align="center">Measure</th>
    <th width="65%" align="center">Description</th>
  </tr>
  <tr>
    <td align="center">
      <img src="https://api.iconify.design/mdi:form-textbox-password.svg?color=%236D28D9" width="32" height="32">
    </td>
    <td><strong>Strong password policy</strong></td>
    <td>Prevent common, short, or predictable passwords by requiring stronger combinations resistant to dictionary attacks.</td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://api.iconify.design/mdi:account-lock.svg?color=%23DC2626" width="32" height="32">
    </td>
    <td><strong>Temporary lockout</strong></td>
    <td>Apply account lockout or temporary delay after multiple invalid authentication attempts.</td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://api.iconify.design/mdi:speedometer-slow.svg?color=%23F59E0B" width="32" height="32">
    </td>
    <td><strong>Rate limiting</strong></td>
    <td>Reduce the speed of attempts per IP, user, or service, making large-scale automated attacks harder.</td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://api.iconify.design/mdi:two-factor-authentication.svg?color=%23059669" width="32" height="32">
    </td>
    <td><strong>MFA</strong></td>
    <td>Require multi-factor authentication when applicable, reducing the impact of a compromised password.</td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://api.iconify.design/mdi:file-search.svg?color=%230EA5E9" width="32" height="32">
    </td>
    <td><strong>Log monitoring</strong></td>
    <td>Identify repeated login attempt patterns, suspicious authentications, and access outside expected behavior.</td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://api.iconify.design/mdi:shield-alert.svg?color=%23EA580C" width="32" height="32">
    </td>
    <td><strong>Fail2ban / IDS</strong></td>
    <td>Automate blocks and alerts based on suspicious behavior, such as multiple authentication failures.</td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://api.iconify.design/mdi:server-off.svg?color=%237C3AED" width="32" height="32">
    </td>
    <td><strong>Disable unnecessary services</strong></td>
    <td>Remove or disable services that are not essential, reducing the available attack surface.</td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://api.iconify.design/mdi:lock-check.svg?color=%2316A34A" width="32" height="32">
    </td>
    <td><strong>Prefer SFTP / FTPS</strong></td>
    <td>Use more secure file transfer protocols, avoiding unnecessary exposure of legacy services.</td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://api.iconify.design/mdi:key-change.svg?color=%23BE123C" width="32" height="32">
    </td>
    <td><strong>Default credential management</strong></td>
    <td>Change or remove default usernames and passwords, especially on newly installed systems or test environments.</td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://api.iconify.design/mdi:lan.svg?color=%230F766E" width="32" height="32">
    </td>
    <td><strong>Network segmentation</strong></td>
    <td>Restrict access to the service only to trusted networks, limiting direct exposure of FTP.</td>
  </tr>
</table>

---

## ✅ Conclusion

This lab demonstrated, in a practical and controlled way, how a dictionary attack can compromise a service when weak or predictable credentials are present.

The activity reinforces the importance of defensive best practices applied in real environments, especially when authentication services are exposed on the network.

<table width="100%">
  <tr>
    <th width="8%" align="center">Visual</th>
    <th width="27%" align="center">Defensive best practice</th>
    <th width="65%" align="center">Importance for mitigation</th>
  </tr>
  <tr>
    <td align="center">
      <img src="https://api.iconify.design/mdi:form-textbox-password.svg?color=%236D28D9" width="32" height="32">
    </td>
    <td><strong>Strong passwords</strong></td>
    <td>Reduce the chance of success in attacks based on common, predictable, or reused combinations.</td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://api.iconify.design/mdi:key-remove.svg?color=%23DC2626" width="32" height="32">
    </td>
    <td><strong>Removal of default credentials</strong></td>
    <td>Prevents known usernames and passwords from being exploited on newly installed or poorly configured systems.</td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://api.iconify.design/mdi:account-lock.svg?color=%23F59E0B" width="32" height="32">
    </td>
    <td><strong>Attempt limitation</strong></td>
    <td>Makes automated tests harder by applying lockouts, delays, or restrictions after multiple authentication failures.</td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://api.iconify.design/mdi:file-search.svg?color=%230EA5E9" width="32" height="32">
    </td>
    <td><strong>Log monitoring</strong></td>
    <td>Helps identify suspicious patterns, such as repeated attempts, failed authentications, and unusual access.</td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://api.iconify.design/mdi:lan.svg?color=%230F766E" width="32" height="32">
    </td>
    <td><strong>Network segmentation</strong></td>
    <td>Restricts access to services only to trusted networks, reducing direct exposure of the environment.</td>
  </tr>
  <tr>
    <td align="center">
      <img src="https://api.iconify.design/mdi:shield-half-full.svg?color=%2316A34A" width="32" height="32">
    </td>
    <td><strong>Attack surface reduction</strong></td>
    <td>Minimizes risk by disabling unnecessary services and keeping only essential resources exposed.</td>
  </tr>
</table>

> Offensive security, when practiced ethically and with authorization, is an essential tool for strengthening real environments.

---

## 👨‍💻 Author

<div align="left">
  <img src="docs/images/avatar.png" alt="Avatar James Taylor" width="72" height="72" align="middle">
  &nbsp;&nbsp;
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=18&pause=1000&color=A78BFA&vCenter=true&multiline=false&width=660&height=72&lines=James+Taylor+%7C+%F0%9F%9B%A1%EF%B8%8F+Cybersecurity+Student,+Blue+Team+and+SOC." alt="James Taylor | Cybersecurity Student, Blue Team and SOC" align="middle">
</div>

---
