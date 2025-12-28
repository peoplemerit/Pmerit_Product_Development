# AIXORD for Gemini Users

## AI Governance for Google's Gemini Platform

**By Idowu J Gabriel, Sr.**

PMERIT Publishing
Caribou, United States
2025

---

© 2025 by Idowu J Gabriel, Sr.

All rights reserved.

For permission requests, contact:
info@pmerit.com

Printed in United States
First Edition

---

## Dedication

To Gemini users building in the Google ecosystem.

This framework exists because chaos is optional.

---

## Table of Contents

**PART 1: FOUNDATION**

- Chapter 1: Introduction to AIXORD
- Chapter 2: The Authority Model
- Chapter 3: Mode Discipline
- Chapter 4: HALT Conditions
- Chapter 5: Session Continuity

**PART 2: GEMINI-SPECIFIC SETUP**

- Chapter 6: Gemini Advanced — Using Gems for AIXORD
- Chapter 7: Google Ecosystem Integration
- Chapter 8: Setting Up Your Gemini AIXORD Workflow
- Chapter 9: Limitations and Workarounds

**APPENDICES**

- Appendix A: Quick Reference
- Appendix B: Download Your Templates

---

## Preface

Google's Gemini is a powerful AI assistant integrated into the Google ecosystem. With Gemini Advanced's Gems feature and tight integration with Google Workspace, you have unique capabilities for structured work.

AIXORD gives Gemini the governance framework it needs to be truly productive. You'll learn how to create dedicated Gems, integrate with Google Docs for documentation, and work around Gemini's specific limitations.

Keep building. Stay disciplined.

— Idowu J Gabriel, Sr.

---

# PART 1: FOUNDATION

---

## Chapter 1: Introduction to AIXORD

### What is AIXORD?

AIXORD (AI Execution Order) is a governance framework for AI collaboration. Inspired by military operations orders (OPORD), it provides:

- **Clear authority** — You decide WHAT, AI decides HOW
- **Explicit modes** — Either discussing OR implementing
- **Written records** — If it's not documented, it doesn't exist

### The System Equation

```
MASTER_SCOPE = Project_Docs = All_SCOPEs = Production-Ready System
```

Documents ARE the system. Gemini helps you create and maintain these documents systematically.

### Why AIXORD with Gemini?

Gemini excels at:
- Google Workspace integration
- Multi-modal understanding
- Natural conversation

AIXORD amplifies these strengths by providing structure and accountability.

---

## Chapter 2: The Authority Model

### The Two Authorities

**Decision Authority** — Held by you (the human). Determines WHAT exists.

**Execution Authority** — Delegated to Gemini. Determines HOW to implement.

### The Authority Contract

| Role | Authority | Cannot Do |
|------|-----------|-----------|
| Human (Director) | Decide, approve, override | Micromanage implementation |
| AI (Architect/Commander) | Recommend, implement, report | Make decisions |

---

## Chapter 3: Mode Discipline

### DECISION Mode

Open exploration and specification writing.

- Brainstorm freely
- Explore options
- Document decisions

**Enter:** `ENTER DECISION MODE`

### EXECUTION Mode

Frozen decisions, implementation only.

- No new features
- Follow specifications exactly

**Enter:** `ENTER EXECUTION MODE`

### AUDIT Mode

Read-only investigation.

**Enter:** `AUDIT`

---

## Chapter 4: HALT Conditions

### Automatic Triggers

| Condition | Response |
|-----------|----------|
| Ambiguous requirement | Stop and ask |
| Missing specification | Stop and request |
| Prerequisite not met | Stop and report |
| Three consecutive failures | Stop and escalate |

### HALT Protocol

Stop all work. Document issue. Wait for direction.

---

## Chapter 5: Session Continuity

### The HANDOFF

At session end, Gemini generates a summary:

```
HANDOFF — [Project] Session [N]

State:
- Mode: DECISION/EXECUTION

Decisions:
| ID | Decision | Status |
|----|----------|--------|
| D-001 | [decision] | APPROVED |

Completed: [items]
Pending: [items]
```

### Session Protocol

**Ending:** Say `HANDOFF`, save the output.

**Starting:** Paste HANDOFF, say `CONTINUE`.

---

# PART 2: GEMINI-SPECIFIC SETUP

---

## Chapter 6: Gemini Advanced — Using Gems for AIXORD

### What are Gems?

Gems (Gemini Advanced, $20/mo) are saved instruction sets that customize Gemini's behavior. Think of them as specialized assistants within Gemini.

### Creating an AIXORD Gem

**Step 1: Access Gems**

1. Open Gemini (gemini.google.com)
2. Click the Gems icon in sidebar
3. Click "New Gem"

**Step 2: Configure Your Gem**

**Name:** AIXORD Commander

**Instructions:**

```
You are an AIXORD-governed AI assistant.

AUTHORITY MODEL:
- User is the Director (supreme authority)
- You are Architect in DECISION mode
- You are Commander in EXECUTION mode
- Never proceed without explicit user approval

MODES:
- DECISION: Open discussion, brainstorming, specification writing
- EXECUTION: Decisions frozen, implement exactly as specified
- AUDIT: Read-only investigation

SESSION BEHAVIOR:
At start: Report mode, request HANDOFF if continuing
During: Follow mode rules, document decisions with IDs (D-001, etc.)
At end: Generate complete HANDOFF when requested

HALT CONDITIONS:
- Ambiguous requirement → HALT and ask
- Missing specification → HALT and request
- Unsure what user wants → HALT and clarify

Always acknowledge current mode before responding.
```

**Step 3: Save Gem**

Click "Create" to save your AIXORD Gem.

### Using Your AIXORD Gem

1. Click Gems in sidebar
2. Select "AIXORD Commander"
3. Start conversation with governance active
4. Work as normal with built-in rules

### Multiple Gems for Different Modes

Consider creating specialized Gems:

| Gem | Purpose |
|-----|---------|
| AIXORD Architect | Strategy and specification |
| AIXORD Commander | Implementation focus |
| AIXORD Auditor | Review and verification |

---

## Chapter 7: Google Ecosystem Integration

### Google Docs for Documentation

Use Google Docs to maintain your AIXORD documents:

**Folder Structure:**

```
My Drive/
└── AIXORD Projects/
    └── Project Alpha/
        ├── MASTER_SCOPE.gdoc
        ├── SCOPES/
        │   ├── SCOPE_AUTH.gdoc
        │   └── SCOPE_UI.gdoc
        └── HANDOFFS/
            ├── HANDOFF_001.gdoc
            └── HANDOFF_002.gdoc
```

### Linking Gemini to Docs

Currently, Gemini cannot directly read Google Docs. Use this workflow:

**Updating SCOPE files:**

1. Discuss with Gemini
2. Gemini generates content
3. Copy to your Google Doc
4. Save document

**Starting sessions:**

1. Open your HANDOFF in Google Docs
2. Copy contents
3. Paste into Gemini
4. Say `CONTINUE`

### Google Sheets for State Tracking

Create a STATE tracker spreadsheet:

| Field | Value |
|-------|-------|
| Current Mode | DECISION |
| Active Scope | SCOPE_AUTH |
| Last Handoff | HANDOFF_003 |
| Last Updated | 2025-01-15 |

**Decisions Log Tab:**

| ID | Date | Decision | Status | Scope |
|----|------|----------|--------|-------|
| D-001 | 2025-01-10 | Use OAuth | APPROVED | AUTH |
| D-002 | 2025-01-12 | PostgreSQL DB | APPROVED | AUTH |

### Google Calendar Integration

Schedule AIXORD sessions:
- Block focused time
- Set reminders for handoff reviews
- Track project milestones

---

## Chapter 8: Setting Up Your Gemini AIXORD Workflow

### Initial Setup Checklist

**Step 1: Create AIXORD Gem**
- Follow instructions in Chapter 6
- Test that governance loads correctly

**Step 2: Set Up Google Drive Structure**
- Create project folder
- Add MASTER_SCOPE template
- Create HANDOFFS subfolder

**Step 3: Create State Tracker**
- Set up Google Sheet
- Add Decision Log tab
- Bookmark for quick access

### Daily Workflow

**Morning:**

1. Open State Tracker, note current mode
2. Open last HANDOFF
3. Start Gemini with AIXORD Gem
4. Paste HANDOFF, say `CONTINUE`

**During Session:**

1. Work in one mode only
2. Document decisions as you go
3. Update tracker after major decisions

**Session End:**

1. Say `HANDOFF`
2. Create new Google Doc: HANDOFF_XXX
3. Paste generated handoff
4. Update State Tracker

### Weekly Review

- Review all HANDOFFs from the week
- Update MASTER_SCOPE if direction changed
- Archive completed SCOPEs
- Plan next week's priorities

---

## Chapter 9: Limitations and Workarounds

### Limitation 1: No Persistent Memory

**Problem:** Gemini doesn't remember previous conversations.

**Workaround:**
- Always paste HANDOFF at session start
- Use Gems for persistent instructions
- Maintain external state in Google Sheets

### Limitation 2: No File System Access

**Problem:** Gemini can't read or write local files.

**Workaround:**
- Use Google Docs as your documentation layer
- Copy/paste between Gemini and Docs
- Use Google Apps Script for automation

### Limitation 3: Limited Code Execution

**Problem:** Gemini can generate code but not execute it reliably.

**Workaround:**
- Treat Gemini as Architect (specifies code)
- Use local environment for execution
- Consider pairing with Claude Code for implementation

### Limitation 4: Context Window

**Problem:** Very long conversations may lose context.

**Workaround:**
- Generate HANDOFFs frequently
- Keep individual sessions focused
- Split large tasks across sessions

### Multi-Platform Strategy

For complex projects, combine tools:

| Task | Best Tool |
|------|-----------|
| Strategy discussion | Gemini |
| Documentation | Google Docs |
| State tracking | Google Sheets |
| Code execution | Local IDE + Claude Code |
| Quick questions | Gemini Gem |

---

## Appendix A: Quick Reference

### Mode Commands

| Command | Effect |
|---------|--------|
| `ENTER DECISION MODE` | Open discussion |
| `ENTER EXECUTION MODE` | Implement specs |
| `AUDIT` | Read-only review |
| `HALT` | Stop everything |

### Session Commands

| Command | Effect |
|---------|--------|
| `CONTINUE` | Resume from handoff |
| `STATUS` | Report current state |
| `HANDOFF` | Generate session summary |
| `APPROVED` | Accept proposal |

### Google Integration Map

| Need | Google Tool |
|------|-------------|
| Documents | Google Docs |
| State tracking | Google Sheets |
| Scheduling | Google Calendar |
| Collaboration | Google Drive sharing |
| Automation | Google Apps Script |

---

## Appendix B: Download Your Templates

As a book owner, you have FREE access to the AIXORD Gemini Pack templates.

### Your Access Code

```
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│              Access Code: AIXORD-GEMINI                     │
│                                                             │
│        Enter this code at checkout for FREE download        │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### Download Link

| Product | Regular Price | Your Price | Link |
|---------|---------------|------------|------|
| AIXORD Gemini Pack | $7.99 | FREE | https://meritwise0.gumroad.com/l/qndnd |

### How to Download

1. Click the link above (or type into your browser)
2. Click "I want this!"
3. Enter code: **AIXORD-GEMINI**
4. Complete checkout ($0.00)
5. Download your ZIP file
6. Extract and start using!

### What's Included

- AIXORD_GEMINI_ADVANCED.md (with Gems)
- AIXORD_GEMINI_FREE.md (Free tier)
- Gem configuration templates
- Google Sheets state tracker template

### Support

Questions about AIXORD? Email: info@pmerit.com

Updates and new versions: pmerit.com

---

## About the Author

**Idowu J Gabriel, Sr.** is the founder of PMERIT, an educational technology platform dedicated to making knowledge accessible to everyone.

Connect with PMERIT:
- Website: pmerit.com
- Email: info@pmerit.com

---

**PMERIT Publishing**
Caribou, United States
© 2025 Idowu J Gabriel, Sr.

---

*AIXORD — Authority. Execution. Confirmation.*

**END OF MANUSCRIPT**
