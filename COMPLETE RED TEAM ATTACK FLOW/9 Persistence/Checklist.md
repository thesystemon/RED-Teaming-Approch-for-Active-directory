# 📕 CHAPTER 9 – PERSISTENCE (LONG-TERM ACCESS)

## 🧠 DEEP PROFESSIONAL RED TEAM CHECKLIST

---

### 1. MULTIPLE PERSISTENCE VECTORS

☐ Create diverse persistence paths to avoid single point of failure
☐ Avoid reliance on just one method (e.g., only hidden accounts or only scheduled tasks)

---

### 2. HIDDEN ADMIN ACCOUNT CREATION & MANAGEMENT

☐ Create admin accounts with legitimate-sounding names
☐ Rename or clone existing admin accounts to avoid detection
☐ Regularly check account status and disable/enable to mimic normal activity
☐ Use SID History or group memberships to mask privileges

---

### 3. GPO-BASED PERSISTENCE

☐ Deploy startup/logon scripts via GPOs for widespread persistence
☐ Modify GPOs silently and keep change logging minimal
☐ Use scheduled tasks and service creation via GPO to maintain control
☐ Monitor GPO replication timing to avoid premature detection

---

### 4. KERBEROS TICKET ABUSE FOR PERSISTENCE

☐ Deploy Golden Tickets for unlimited domain access without password knowledge
☐ Use Silver Tickets for specific service persistence
☐ Renew and rotate tickets to avoid expiry and suspicion
☐ Store tickets stealthily and prevent credential dumping alerts

---

### 5. SCHEDULED TASK & SERVICE HIJACKING

☐ Create scheduled tasks with plausible names and low execution frequency
☐ Hijack legitimate services to run attacker code at startup
☐ Avoid overlapping tasks that may cause anomalies in logs
☐ Ensure persistence survives system reboot and user logoff

---

### 6. PASSWORD CHANGE & POLICY RESILIENCE

☐ Establish persistence that survives password resets (e.g., Golden Tickets, backdoor accounts)
☐ Use service accounts with rarely changed passwords for persistence
☐ Monitor password policy changes and adapt accordingly
☐ Prepare fallback persistence mechanisms for account lockouts or disables

---

### 7. STEALTH & LOG CLEANING STRATEGY

☐ Avoid generating noisy logs when creating or using persistence
☐ Employ log cleaning or tampering techniques cautiously
☐ Mimic legitimate user or admin activity patterns during persistence actions
☐ Maintain low frequency of persistence triggers to reduce suspicion

---

### 8. PERSISTENCE ROTATION & MAINTENANCE

☐ Schedule periodic checks and rotate persistence artifacts
☐ Remove or replace old persistence to avoid detection
☐ Automate cleanup and recreation where possible
☐ Test persistence effectiveness regularly

---

### 9. PERSISTENCE CAMOUFLAGE

☐ Use legitimate-sounding account names and service descriptions
☐ Blend scheduled tasks and services within normal operational hours
☐ Avoid unusual command-line arguments or script locations
☐ Use environment variables and standard folders for payload storage

---

### 10. PREPARE FOR ENVIRONMENT RECOVERY SCENARIOS

☐ Plan persistence that survives common incident response actions
☐ Build redundancy to withstand account disablement or password resets
☐ Document fallback entry points mentally (not physically)
☐ Anticipate potential defender tools and bypass strategies

---

## 🔑 ONE-LINE TRUTH (PERSISTENCE)

> **“Long-term access demands silent, diverse, and adaptive footholds that outlive defenses.”**

---


