# AIXORD for ChatGPT Users

## Structured Workflows for ChatGPT Pro and Plus Subscribers

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

To ChatGPT users who want their AI assistant to deliver real results.

This framework exists because chaos is optional.

---

## Table of Contents

**PART 1: FOUNDATION**

- Chapter 1: Introduction to AIXORD
- Chapter 2: The Authority Model
- Chapter 3: Mode Discipline
- Chapter 4: HALT Conditions
- Chapter 5: Session Continuity

**PART 2: CHATGPT-SPECIFIC SETUP**

- Chapter 6: ChatGPT Pro — Maximum Capability Setup
- Chapter 7: ChatGPT Plus — Custom Instructions Integration
- Chapter 8: Building a Dedicated AIXORD GPT
- Chapter 9: Using Code Interpreter with AIXORD
- Chapter 10: Memory and Context Management

**APPENDICES**

- Appendix A: Quick Reference
- Appendix B: Download Your Templates

---

## Preface

ChatGPT is the world's most popular AI assistant. Whether you're on the $200/month Pro tier with o1-level reasoning or the $20/month Plus tier with GPT-4, you have access to powerful capabilities.

But power without structure leads to chaos.

AIXORD gives ChatGPT the governance framework it needs to be truly productive. You'll learn how to use Custom Instructions, Custom GPTs, and Code Interpreter with AIXORD discipline—transforming conversations into completed projects.

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

Documents ARE the system. Your specifications, decisions, and research are as real as the code they produce.

### Why AIXORD with ChatGPT?

ChatGPT excels at:
- Natural conversation
- Creative problem solving
- Broad knowledge application

AIXORD amplifies these strengths by providing:
- Persistent context through HANDOFFs
- Clear role definitions
- Predictable behavior patterns

---

## Chapter 2: The Authority Model

### The Two Authorities

**Decision Authority** — Held by you (the human). Determines WHAT exists.

**Execution Authority** — Delegated to ChatGPT. Determines HOW to implement.

These never overlap.

### The Authority Contract

| Role | Authority | Cannot Do |
|------|-----------|-----------|
| Human (Director) | Decide, approve, override | Micromanage implementation |
| AI (Architect/Commander) | Recommend, implement, report | Make decisions, assume approval |

### The Golden Rule

ChatGPT proposes. You approve. Nothing proceeds without explicit approval.

---

## Chapter 3: Mode Discipline

### DECISION Mode

Open exploration and specification writing.

- Brainstorm freely
- Explore options
- Document decisions (D-001, D-002, etc.)
- ChatGPT operates as Architect

**Enter:** `ENTER DECISION MODE`

### EXECUTION Mode

Frozen decisions, implementation only.

- No new features
- No scope changes
- ChatGPT operates as Commander

**Enter:** `ENTER EXECUTION MODE`

### AUDIT Mode

Read-only investigation.

- Compare reality to documentation
- Find gaps
- No modifications

**Enter:** `AUDIT`

### The Discipline Rule

Never mix modes. If you need to change something during EXECUTION:

1. Say `HALT`
2. Enter DECISION mode
3. Make and document changes
4. Return to EXECUTION mode

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

1. Stop all execution
2. Document what triggered HALT
3. Report to human
4. Wait for direction

### Embracing HALT

HALT is protection, not failure. Every HALT catches a problem early.

---

## Chapter 5: Session Continuity

### The HANDOFF

At session end, ChatGPT generates a structured summary:

```
HANDOFF — [Project] Session [N]

State:
- Mode: DECISION/EXECUTION
- Active Scope: [name]

Decisions:
| ID | Decision | Status |
|----|----------|--------|
| D-001 | [decision] | APPROVED |

Completed:
- [items]

Pending:
- [items]
```

### Session Protocol

**Ending:**
1. Say `HANDOFF`
2. Copy and save the generated summary

**Starting:**
1. Paste your HANDOFF
2. Say `CONTINUE`
3. ChatGPT reconstructs context

---

# PART 2: CHATGPT-SPECIFIC SETUP

---

## Chapter 6: ChatGPT Pro — Maximum Capability Setup

### What ChatGPT Pro Offers

ChatGPT Pro ($200/mo) provides:
- Extended thinking with o1 model
- Unlimited GPT-4 access
- Priority during high demand
- Access to advanced features

### Using o1 with AIXORD

The o1 model excels at complex reasoning. Use it for:
- Architecture decisions
- Complex specification writing
- Problem analysis

### Pro Setup Pattern

**For Complex Decisions:**

```
You are operating under AIXORD governance.
I am the Director. You are the Architect.
Use your extended thinking to analyze this problem:
[Your complex question]
```

**For Implementation:**

```
AIXORD EXECUTION MODE.
Decisions are frozen. Implement this specification exactly:
[Paste specification]
```

### Maximizing Pro Benefits

| Task | Model | Why |
|------|-------|-----|
| Strategy decisions | o1 | Deep reasoning |
| Specification writing | GPT-4 | Good enough, faster |
| Code generation | GPT-4 | Optimized for code |
| Complex debugging | o1 | Pattern recognition |

---

## Chapter 7: ChatGPT Plus — Custom Instructions Integration

### What are Custom Instructions?

Custom Instructions let you define persistent context that ChatGPT remembers across conversations.

### Setting Up AIXORD Custom Instructions

**Step 1: Access Settings**

1. Click your profile icon
2. Select "Customize ChatGPT"
3. Find "Custom Instructions"

**Step 2: Configure "What would you like ChatGPT to know?"**

```
I use AIXORD governance for all projects.

AIXORD Rules:
- I am the Director (decision authority)
- You are Architect (DECISION mode) or Commander (EXECUTION mode)
- Nothing proceeds without my explicit approval
- Say HALT if anything is unclear

My current projects: [list your active projects]
```

**Step 3: Configure "How would you like ChatGPT to respond?"**

```
Always:
- Acknowledge current mode (DECISION or EXECUTION)
- Document decisions with IDs (D-001, D-002)
- Ask before proceeding on ambiguous items
- Generate HANDOFF when requested

Format responses with clear structure:
- Mode status at top
- Action taken
- What needs approval
- Next steps
```

### Benefits

- AIXORD rules load automatically
- No need to re-explain governance each session
- Consistent behavior across conversations

---

## Chapter 8: Building a Dedicated AIXORD GPT

### What are Custom GPTs?

Custom GPTs are specialized ChatGPT instances with:
- Pre-loaded instructions
- Uploaded knowledge files
- Custom capabilities

### Creating Your AIXORD GPT

**Step 1: Access GPT Builder**

1. Go to chat.openai.com
2. Click "Explore GPTs"
3. Click "Create"

**Step 2: Configure Basic Settings**

- Name: "AIXORD Commander"
- Description: "Structured AI collaboration with AIXORD governance"
- Instructions: [See below]

**Step 3: Instructions**

```
You are an AIXORD-governed AI assistant.

AUTHORITY MODEL:
- User is the Director (supreme authority)
- You are Architect in DECISION mode
- You are Commander in EXECUTION mode
- Never proceed without explicit approval

MODES:
- DECISION: Open discussion, brainstorming, specification
- EXECUTION: Frozen decisions, implement exactly as specified
- AUDIT: Read-only investigation

BEHAVIOR:
- At session start, report current mode and request HANDOFF
- Document all decisions with IDs (D-001, D-002, etc.)
- HALT immediately on ambiguity
- Generate HANDOFF at end of each session

Always acknowledge mode and state before responding.
```

**Step 4: Upload Knowledge**

Add these files:
- AIXORD governance template
- SCOPE template
- HANDOFF template

**Step 5: Enable Capabilities**

- Web Browsing: Optional (for research)
- Code Interpreter: Recommended
- DALL-E: Optional

### Using Your AIXORD GPT

1. Open your custom GPT
2. It already knows AIXORD rules
3. Start with your HANDOFF or project description
4. Work as normal with built-in governance

---

## Chapter 9: Using Code Interpreter with AIXORD

### What is Code Interpreter?

Code Interpreter lets ChatGPT:
- Write and execute Python code
- Process uploaded files
- Generate downloadable outputs

### AIXORD + Code Interpreter Pattern

**Phase 1: Specification (DECISION Mode)**

```
ENTER DECISION MODE

I need a Python script that:
- Reads a CSV file
- Calculates monthly totals
- Generates a summary report

Propose a specification.
```

ChatGPT proposes. You approve or modify.

**Phase 2: Implementation (EXECUTION Mode)**

```
ENTER EXECUTION MODE

Implement the approved specification.
Upload capability is enabled.
Generate the script and test it.
```

ChatGPT writes and runs the code.

**Phase 3: Verification**

```
AUDIT

Show me:
- What the script does
- Sample output
- Any limitations
```

### Best Practices

| Do | Don't |
|----|----- |
| Specify requirements first | Jump straight to "write code" |
| Approve before execution | Let ChatGPT decide scope |
| Review generated code | Blindly trust output |
| Save important outputs | Assume persistence |

### File Handling

Code Interpreter sessions are temporary. Always:
1. Download generated files immediately
2. Save code to your local machine
3. Document what was created in HANDOFF

---

## Chapter 10: Memory and Context Management

### ChatGPT Memory Feature

ChatGPT can remember things across conversations:
- Facts about you
- Project details
- Preferences

### Using Memory with AIXORD

**Good Uses:**
- "Remember that Project Alpha uses AIXORD"
- "Remember my role is Director"
- "Remember to always start with mode status"

**Bad Uses:**
- Trying to store entire HANDOFFs
- Relying on memory for critical decisions
- Assuming perfect recall

### The Memory Hierarchy

```
1. Custom Instructions — Always loaded
2. Memory — Usually loaded
3. HANDOFF — You paste at session start
4. Conversation — Current session only
```

### Best Practice

Don't rely solely on memory. Always:
1. Paste your current HANDOFF
2. State your current mode explicitly
3. Confirm ChatGPT has correct context

### Managing Memory

View and edit memory:
1. Settings → Personalization → Memory
2. Review stored memories
3. Delete incorrect entries
4. Add important project facts

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

### ChatGPT Feature Map

| Feature | AIXORD Use |
|---------|------------|
| Custom Instructions | Persistent governance |
| Custom GPT | Dedicated AIXORD assistant |
| Code Interpreter | Structured code generation |
| Memory | Project facts storage |
| o1 (Pro) | Complex reasoning |

---

## Appendix B: Download Your Templates

As a book owner, you have FREE access to the AIXORD ChatGPT Pack templates.

### Your Access Code

```
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│              Access Code: AIXORD-CHATGPT                    │
│                                                             │
│        Enter this code at checkout for FREE download        │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### Download Link

| Product | Regular Price | Your Price | Link |
|---------|---------------|------------|------|
| AIXORD ChatGPT Pack | $9.99 | FREE | https://meritwise0.gumroad.com/l/jfnzh |

### How to Download

1. Click the link above (or type into your browser)
2. Click "I want this!"
3. Enter code: **AIXORD-CHATGPT**
4. Complete checkout ($0.00)
5. Download your ZIP file
6. Extract and start using!

### What's Included

- AIXORD_CHATGPT_PRO.md ($200/mo tier)
- AIXORD_CHATGPT_PLUS.md ($20/mo tier)
- AIXORD_CHATGPT_FREE.md (Free tier)
- Custom Instructions template
- GPT Builder instructions

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
