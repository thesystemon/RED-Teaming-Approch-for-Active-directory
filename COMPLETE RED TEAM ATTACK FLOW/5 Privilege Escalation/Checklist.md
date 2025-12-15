# ✅ CHAPTER 5 – PRIVILEGE ESCALATION

## 🔥 DEEP RED TEAM CHECKLIST

---

## 🧠 1. PRIVILEGE CONTEXT UNDERSTANDING

☐ Current access level clearly identified
☐ User kis tier me hai (User / Workstation / Server / Admin)
☐ Privilege temporary hai ya persistent?
☐ Ye access business-role ke hisaab se normal lagta hai?
☐ Defender ke liye suspicious to nahi dikhega?

📌 **Red team thought:**

> “Main kaha khada hoon aur meri reach kitni hai?”

---

## 🧩 2. DELEGATED PERMISSIONS ANALYSIS (MOST ABUSED)

☐ User / Group ke delegated rights mapped
☐ Kis object pe write / modify control hai
☐ Group membership modify kar sakta hai ya nahi
☐ Service account properties modify ho sakti hain?
☐ GPO pe partial ya full control available hai?

📌 **Red team thought:**

> “Password nahi chahiye, control chahiye.”

---

## 🧩 3. SERVICE ACCOUNT EXPOSURE REVIEW

☐ Environment me service accounts identified
☐ Service account ka purpose understood
☐ Password rotation policy weak hai ya absent
☐ Service account ke rights mapped
☐ Kya service account high-value system pe run ho raha hai?

📌 **Real insight:**

> Service accounts = admin power + no human attention

---

## 🧩 4. LOCAL ADMIN POTENTIAL

☐ Current user local admin hai kisi system pe
☐ Kis machines pe local admin rights hain
☐ Ye machines kis users dwara use hoti hain
☐ Kya koi admin in machines pe login karta hai
☐ Ye system business-critical hai ya not?

📌 **Red team logic:**

> Local admin = stepping stone, not final goal

---

## 🧩 5. ADMIN SESSION PROXIMITY CHECK

☐ Active admin sessions identified
☐ Kaun admin kis system pe regularly login karta hai
☐ Kya admin daily-use machine pe login karta hai
☐ Kya admin aur compromised system same zone me hain
☐ Kya admin ke habits predictable hain?

📌 **GOLD RULE:**

> Admin ke paas jaana hai, DC ke paas nahi

---

## 🧩 6. GROUP POLICY INFLUENCE

☐ GPO hierarchy understood
☐ Kya user / group GPO modify kar sakta hai
☐ Kya GPO important systems pe linked hai
☐ Kya legacy / unused GPO present hai
☐ Kya GPO change defenders ko immediately dikhega?

📌 **Insight:**

> Ek GPO = hundreds of machines

---

## 🧩 7. TIER SEPARATION FAILURE CHECK

☐ Tier 0 / Tier 1 / Tier 2 separation properly followed?
☐ Admin accounts kaha login karte hain
☐ Kya same credentials multiple zones me use hote hain
☐ Kya admin workstation hardened hai?
☐ Kya admin policies paper pe hi hain?

📌 **Reality:**

> Jahan tier mix hota hai, wahi breach hota hai

---

## 🧩 8. STEALTH & TIMING EVALUATION

☐ Escalation slow & incremental hai
☐ Ek time pe ek hi move planned
☐ Defender activity observe ki ja rahi hai
☐ Alerts / logs ka impact evaluate hua
☐ Weekend / off-hours consideration ki gayi?

📌 **Elite mindset:**

> Noise = failure

---

## 🧩 9. PRIVILEGE VALIDATION (WITHOUT ABUSE)

☐ Gained privilege logically validated
☐ Actual destructive action avoid kiya
☐ Stability check performed
☐ Reversibility considered
☐ Defender visibility risk assessed

📌 **Professional rule:**

> Power test karna ≠ power use karna

---

## 🧩 10. ESCALATION DECISION POINT

☐ Domain Admin really required?
☐ Lateral movement better option hai?
☐ Objective already achieved?
☐ Risk vs reward evaluated
☐ Stop / continue decision documented

📌 **Senior red team thinking:**

> “Just because I can, doesn’t mean I should.”

---

## 🧠 FINAL RED TEAM SELF-CHECK

☐ Koi password brute-force nahi kiya
☐ Koi exploit spam nahi kiya
☐ Koi suspicious admin action nahi dikhaya
☐ Escalation business-context me fit hoti hai
☐ Findings clearly reportable hain

---

## 📝 REPORT-STYLE STATEMENT (READY TO USE)

> “Privilege escalation was achieved through analysis of delegated permissions, service account exposure, and administrative access proximity, allowing controlled elevation without exploiting software vulnerabilities or generating anomalous security events.”

---

## 🔑 ONE-LINE TRUTH (CHAPTER 5 CHECKLIST)

> **Privilege escalation is about understanding control flow, not breaking systems.**

---
---

----
---

# CHECKLIST PART 2

# 🔥 CHECKLIST

## ❓ HOW A NORMAL USER BECOMES POWERFUL (REAL-WORLD AD LOGIC)

---

## 🧠 A. USER CONTEXT VALIDATION (START POINT)

☐ User normal domain user hai (non-admin)
☐ User daily operational workflow ka hissa hai
☐ User frequently internal resources access karta hai
☐ User IT / infra teams ke contact me aata hai
☐ User ka system shared / common usage me aata hai

📌 **Goal:**

> “Ye user business ke liye kitna trusted hai?”

---

## 🔐 B. SERVICE ACCOUNT EXPOSURE CHECK

☐ Kya service accounts exist karte hain?
☐ Kya service account ka password long time se change nahi hua?
☐ Kya service account multiple systems pe use hota hai?
☐ Kya service account privileged groups ka member hai?
☐ Kya service account monitoring / alerting me covered nahi hai?

📌 **Red Team Insight:**

> Service accounts = privilege without ownership

---

## 🧩 C. IT SUPPORT & OPERATIONAL TRUST CHECK

☐ IT Support users identify hue
☐ IT Support ke paas local admin rights widely distributed hain
☐ IT Support frequently user machines pe login karta hai
☐ IT Support credentials multiple machines pe exposed hote hain
☐ IT Support role highly trusted hai (low suspicion)

📌 **Reality:**

> IT Support = lateral movement bridge

---

## 💻 D. ADMIN LOGIN BEHAVIOR CHECK

☐ Kya admins DC ke alawa bhi login karte hain?
☐ Kya admins file servers / app servers use karte hain?
☐ Kya admins normal user machines pe troubleshooting karte hain?
☐ Kya jump server policy strictly follow hoti hai?
☐ Kya admin sessions monitored hote hain?

💥 **GOLD CONDITION:**
☐ Domain Admin logged into non-hardened machine

---

## 🧠 E. CACHED CREDENTIAL RISK CHECK

☐ Kya admin kisi normal PC pe login hua tha?
☐ Kya shared systems use ho rahe hain?
☐ Kya credential hygiene enforced nahi hai?
☐ Kya admin logout discipline weak hai?
☐ Kya EDR memory-level visibility weak hai?

📌 **Silent Risk:**

> No password cracking required

---

## 🔑 F. GROUP & ROLE RELATIONSHIP CHECK

☐ User kis-kis group ka member hai
☐ Groups nested hain ya directly assigned
☐ Kya group kisi privileged role se indirectly linked hai
☐ Kya group IT / server / backup related hai
☐ Kya group rarely reviewed hota hai

📌 **Truth:**

> Groups hide power better than accounts

---

## 🧷 G. PERMISSION / ACL MISCONFIGURATION CHECK

☐ User ke paas group modify rights hain
☐ User ke paas GPO edit / link permissions hain
☐ User ke paas OU level delegated control hai
☐ Permissions inherited hain (not explicit)
☐ Permissions documented nahi hain

💥 **CRITICAL:**
☐ Privilege escalation possible **without password compromise**

---

## 🔄 H. TRUST & ASSUMPTION CHECK

☐ Internal users trusted by default
☐ MFA internal operations pe relaxed hai
☐ Logging focused on external threats only
☐ Internal abuse scenarios considered nahi hote
☐ “Known user = safe user” mindset

📌 **Red Team Rule:**

> Trust is the biggest vulnerability

---

## 🧠 I. ATTACKER DECISION CHECKPOINT

☐ Admin password directly attack karna risky hai
☐ Admin workflow predictable hai
☐ Permissions path zyada silent hai
☐ Operational behavior exploit natural lagega
☐ Detection probability low hai

📌 **Decision:**

> Target behavior, not credentials

---

## 🏁 J. FINAL POWER TRANSITION CONFIRMATION

☐ Normal user now controls privileged function
☐ Privilege escalation happened without alert
☐ No brute force / exploit noise generated
☐ Access appears legitimate
☐ Organization ke liye impact high hai

🔥 **RESULT:**

> Normal User → Effective Domain Control Path

---

## 📝 REAL RED TEAM REPORT LINE (EXAMPLE)

> “A standard domain user was able to escalate privileges through inherited permissions, service account exposure, and administrative login behavior, without requiring direct credential compromise of privileged accounts.”

---

## 🔑 ONE-LINE FINAL TRUTH

> **In Active Directory, the fastest way to power is not breaking security — it’s following normal operations.**

---



