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