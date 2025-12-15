# 📕 CHAPTER 9

## PERSISTENCE (LONG-TERM ACCESS)

### “Getting in is good. Staying in, no matter what, is mastery.”

---

## 🧠 CHAPTER 9 KA GOAL

Red teamer yahan pe “access ko survive karna” seekhta hai — matlab:

* Password change ho jaye, MFA lag jaye, account disable ho jaye — phir bhi attacker ka control environment pe bana rahe.
* Bina noisy alerts ke, silent aur durable presence create karna.

Yeh wo phase hai jahan attacker apne footprint ko smartly hide karta hai, taaki defender usko detect ya block na kar sake.

---

## 🔴 REAL RED TEAM MINDSET

❌ “Main bas ek baar hi andar aa jaoon, fir access gaya to phir nahi milega.”
✅ “Main apna rasta aise banaata hoon ki wo bar-bar reopen ho.”
✅ “Har defense ko anticipate karo, aur uske bypass plan rakho.”

> Persistence is like planting seeds — they grow quietly, and come back when you’re needed.

---

## 🧩 PHASE 9.1 – HIDDEN ADMIN ACCOUNTS

* Create karo alternate admin accounts jinka naam normal lagta ho (example: svc_admin, backup_ops)
* Rename existing accounts for confusion (ex: Administrator -> Adm1n)
* Use karo “SID History” attribute to maintain stealthy privilege
* Accounts ko disable / enable karna, jisse suspicion kam ho

📌 Insight:

> These accounts should blend in with normal environment noise.

---

## 🧩 PHASE 9.2 – GPO BACKDOORS

* GPO ko modify karke malicious scripts push karna (Startup/Logon scripts)
* Scheduled task create karna via GPO for persistence
* PowerShell payloads silently deploy karna
* Ensure karo GPO changes ka logging minimal ho

📌 Reality:

> One GPO tweak se hundreds of machines controlled ho sakte hain.

---

## 🧩 PHASE 9.3 – KERBEROS TICKET ABUSE

* Use karo Golden Ticket attacks for unlimited domain access
* Silver Ticket for service-specific stealth access
* Pass-the-Ticket to reuse valid Kerberos tickets silently
* Rotate tickets aur monitor ticket expiration silently
* Keep tickets hidden and refresh on schedule

📌 Gold nugget:

> Kerberos persistence bina password change ke access deta hai.

---

## 🧩 PHASE 9.4 – SCHEDULED TASKS & SERVICES

* Scheduled tasks banake repetitive payloads chalana (remote commands, data exfil)
* Services hijack karke attacker code auto-run karwana
* Task names aur service descriptions normal rakhna
* Clean-up aur rotation ke liye scripts banaye rakhna

📌 Pro tip:

> Scheduled tasks quietly survive reboot aur user logout.

---

## 🧩 PHASE 9.5 – PASSWORD CHANGE RESILIENCE

* Jab bhi target account ka password change hota hai, persistence wahan se lost ho sakti hai — isliye multiple paths create karo.
* Use karo service accounts jinke passwords rarely change hote hain
* Maintain karo Kerberos tickets / hashes jo offline use ho sakte hain
* Backdoor admin accounts hamesha ready rakhna
* Continuous monitoring karo password policy changes

📌 Reality check:

> Real attackers prepare for “password apocalypse”.

---

## 🧠 REAL RED TEAMER QUESTIONS

* Kya mera persistence noisy to nahi?
* Kya defender mujhe trace kar sakta hai logs se?
* Kya mera backdoor environment reboot ke baad bhi survive karega?
* Kya multiple fallback persistence hai?
* Kya mera persistence business-as-usual lagta hai?

---

## 🧠 REPORT-GRADE NOTE

> “Attacker established multiple stealth persistence methods including hidden admin accounts, GPO backdoors, Kerberos ticket abuse, and scheduled tasks. These ensured continued access even after password changes or account disablement, making eradication difficult without full environment rebuild.”

---

## 🧠 CHAPTER 9 SUMMARY (ONE VIEW)

```
Multiple persistence methods deployed
      ↓
Hidden admin accounts created & masked
      ↓
GPO and scheduled tasks leveraged
      ↓
Kerberos ticket abuse maintained
      ↓
Prepared for password changes & detection
      ↓
Silent, durable long-term access ensured
```

---

## 🔑 ONE-LINER TRUTH (CHAPTER 9)

> **“Persistence is not just staying in — it’s surviving every defense thrown at you.”**

---


