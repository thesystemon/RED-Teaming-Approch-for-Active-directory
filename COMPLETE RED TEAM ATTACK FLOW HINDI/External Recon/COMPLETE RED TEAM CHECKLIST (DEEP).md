# 📕 CHAPTER 1 – EXTERNAL RECONNAISSANCE

## 🔍 COMPLETE RED TEAM CHECKLIST (DEEP)

---

## 🧠 1. RECON OBJECTIVE DEFINITION

☐ Clearly define **engagement goal** (e.g., Domain compromise, data access)
☐ Understand **rules of engagement** (what is allowed / not allowed)
☐ Identify **stealth requirements** (low-noise vs assumed breach)
☐ Define **success criteria** from a red team perspective
☐ Establish **initial access assumptions** (user-level vs system-level)

📌 *Red team thinking:*

> “What does success look like before I touch anything?”

---

## 🏢 2. ORGANIZATION PROFILING

☐ Identify company name, brand names, subsidiaries
☐ Identify industry sector (finance, healthcare, tech, etc.)
☐ Estimate company size (small / mid / enterprise)
☐ Identify geographic locations (HQ, branches, remote workforce)
☐ Understand business operations (24x7, shift-based, seasonal peaks)

📌 *Why this matters:*
Business context decides **attack timing** and **human behavior**

---

## 👥 3. PEOPLE & IDENTITY MAPPING (CRITICAL)

☐ Enumerate employee names from public sources
☐ Identify **departments** (HR, IT, Finance, Legal, DevOps)
☐ Identify **high-value roles**:

* IT Support
* System Administrators
* Network Engineers
* Domain / Infrastructure teams

☐ Identify **decision makers** and **authority figures**
☐ Identify contractors / third-party employees
☐ Identify recently hired employees (higher risk)

📌 *Red team priority:*

> IT Support and HR are more valuable than CEOs

---

## 📧 4. EMAIL & IDENTITY STRUCTURE DISCOVERY

☐ Determine corporate email format
☐ Validate consistency of naming conventions
☐ Identify shared mailboxes or role-based emails
☐ Check for exposed email addresses on public platforms
☐ Assess predictability of usernames

📌 *Impact:*
Predictable identities enable **targeted and believable access paths**

---

## 🧑‍💻 5. TECHNOLOGY STACK INFERENCE (PASSIVE)

☐ Identify use of Active Directory (job descriptions, documentation)
☐ Identify VPN usage references
☐ Identify cloud services (O365, Google Workspace, Azure, AWS)
☐ Identify endpoint OS assumptions (Windows/macOS/Linux)
☐ Identify remote access patterns (WFH, BYOD)

📌 *Red team goal:*

> “What technology am I likely to encounter once inside?”

---

## 🌐 6. EXTERNAL ATTACK SURFACE VISIBILITY

☐ Identify externally accessible portals (login pages, VPN gateways)
☐ Identify password reset or authentication portals
☐ Identify third-party services integrated with company identity
☐ Identify exposed APIs or portals referenced publicly
☐ Identify legacy or region-specific portals

⚠️ *Important:*
This is **visibility**, not exploitation

---

## 🧠 7. HUMAN BEHAVIOR & PSYCHOLOGY ANALYSIS

☐ Observe employee social media behavior
☐ Identify stress indicators (deadlines, hiring, audits, migrations)
☐ Identify authority trust patterns (managers, HR, IT notices)
☐ Identify routine events (salary cycles, reviews, onboarding)
☐ Identify language tone used internally (formal/informal)

📌 *Key insight:*

> Attacks succeed when they feel **normal**

---

## 🔐 8. IDENTITY HYGIENE ASSESSMENT (PASSIVE)

☐ Look for signs of password reuse culture
☐ Identify mentions of legacy systems
☐ Identify absence of MFA references
☐ Identify long-tenured employees (less password rotation)
☐ Identify third-party credential dependencies

📌 *Red team focus:*
Identity weakness > network weakness

---

## 🔄 9. THIRD-PARTY & SUPPLY CHAIN AWARENESS

☐ Identify vendors and partners
☐ Identify outsourced IT or support services
☐ Identify shared platforms or integrations
☐ Identify trust relationships publicly disclosed
☐ Identify weakest external trust dependency

📌 *Reality:*
Many breaches start **outside** the main organization

---

## 🧩 10. INITIAL ACCESS HYPOTHESIS CREATION

☐ List all plausible initial access vectors
☐ Rank vectors by:

* Stealth
* Believability
* Business realism
* Impact potential

☐ Select **primary** and **backup** access hypotheses
☐ Define assumptions for each hypothesis
☐ Document expected privileges from each access type

📌 *Example hypothesis:*

> “A compromised IT support user is likely to provide lateral movement opportunities across multiple systems.”

---

## 🗺️ 11. ATTACK PATH PRE-MAPPING

☐ Predict internal access level after initial entry
☐ Predict likely lateral movement candidates
☐ Identify potential privilege escalation choke points
☐ Predict where admins are likely to log in
☐ Identify potential high-value systems early

📌 *This is not execution — this is strategy.*

---

## 📝 12. RECON DOCUMENTATION & REPORTING

☐ Document all assumptions clearly
☐ Separate facts from hypotheses
☐ Note confidence levels for each finding
☐ Prepare recon summary for red team lead
☐ Maintain audit trail for engagement transparency

📌 *Professional red teamers document everything.*

---

## 🚨 13. OPERATIONAL SECURITY CHECK

☐ Confirm no active interaction occurred
☐ Confirm no alerts were triggered
☐ Confirm no target awareness indicators
☐ Validate recon remains legally compliant
☐ Ensure readiness for next phase

---

# 🧠 CHAPTER 1 FINAL SUMMARY CHECKLIST

☐ Organization understood
☐ People mapped
☐ Trust relationships identified
☐ Likely initial access paths defined
☐ Attack hypotheses documented
☐ Ready for Initial Access phase

---

## 🔑 CHAPTER 1 ONE-LINE TRUTH

> **External reconnaissance determines the entire success or failure of a red team operation.**

---


