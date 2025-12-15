# 📕 CHAPTER 2 – INITIAL ACCESS

## 🚪 COMPLETE RED TEAM CHECKLIST (DEEP)

---

## 🧠 1. INITIAL ACCESS OBJECTIVE DEFINITION

☐ Clearly define **why access is needed** (visibility, pivot, trust)
☐ Confirm **minimum required privilege** for next phases
☐ Define **acceptable detection risk level**
☐ Confirm **rules of engagement alignment**
☐ Decide whether access must be:

* Short-term
* Long-term
* Disposable
* Persistent

📌 *Red team mindset:*

> “I don’t need power — I need position.”

---

## 👤 2. INITIAL IDENTITY SELECTION (MOST CRITICAL)

☐ Identify business-relevant user roles
☐ Prioritize users with **high interaction & trust**
☐ Evaluate user’s proximity to IT / Admin teams
☐ Confirm user fits **normal daily workflows**
☐ Ensure identity choice supports **lateral movement potential**

### Identity Priority Logic:

☐ IT Support
☐ Infrastructure / Ops
☐ HR
☐ Finance
☐ Remote Employees
☐ Contractors / Vendors

📌 *Golden Rule:*

> The best initial user is the one nobody questions.

---

## 🧩 3. ACCESS PATH JUSTIFICATION

☐ Document **why this access path is realistic**
☐ Confirm access method aligns with company culture
☐ Validate access method is **commonly used internally**
☐ Avoid rare or exotic access paths
☐ Ensure access looks **routine in logs**

📌 *Red team question:*

> “Would SOC ignore this if they saw it once?”

---

## 🔐 4. AUTHENTICATION & TRUST MODEL ANALYSIS

☐ Identify authentication type (password-based, hybrid, SSO)
☐ Assess presence or absence of MFA
☐ Evaluate password hygiene assumptions
☐ Identify trusted authentication sources (VPN, IdP, SaaS)
☐ Determine how often users authenticate daily

📌 *Reality:*

> Trust is enforced by habit, not policy.

---

## 🕒 5. TIMING & BEHAVIOR MODELING

☐ Select realistic login time windows
☐ Align access timing with business hours
☐ Avoid abnormal access frequency
☐ Mimic standard user session duration
☐ Ensure no burst or erratic behavior

📌 *SOC detects behavior, not intent.*

---

## 🌍 6. LOCATION & CONTEXT BELIEVABILITY

☐ Ensure geographic access makes sense
☐ Align access with known employee locations
☐ Avoid sudden impossible travel patterns
☐ Maintain consistency across sessions
☐ Match device & network expectations

📌 *Red team rule:*

> One wrong context can expose everything.

---

## 🧪 7. INITIAL ACCESS VALIDATION (POST-ENTRY)

☐ Confirm credentials/session stability
☐ Validate repeatable access
☐ Identify session expiration behavior
☐ Check for forced resets or alerts
☐ Confirm account is not flagged or restricted

📌 *Access without stability is useless.*

---

## 🧠 8. ACCESS RISK EVALUATION

☐ Estimate likelihood of SOC review
☐ Identify logging depth for this identity
☐ Assess whether user is high-visibility
☐ Evaluate anomaly risk
☐ Decide whether to continue or pivot

📌 *Professional red teamers abandon access early if needed.*

---

## 🧩 9. ACCESS CLASSIFICATION & LABELING

☐ Classify access type:

* External SaaS only
* VPN access
* Internal domain user
* Privileged user
* Hybrid cloud/on-prem

☐ Assign confidence level to access
☐ Document limitations clearly
☐ Note segmentation boundaries
☐ Identify reachable internal zones

📌 *This classification drives all next phases.*

---

## 🛑 10. OPSEC & DETECTION SAFETY CHECK

☐ No repeated authentication failures
☐ No abnormal request patterns
☐ No privilege abuse at this stage
☐ No system interaction beyond necessity
☐ No deviation from user’s normal role

📌 *Initial access phase is NOT enumeration.*

---

## 🔄 11. BACKUP & CONTINGENCY PLANNING

☐ Identify backup access hypothesis
☐ Prepare fallback identity
☐ Define clean exit strategy
☐ Ensure no dependency on single session
☐ Document recovery assumptions

📌 *Good red teamers plan for loss.*

---

## 🧭 12. TRANSITION READINESS TO FOOTHOLD PHASE

☐ Access documented clearly
☐ Identity risk profile completed
☐ Detection likelihood assessed
☐ Next phase objectives aligned
☐ Engagement still stealth-compliant

📌 *Initial Access ends when planning begins.*

---

## 📝 13. REPORTING & EVIDENCE NOTES

☐ Document access narrative (business-aligned)
☐ Avoid technical jargon in summary
☐ Highlight root cause, not technique
☐ Map access to real business risk
☐ Provide defensive recommendations later

📌 *Reports convince leadership, not hackers.*

---

# 🧠 CHAPTER 2 FINAL SUMMARY CHECKLIST

☐ Right identity selected
☐ Access path justified
☐ Behavior matched real users
☐ Access validated & stable
☐ Detection risk acceptable
☐ Ready for Foothold & Stability phase

---

## 🔑 ONE-LINE TRUTH (CHAPTER 2)

> **Initial Access is successful only when defenders believe you belong there.**

---


