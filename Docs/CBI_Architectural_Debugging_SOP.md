📄 CBI_Architectural_Debugging_SOP.md

# CBI Architectural Debugging SOP  
### Version 1.0 — December 2025  
*(For use with ChatGPT + CBI Architectural Snapshots)*

---

## 1. PURPOSE
This SOP defines the workflow for safely modifying or debugging any AutoCAD tool within the CBI solution using ChatGPT, **without breaking unrelated tools**.  
It ensures:

- Proper scoping  
- Accurate architectural context  
- Safe and minimal code editing  
- High repeatability  
- Clear historical traceability via changelogs

---

## 2. WHEN TO USE
Use this SOP **every time** you start a new debugging or development thread that involves:

- Fixing a broken tool  
- Adding a feature  
- Modifying palettes or UI  
- Adjusting NOD / XData logic  
- Working with validation or ProjectStore  
- Updating entity-processing logic  
- Any AutoCAD 2020 plug-in logic

---

## 3. REQUIRED ARTIFACTS

### 3.1 Architectural Snapshots (Public)
Stored in the repository:

https://github.com/Thor-Prime/CBI_Architecture_Snapshots/tree/main

Every tool uses two files:

- `ToolIndex.<Tool>.json` — tool root, class membership  
- `ClassGraph.<Tool>.json` — relationships between classes  

These give ChatGPT structural awareness.

---

### 3.2 Actual Code (Private)
Paste the **exact** file, class, or method you're working with.  
Do not summarize or paraphrase.

---

### 3.3 Active Tool Declaration
Prevents cross-tool contamination.

Example:

Active Tool: CBI Properties Palette Scope: NOD Identification Fields only

---

## 4. STARTING A NEW THREAD (MANDATORY TEMPLATE)

Copy/paste this entire block into the first message of every new thread:

---

### 🔷 THREAD STARTER TEMPLATE (copy/paste)

**Architect’s Lens ON.**  
Load architectural snapshots for this tool:

- **ToolIndex:** `<RAW URL to ToolIndex.XYZ.json>`
- **ClassGraph:** `<RAW URL to ClassGraph.XYZ.json>`

**Active Tool:** `<Tool Name>`  
**Scope Guard:**
- Only modify classes inside this tool's namespace  
- Do not change shared libraries unless explicitly requested  
- Do not modify other tools  
- Follow AutoCAD document-locking rules

**Problem Description:**  
(Brief high-level summary of what is broken or being added.)

**Here is the code we need to analyze:**  
(Paste exact code or file.)

**Do NOT generate code yet. Begin with analysis only.**

---

## 5. CHATGPT WORKFLOW EXPECTATIONS

### Step A — Analysis Phase (ChatGPT)
ChatGPT must:

- Load JSON architecture  
- Identify root causes  
- Validate the declared scope  
- Detect cross-class implications  

No code is generated yet.

---

### Step B — Approval Phase (User)
User confirms:

- The analysis appears correct  
- Scope is correct  
- No cross-tool impact  

User replies:

Approved. Proceed with proposed changes.

---

### Step C — Patch Phase (ChatGPT)
ChatGPT provides:

- Exact code modifications  
- Limited strictly to the active tool  
- Using C# 7.3 syntax, language version 9+  
- Following AutoCAD API locking rules  
- No refactors outside the approved scope

---

### Step D — Verification Phase (User)
User will:

- Apply code changes  
- Compile in Visual Studio  
- Test in AutoCAD  
- Report issues using the **CBI Crash Report Template**

---

### Step E — Changelog Update
Record modifications in the root-level changelog file:

AutoCAD/ └─ CBI_Tools_ChangeLog.md

Changelogs/ ├─ PropertiesPalette.changes.md ├─ ValveInsert.changes.md └─ etc...

Include:

- Tool name  
- Tool version  
- Summary of changes  
- Files modified  
- Reason for change  
- Risks / side effects  
- Follow-up items

---

## 6. WHEN TO REGENERATE ARCHITECTURAL SNAPSHOTS

Re-run `CBI.ArchMap.exe` and update JSON snapshots when:

- You create a new class  
- Move or rename a class  
- Delete a class  
- Add or remove a command  
- Add a new tool  
- Perform structural refactors  

Then **commit + push** updated files to GitHub.

---

## 7. WHAT THIS SOP PREVENTS

❌ Guessing class relationships  
❌ Breaking other tools  
❌ Scope creep  
❌ Hallucinated code  
❌ Complex detours  
❌ Out-of-date architectural assumptions  

Replaced by:

✔ Structural truth  
✔ Scoped precision  
✔ High-quality code patches  
✔ Predictable behavior  
✔ Repeatable debugging  
✔ Professional engineering rigor

---

## 8. OPTIONAL ENHANCEMENTS

Future additions can include:

- VS Code / VS 2022 snippet for the thread template  
- GitHub Action that validates JSON architecture  
- Tool Version Registry for tracking tool evolution  
- Obsidian developer dashboard  
- Web UI to browse architecture snapshots  

---

## 9. REVISION HISTORY

| Version | Date | Author | Notes |
|--------|-------|---------|-------|
| 1.0 | 2025-12-03 | ChatGPT (for Brian) | Initial release |

---

**End of Document**


---
