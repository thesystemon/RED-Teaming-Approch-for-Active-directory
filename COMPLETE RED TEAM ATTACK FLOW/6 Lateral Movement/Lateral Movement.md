# 📕 CHAPTER 6

## 🔥 LATERAL MOVEMENT (The Staircase to Domain Control)

---

### ❓ Lateral Movement Kya Hai?

Ek compromised system se dusre system me hop karna, taaki higher privileges aur better access mil sake.

> **Simple:** “Main yahan hoon, ab main aur aage kaise jaaun?”

---

### 🎯 REAL LOGIC (Why Lateral Movement Matters)

**1. Low-Value PC se Start**
Sabse kam sensitive machine jahan attacker ko initial access milta hai (e.g. user’s laptop).
Yahan se direct Domain Controller (DC) pe jana risky hota hai, kyunki:

* DC highly monitored hota hai
* Direct attack suspicious hota hai
* DC par security controls zyada tight hote hain

**2. Servers ka Role**
Lateral movement me next step generally hota hai servers ka compromise:

* File servers
* Application servers
* Jump servers

**Kyun?**

* Admins frequently in servers pe login karte hain (daily use)
* Servers pe elevated permissions milna zyada common hai
* Monitoring thodi kam strict hoti hai normal servers pe (compared to DC)

**3. High-Value Servers**
Ye wo servers hote hain jinme sensitive data ya privileged accounts ki access hoti hai:

* Backup servers
* Database servers
* Identity management servers

**4. Domain Controller (DC)**
Sabse last step hota hai DC ka control lena, kyunki yeh poora domain ka king hai.
Lekin direct DC par jump bahut loud aur risky hota hai, isliye attacker **stairs use karta hai, elevator nahi**.

---

### 🧠 REAL RED TEAM MINDSET – WHY STAIRS, NOT ELEVATOR?

* **Stealth is King**
  Direct DC attack se alert trigger hone ke chances bahut high hote hain.
  Staged movement me attacker silently apne footprint ko minimize karta hai.

* **Trust Exploitation**
  Normal users aur servers ke beech ke trust relationships ko exploit karna easy hota hai.
  Ye trust chain attacker ko internally move karne me help karti hai.

* **Privilege Escalation + Lateral Movement Combo**
  Har system me attacker privilege escalate karta hai (example: local admin ban jaata hai), phir next system pe lateral move karta hai.
  Is gradual approach se detection avoid hota hai.

---

### 🧩 PHASE 6.1 – IDENTIFY LATERAL MOVEMENT VECTORS

1. **Remote Desktop Protocol (RDP)**
   Sabse common lateral movement vector, jo mostly admins aur IT use karte hain.

2. **SMB (Server Message Block)**
   File sharing ke zariye unauthorized access mil sakta hai, agar permissions weak hain.

3. **PSExec / WMI / PowerShell Remoting**
   Powerful admin tools jo remote command execution ke liye use hote hain, lateral movement ke liye ideal.

4. **Pass-the-Hash / Pass-the-Ticket**
   Credentials reuse karke bina password jaane lateral move karna.

5. **Scheduled Tasks / Services Hijacking**
   Remote services ya scheduled tasks ko manipulate karke access gain karna.

6. **Windows Management Instrumentation (WMI)**
   Query aur execute commands remotely with minimal noise.

7. **Remote Registry Access**
   Registry ke zariye configuration ya credentials access karna.

8. **Network Shares / Mapped Drives**
   Shared drives ke zariye files aur credentials ka indirect access.

9. **Printer and Other Network Devices Abuse**
   Devices jo network me hain unka misuse lateral movement ke liye.

10. **Third-party Remote Management Tools**
    TeamViewer, AnyDesk jaise tools jo network pe ho sakte hain, attacker use kar sakta hai.

---

### 🧩 PHASE 6.2 – FINDING ENTRY POINTS ON TARGET MACHINES

1. **Open Admin Shares (C$, ADMIN$)**
   Remote file system access ke liye sabse common gateway.

2. **Weak or reused credentials**
   Credentials jo already compromised hain ya easily guessable.

3. **Cached credentials on compromised machine**
   Memory ya disk pe stored credentials jinse lateral move possible ho.

4. **Misconfigured ACLs allowing access**
   Access Control Lists me galti se zyada permissions milna.

5. **Old sessions with valid tokens**
   Purani sessions jo ab bhi active hain, unka misuse.

6. **Misconfigured Remote Desktop settings**
   Nahi properly secured RDP jo lateral move facilitate karta hai.

7. **Unpatched vulnerabilities on internal systems**
   Known vulnerabilities jo patch nahi hue internal machines me.

8. **Poor network segmentation**
   Internal network me systems ka freely communicate karna, lateral move easy karna.

9. **Default or weak local admin passwords**
   Local admin accounts jo easily accessible hain.

10. **Use of common credentials across machines**
    Password reuse across multiple systems.

---

### 🧩 PHASE 6.3 – EXECUTION STRATEGY

1. **Step-by-step system hop**
   Low privilege se gradually high privilege system tak.

2. **Stabilize control on each compromised system**
   Persistence setup karna, backdoors install karna, clean logs karna.

3. **Mimic normal admin behavior**
   Activity ko legitimate lagana jaise RDP sessions, scheduled tasks.

4. **Bypass Network Segmentation**
   VLAN hopping, VPN tunneling jaise methods use karna.

5. **Avoid detection mechanisms**
   Event log tampering, stealthy tools use karna.

6. **Credential harvesting at each step**
   Mimikatz ya similar tools se tokens aur hashes collect karna.

7. **Use trusted tools (‘Living off the Land’)**
   Windows ke apne tools se attack execute karna taaki suspicion na aaye.

8. **Credential reuse / Pass-the-Hash / Pass-the-Ticket**
   Jo credentials mile unka use karna next hop ke liye.

9. **Clean up after every step**
   Logs modify karna ya delete karna taaki trace kam pade.

10. **Continual recon at each compromised node**
    Har system ka detailed enumeration taaki agla target select kar sake.

---

### 🔥 GOLDEN RULE OF LATERAL MOVEMENT

> **“Attackers use stairs, not elevators.”**
> Matlab, attacker har step pe apne traces ko kam karta hai, controlled tarike se aage badhta hai, bina suspicious activity trigger kiye.

---

### 🧠 REAL WORLD EXAMPLE

* Attacker ko initial access mila ek junior employee ke laptop pe
* Laptop pe local admin rights mile
* Usne nearby file server ko RDP kiya, jahan usne apni permissions badhai
* File server se backup server pe lateral move kiya, wahan se domain admin credentials capture kiye
* Phir DC pe gaya, domain poora compromise kar liya

---

### 🧠 CHAPTER 6 SUMMARY

Lateral movement me focus hai:

* **Silent hop** karna low-value se high-value targets tak
* Har system me apna control **stabilize** karna
* **Admin workflows aur trust** ko exploit karna
* Detection avoid karna with **normal behavior mimicry**
* **Gradual, step-wise approach**

---


