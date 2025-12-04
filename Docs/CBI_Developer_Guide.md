# CBI Developer Guide  
### Version 1.0 — December 2025

A unified reference guide for working on the CBI AutoCAD plugin ecosystem.

---

## 1. CORE PRINCIPLES

1. **Architectural snapshots drive all AI-assisted debugging.**  
2. **Every tool obeys Scope Guard.**  
3. **All changes must be logged in changelogs.**  
4. **AutoCAD locking rules are non-negotiable.**  
5. **Thread Starter Template is required for every new ChatGPT session.**

---

## 2. DIRECTORY STRUCTURE OVERVIEW

AutoCAD/ ├─ AutoCAD2020/ │   ├─ Commands.cs │   ├─ PropertiesHub/ │   ├─ ProjectStore/ │   ├─ Tagging/ │   ├─ ValveInsert/ │   ├─ Sheet_Set_Manager/ │   └─ Shared + Interop ├─ AutoCAD_Shared_Project/ │   └─ helper libraries ├─ CBI_Tools_ChangeLog.md └─ Changelogs/

---

## 3. TOOL ARCHITECTURE

Each tool has:

- A namespace root (`AutoCAD2020.<Tool>`)  
- Command entry points (`Commands.cs`)  
- Supporting classes in its folder  
- Cross-tool helpers in the Shared project  
- JSON architectural snapshots  
- A per-tool changelog  

---

## 4. WORKFLOW WITH CHATGPT

### Step 1 — Create a new debugging thread  
Paste the **Thread Starter Template**

### Step 2 — ChatGPT performs analysis  
No code is generated yet.

### Step 3 — Approve the scope  
Reply with:

Approved. Proceed with proposed changes.

### Step 4 — Apply patches  
Copy edits into Visual Studio and test in AutoCAD.

### Step 5 — Log changes  
Update both master changelog and tool changelog.

---

## 5. REGENERATING ARCHITECTURE SNAPSHOTS

Run:

CBI.ArchMap.exe

Use when:

- New classes added  
- Namespaces changed  
- Commands added  
- Major refactor occurred  

Then commit and push.

---

## 6. SUPPORTING DOCUMENTS

See also:

- CBI Architectural Debugging SOP  
- CBI Crash Report SOP  
- CBI Thread Starter Template  
- CBI Changelog SOP  

---

## 7. REVISION HISTORY

| Version | Date | Author | Notes |
|--------|-------|---------|-------|
| 1.0 | 2025-12-03 | ChatGPT (for Brian) | Initial release |
