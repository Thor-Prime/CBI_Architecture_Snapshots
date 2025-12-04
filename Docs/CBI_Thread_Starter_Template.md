# CBI Thread Starter Template  
### Version 1.0 — December 2025

Use this template at the beginning of **every new ChatGPT debugging or development thread**.

---

## 🔷 THREAD STARTER TEMPLATE — COPY/PASTE INTO CHATGPT

**Architect’s Lens ON.**  
Load architectural snapshots:

- **ToolIndex:** `<RAW URL to ToolIndex.TOOLNAME.json>`
- **ClassGraph:** `<RAW URL to ClassGraph.TOOLNAME.json>`

**Active Tool:** `<Tool Name>`  
**Scope Guard:**  
- Only modify classes within this tool's namespace  
- No refactors outside scope  
- Follow AutoCAD document-locking rules  
- Do not modify shared projects unless explicitly approved  

**Problem Description:**  
(Short 2–4 sentence summary)

**Exact Code:**  
(Paste the real method, class, or file — no summaries)

**Do NOT generate code yet. Begin with analysis.**

---

## USAGE NOTES

- Always include raw URLs, not GitHub tree links  
- Always declare scope to avoid cross-tool breakage  
- Always paste exact code so ChatGPT can perform structural matching  
- Always let ChatGPT perform analysis *before* code generation  

---

## REVISION HISTORY

| Version | Date | Author | Notes |
|--------|-------|---------|-------|
| 1.0 | 2025-12-03 | ChatGPT (for Brian) | Initial release |
