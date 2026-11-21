# 🔐 Cryptographic Hash Extraction & Password Cracking

**Offensive security assessment involving hash isolation, dictionary-based password cracking, and AI-assisted workflows in a Kali Linux environment**

![Skill](https://img.shields.io/badge/Skill-Cybersecurity-404040?style=flat-square&labelColor=C00000) ![OS](https://img.shields.io/badge/Guest%20OS-Kali%20Linux-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white) ![Tool](https://img.shields.io/badge/Tool-pdf2john-0070C0?style=flat-square&labelColor=000000) ![Tool](https://img.shields.io/badge/Tool-John%20the%20Ripper-238F89?style=flat-square&labelColor=000000) ![Wordlist](https://img.shields.io/badge/Wordlist-rockyou.txt-C00000?style=flat-square&labelColor=000000) ![AI](https://img.shields.io/badge/AI-HexStrike%20MCP-404040?style=flat-square&labelColor=0070C0) ![Penetration Testing](https://img.shields.io/badge/Penetration%20Testing-C00000?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white) ![GitHub](https://img.shields.io/badge/GitHub-404040?style=flat-square&labelColor=0070C0&logo=github&logoColor=white) ![NetworkWalks](https://img.shields.io/badge/NetworkWalks-404040?style=flat-square&labelColor=C00000) ![Ethical Hacking](https://img.shields.io/badge/Ethical%20Hacking-E87500?style=flat-square&labelColor=000000) ![Author](https://img.shields.io/badge/Mubassir-C00000?style=flat-square)

---

## 📌 Project Overview

This is my **Week 3** submission for the Networkwalks Cybersecurity & Ethical Hacking Internship.

This week's focus was on **offensive security assessments**: isolating cryptographic hashes from a protected target file, running dictionary-based password-cracking attacks against those hashes, and documenting the methodology plus defensive remediation steps.

> **Note:** All work was carried out against lab-provided target files inside an isolated Kali Linux environment as part of the Networkwalks training program.

---

## 🎯 Objectives

- Analyze an encrypted/password-protected target file.
- Extract crackable password hashes using `pdf2john`.
- Run wordlist-driven cracking attacks with John the Ripper (`rockyou.txt`).
- Explore AI-assisted security workflows via a HexStrike AI MCP server.
- Capture and verify milestone flags.
- Document the methodology and defensive remediation steps.

---

## 🛡️ Purpose of the Exercise

This exercise builds practical skill in:

- Offline hash extraction from protected documents
- Dictionary-based password auditing
- Understanding how weak password policies expose protected files
- Integrating AI-assisted tooling into a security workflow
- Recording evidence and findings in a reproducible way

⚠️ **Important:** These techniques were applied only to lab-provided target files inside an authorized training environment. Never use these tools against real, unauthorized targets.

---

## 🏗️ Workflow Architecture

```
   Target File (hash3.networkwalks_flag1.pdf)
                |
         pdf2john (hash extraction)
                |
         extracted_hash.txt
                |
   John the Ripper + rockyou.txt (cracking)
                |
         Recovered Password
                |
      Flag Verification & Documentation
```

More advanced cracking modes and custom wordlists can be layered onto this same workflow in future exercises.

---

## ⚙️ Lab Configuration

| 🧩 Component | ⚙️ Configuration |
|---|---|
| 🐉 Guest OS | Kali Linux |
| 🎯 Target File | `hash3.networkwalks_flag1.pdf` |
| 🔧 Hash Extraction Tool | `pdf2john` |
| 🛠️ Cracking Tool | John the Ripper |
| 📖 Wordlist | `rockyou.txt` |
| 🤖 AI Integration | HexStrike AI MCP server |

---

# 🪜 Procedure

## Step 1. Cryptographic Hash Isolation

The encrypted target file (`hash3.networkwalks_flag1.pdf`) was analyzed and its password hash extracted using `pdf2john`, preparing it for offline auditing:

```bash
pdf2john hash3.networkwalks_flag1.pdf > extracted_hash.txt
```

## Step 2. Dictionary-Based Password Auditing

A wordlist-driven cracking attack was configured and run against the extracted hash using John the Ripper with the `rockyou.txt` wordlist:

```bash
john --wordlist=/usr/share/wordlists/rockyou.txt extracted_hash.txt
john --show extracted_hash.txt
```

This demonstrated how weak password policies can leave protected documents exposed to offline attacks.

## Step 3. AI-Assisted Security Workflows

Local offensive security utilities were integrated with a **HexStrike AI** MCP server environment to streamline reconnaissance, vulnerability checks, and lab execution pipelines.

## Step 4. Flag Verification & Documentation

All target milestone flags were captured and verified, and the methodology plus defensive remediation steps were documented:

- `nw{cybersecurity_flag_captured_2608}`
- `nw{networkwalks_flag_260821_1}`
- `nw{networkwalks_flag1_jtr_270521_1}`
- `nw{networkwalks_persistence_jtr_270521}`

---

# 🔎 Verification

| ✅ Test | 🧾 Command / Action | 🎯 Result |
|---|---|---|
| 🔑 Hash extraction | `pdf2john hash3.networkwalks_flag1.pdf` | Hash successfully extracted |
| 🧩 Password recovery | `john --wordlist=rockyou.txt extracted_hash.txt` | Password cracked |
| 🏁 Flag capture | Verified against lab portal | All 4 flags confirmed |
| 📝 Documentation | Methodology + remediation write-up | Completed |

---

# 💡 What I Learned

### 1. Offline hash extraction
I learned how tools like `pdf2john` convert protected file formats into a hash format suitable for offline cracking tools.

### 2. Dictionary attacks
I practiced configuring John the Ripper with a real-world wordlist (`rockyou.txt`) and saw firsthand how predictable passwords fall quickly to dictionary attacks.

### 3. Password policy impact
This exercise reinforced why strong, unique passwords matter — weak ones can be recovered offline in minutes.

### 4. AI-assisted tooling
Integrating a HexStrike AI MCP server showed how AI can help streamline reconnaissance and lab execution pipelines.

### 5. Documentation discipline
Capturing commands, flags, and remediation notes is as important as the technical attack itself in professional security work.

---

# 🔐 Security & Ethical Use

This work was performed only against lab-provided target files inside an authorized training environment as part of the Networkwalks internship. I will only test systems and files that I own or have explicit written permission to test.

---

# 🔗 Tools & Resources

- **John the Ripper:** https://www.openwall.com/john/
- **pdf2john:** bundled with John the Ripper (jumbo) community tools
- **rockyou.txt wordlist:** included in Kali Linux wordlists
- **Kali Linux:** https://kali.org/get-kali

---

# 👤 Author

**Mubassir**
Cybersecurity Intern, Networkwalks
Instructor: Waqas Karim CCIE

---

## 📌 Project Information

**Program Name:** Cybersecurity & Ethical Hacking at Networkwalks | **Week:** 03 | **Project:** Cryptographic Hash Extraction & Password Cracking | **Repository:** GitHub
