# HANDOFF: AIXORD v2.0 Development — Claude Web Session 2

**Created:** 2025-12-27
**Created By:** Claude Code (Commander)
**For:** Claude Web (Architect)
**Mode:** DECISION (brainstorming and specification)

---

## SESSION 1 SUMMARY

### Completed Work

| Artifact | Status | Location |
|----------|--------|----------|
| AIXORD_CHATGPT_REVIEWER_V2.md | Done | Created in Claude Web (needs placement in v2/) |
| CLAUDE_WEB_INSTRUCTIONS_PMERIT.md | Done | Pasted into Claude Web Project Instructions |
| AIXORD_GOVERNANCE_V2.md | Done | `products/aixord/v2/AIXORD_GOVERNANCE_V2.md` |
| Folder Reorganization | Done | archive/, v1/, v2/ structure created |

### Folder Reorganization (Completed This Session)

```
products/aixord/
├── archive/                    ← 5 legacy ScopeOrderSystem files
│   ├── HANDOFF_SCOPE_ORDER_SYSTEM_v3.md
│   ├── MANUSCRIPT_ScopeOrderSystem.md
│   ├── MANUSCRIPT_ScopeOrderSystem_v2.md
│   ├── MANUSCRIPT_ScopeOrderSystem_v3.md
│   └── MANUSCRIPT_ScopeOrderSystem_v3_DOCX.md
├── v1/                         ← Published AIXORD v1.0 reference
│   ├── MANUSCRIPT_AIXORD_v1.md
│   └── templates/              ← 9 template files
├── v2/                         ← Active v2.0 development
│   ├── AIXORD_GOVERNANCE_V2.md ← NEW (679 lines, comprehensive)
│   ├── README.md
│   └── HANDOFF_CLAUDE_WEB_SESSION_2.md ← THIS FILE
├── distribution/
├── 01-PRODUCT_OVERVIEW.md
├── 02-QUICK_START_GUIDE.md
├── 03-SALES_PAGE.md
├── 04-PRICING_STRATEGY.md
├── 05-EXAMPLE_WORKFLOW.md
├── AIXORD_VARIANTS.md
├── HANDOFF_AIXORD_V2.md
├── KDP_REPUBLISH_CHECKLIST.md
├── PRODUCT_TEST_FINDINGS.md
└── README.md
```

---

## ACTIVE DECISIONS (From Session 1)

| ID | Decision | Status |
|----|----------|--------|
| D-001 | Hardened authority model is canonical (from ChatGPT conversation) | ACTIVE |
| D-002 | AIXORD v2.0 replaces v1.1 on Gumroad | ACTIVE |
| D-003 | Moderate breaking change acceptable (clean naming, migration guide) | ACTIVE |
| D-004 | Product artifacts first, then PMERIT platform alignment | ACTIVE |
| D-005 | System Equation: MASTER_SCOPE = Project_Docs = All_SCOPEs = Production-Ready System | ACTIVE |

---

## SCOPE DECOMPOSITION STATUS

```
MASTER_SCOPE: AIXORD v2.0 Product
│
├── SCOPE_AIXORD_V2_CORE          ← IN_PROGRESS
│   ├── [x] ChatGPT Reviewer (created in Claude Web)
│   ├── [x] Claude Web Instructions (pasted)
│   ├── [x] AIXORD_GOVERNANCE_V2.md (679 lines - COMPLETE)
│   ├── [ ] AIXORD_STATE_V2.json (template)
│   └── [ ] CLAUDE_V2.md (Claude Code template)
│
├── SCOPE_CHATBOT_VARIANTS        ← BLOCKED (waiting on CORE complete)
│   ├── [ ] AIXORD_CHATGPT_PRO.md
│   ├── [ ] AIXORD_GEMINI_ADVANCED.md
│   ├── [ ] AIXORD_COPILOT.md
│   └── [ ] AIXORD_UNIVERSAL.md
│
├── SCOPE_MANUSCRIPT_V2           ← BLOCKED (waiting on VARIANTS)
│   └── [ ] Updated manuscript with v2.0 changes
│
└── SCOPE_DISTRIBUTION            ← BLOCKED (waiting on MANUSCRIPT)
    ├── [ ] aixord-v2-templates.zip
    └── [ ] Gumroad product update
```

---

## GOVERNANCE V2 HIGHLIGHTS

The new `AIXORD_GOVERNANCE_V2.md` (679 lines) includes these key additions from v1:

### New Features

1. **Visual Audit Mode** (Section 3.4)
   - Screenshot-driven verification for UI implementations
   - Required screenshots by SCOPE type
   - VISUAL_AUDIT_REPORT format
   - Automatic transition: EXECUTION → VISUAL_AUDIT → COMPLETE

2. **Enhanced SCOPE Lifecycle** (Section 4.3)
   ```
   EMPTY → AUDITED → SPECIFIED → IN_PROGRESS → VISUAL_AUDIT → COMPLETE → LOCKED
   ```

3. **VISUAL_AUDIT_REPORT Section** (Required for UI SCOPEs)

4. **Hardened Authority Model**
   - Explicit "What Each Role CANNOT Do" (Section 2.4)
   - Authority Transfer Rules (Section 2.3)

5. **Decision Log Protocol** (Section 5)
   - Append-only, never delete
   - Decision states: ACTIVE, SUPERSEDED, EXPERIMENTAL, REJECTED

6. **HALT Conditions** (Section 7)
   - 8 automatic triggers including "Visual discrepancy unresolved after 2 fix attempts"

---

## REMAINING WORK FOR SCOPE_AIXORD_V2_CORE

### 1. AIXORD_STATE_V2.json

Create a state template that includes:
- Authority tracking (decision_authority, execution_authority)
- Mode tracking (DECISION, EXECUTION, AUDIT, VISUAL_AUDIT)
- Visual audit state (pending_screenshots, last_audit_date)
- SCOPE status with lifecycle states

**Suggested Structure:**
```json
{
  "version": "2.0",
  "project_name": "[PROJECT]",
  "session": 1,
  "authority": {
    "decision": "human",
    "execution": "none"
  },
  "mode": "DECISION",
  "active_scope": null,
  "scope_status": {},
  "visual_audit": {
    "pending": [],
    "last_date": null
  },
  "blockers": [],
  "last_updated": "[DATE]"
}
```

### 2. CLAUDE_V2.md (Claude Code Template)

Create Claude Code instructions that enforce:
- Mandatory startup protocol (read governance, state, handoffs)
- Mode enforcement (refuse execution without HANDOFF)
- File lock checking before modifications
- HALT condition detection
- Visual audit triggers

**Key Sections Needed:**
- Startup Protocol (mirroring PMERIT CLAUDE.md pattern)
- Mode Commands
- SCOPE Commands
- Pre-Modification Check (lock enforcement)
- Error Handling (three-attempt rule)
- Session Continuity

### 3. Place AIXORD_CHATGPT_REVIEWER_V2.md

The ChatGPT Reviewer instructions were created in Claude Web Session 1 but need to be placed in `products/aixord/v2/`. User should copy from the Claude Web chat or recreate.

---

## FILES TO REFERENCE

| File | Purpose |
|------|---------|
| `v2/AIXORD_GOVERNANCE_V2.md` | Canonical v2 methodology (679 lines) |
| `v1/MANUSCRIPT_AIXORD_v1.md` | Published v1 manuscript for migration reference |
| `v1/templates/CLAUDE.md` | v1 Claude Code template (basis for v2) |
| `v1/templates/STATE.json` | v1 state template (basis for v2) |
| `AIXORD_VARIANTS.md` | Product variant roadmap |
| `HANDOFF_AIXORD_V2.md` | Session 1 original handoff |

---

## NEXT SESSION PRIORITIES

### Priority 1: Complete SCOPE_AIXORD_V2_CORE

1. **Create AIXORD_STATE_V2.json** — State template with v2 authority/mode fields
2. **Create CLAUDE_V2.md** — Claude Code instructions with mode enforcement
3. **Place AIXORD_CHATGPT_REVIEWER_V2.md** — User provides from Session 1

### Priority 2: ChatGPT Review

4. Have ChatGPT Reviewer validate:
   - AIXORD_GOVERNANCE_V2.md (already created)
   - AIXORD_STATE_V2.json (once created)
   - CLAUDE_V2.md (once created)

### Priority 3: Begin SCOPE_CHATBOT_VARIANTS

5. Create platform-specific instruction sets:
   - AIXORD_CHATGPT_PRO.md
   - AIXORD_GEMINI_ADVANCED.md
   - AIXORD_COPILOT.md
   - AIXORD_UNIVERSAL.md

---

## AUTHORITY STATE

| Authority | Current Holder |
|-----------|----------------|
| Decision Authority | Human (Director) |
| Execution Authority | Not transferred (still in DECISION MODE) |

**Current Mode:** DECISION

---

## CONTEXT FOR ARCHITECT

When continuing this session:

1. **System Equation is canonical:**
   ```
   MASTER_SCOPE = Project_Docs = All_SCOPEs = Production-Ready System
   ```

2. **v2 Breaking Changes from v1:**
   - Required SCOPE sections (VISUAL_AUDIT_REPORT for UI SCOPEs)
   - DECISION LOG immutability
   - Explicit mode commands
   - Enhanced HALT conditions
   - VISUAL_AUDIT lifecycle state

3. **Key Insight:** Visual Audit Mode was added because "code can be correct while UX is broken" — screenshots verify what users actually see.

4. **Repository:** `Pmerit_Product_Development/products/aixord/v2/`

---

*AIXORD v2.0 — Authority. Execution. Confirmation.*
*Handoff created: 2025-12-27 by Claude Code*
