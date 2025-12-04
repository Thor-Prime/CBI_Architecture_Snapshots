# CBI Crash Report SOP  
### Version 1.0 — December 2025

This SOP defines how to report AutoCAD crashes or exceptions during development, ensuring ChatGPT receives complete and actionable diagnostic data.

---

## 1. PURPOSE
To provide a consistent crash-reporting format so debugging sessions remain fast, predictable, and safe.

This SOP applies to all CBI tools:

- Properties Palette  
- Valve Insert  
- Tag Manager  
- Sheet Set Manager  
- ProjectStore  
- Batch Update Tool  
- Any new tools added later  

---

## 2. WHEN TO USE
Use this SOP anytime:

- AutoCAD throws an exception  
- A tool stops mid-execution  
- An eLockViolation appears  
- Commands behave unexpectedly  
- Data fails validation  
- UI elements vanish or mis-bind  

---

## 3. CRASH REPORT TEMPLATE

Copy/paste the following whenever reporting a crash:

---

### 🔥 **CBI Crash Report Template**

**Active Tool:** `<Tool name>`  
**Command Used:** `<Command used at time of crash>`  

**What I was doing:**  
(1–3 sentences describing the action immediately before the crash)

**Crash / Exception Message (first lines only):**

<copy from AutoCAD / Visual Studio / MessageBox>

**Stack Trace (top 5–10 lines):**

<paste here>
```Reproducibility:

Does it happen every time? (Yes/No)

Does it occur on other drawings?

Does it occur after restarting AutoCAD?


Drawing Context:

Model space or paper space?

Block selected?

Same drawing opened multiple times?


Additional Notes:
(Anything unusual or relevant)


---

4. CHATGPT RESPONSE EXPECTATION

ChatGPT will:

1. Analyze the stack trace


2. Map it to architectural JSON


3. Identify the probable failure location


4. Check scope boundaries


5. Propose a safe fix




---

5. REVISION HISTORY

Version	Date	Author	Notes

1.0	2025-12-03	ChatGPT (for Brian)	Initial release
