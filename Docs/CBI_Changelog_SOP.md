# CBI Tool Changelog SOP  
### Version 1.0 — December 2025

This SOP defines how to maintain changelogs for every CBI tool, ensuring long-term traceability and preventing future breakage.

---

## 1. PURPOSE
To maintain a permanent, human-readable record of:

- What changed  
- Why it changed  
- Which files were affected  
- What risks were introduced  
- What follow-up actions remain  

This allows ChatGPT and future developers to understand tool evolution.

---

## 2. LOCATION OF CHANGELOGS

### Root master file:

AutoCAD/CBI_Tools_ChangeLog.md

### Per-tool logs:

AutoCAD/Changelogs/ ├─ PropertiesPalette.changes.md ├─ ValveInsert.changes.md ├─ ProjectStore.changes.md ├─ Tagging.changes.md ├─ SheetSetManager.changes.md └─ etc.

---

## 3. WHEN TO CREATE A CHANGELOG ENTRY
Add a new entry whenever a thread results in:

- Modified code  
- New classes  
- Deleted classes  
- Refactors  
- UI behavior changes  
- NOD/XData structural modifications  
- ProjectStore schema updates  
- AutoCAD locking behavior fixes  

---

## 4. CHANGELOG TEMPLATE

YYYY-MM-DD — Version <Tool v1.x>

Tool: <Tool Name>
Summary:
(Short description of the change)

Files Modified:

/path/to/ClassA.cs

/path/to/ClassB.cs


Details of Changes:

Bullet list of what was changed and why

Reasoning behind architectural decisions


Risk Assessment:
(Any potential impact on other tools or shared services)

Follow-Up Actions:

Items left to do

Items to test later


---

## 5. REVISION HISTORY

| Version | Date | Author | Notes |
|--------|-------|---------|-------|
| 1.0 | 2025-12-03 | ChatGPT (for Brian) | Initial release |
