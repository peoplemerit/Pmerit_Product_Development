# AIXORD for Claude Users

## Maximize Claude Pro and Claude Code with Structured Governance

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

To Claude users who want more than conversations—they want results.

This framework exists because chaos is optional.

---

## Table of Contents

**PART 1: FOUNDATION**

- Chapter 1: Introduction to AIXORD
- Chapter 2: The Authority Model
- Chapter 3: Mode Discipline
- Chapter 4: HALT Conditions
- Chapter 5: Session Continuity

**PART 2: CLAUDE-SPECIFIC SETUP**

- Chapter 6: Claude Pro — Project Knowledge Integration
- Chapter 7: Claude Code — File System Access & Automation
- Chapter 8: The Dual Workflow — Web = Architect, Code = Commander
- Chapter 9: Setting Up Your Claude AIXORD Project
- Chapter 10: Advanced — Parallel AI Instances

**APPENDICES**

- Appendix A: Quick Reference
- Appendix B: Download Your Templates

---

## Preface

Claude is one of the most capable AI assistants available. With Claude Pro's Project Knowledge and Claude Code's file system access, you have a powerful combination for building real projects.

But power without structure leads to chaos.

AIXORD gives Claude the governance framework it needs to be truly productive. You'll learn how to configure Claude Pro as your strategic Architect and Claude Code as your execution Commander—a workflow that matches AIXORD's authority model perfectly.

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

### Why AIXORD with Claude?

Claude excels at:
- Understanding context
- Following nuanced instructions
- Maintaining consistency within sessions

AIXORD amplifies these strengths by providing:
- Persistent context through HANDOFFs
- Clear role definitions
- Predictable behavior patterns

---

## Chapter 2: The Authority Model

### The Three Roles

**Human (Director)**
- Supreme authority
- Decides WHAT exists
- Approves all specifications

**AI Architect (Claude Web)**
- Advisory authority
- Proposes solutions
- Writes specifications

**AI Commander (Claude Code)**
- Delegated authority
- Implements specifications
- Executes exactly as specified

### The Authority Contract

| Role | Can Do | Cannot Do |
|------|--------|-----------|
| Director | Decide, approve, override | Micromanage implementation |
| Architect | Recommend, specify, advise | Execute, deploy |
| Commander | Implement, report, request clarification | Change requirements |

---

## Chapter 3: Mode Discipline

### DECISION Mode

Open exploration and specification writing.

- Brainstorm freely
- Explore options
- Document decisions (D-001, D-002, etc.)
- Claude operates as Architect

**Enter:** `ENTER DECISION MODE`

### EXECUTION Mode

Frozen decisions, implementation only.

- No new features
- No scope changes
- Claude operates as Commander

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
| Authority violation | Stop immediately |

### HALT Protocol

1. Stop all execution
2. Document what triggered HALT
3. Report to human
4. Wait for direction
5. No workarounds

### Embracing HALT

HALT is not failure—it's protection. Every HALT catches a problem before it compounds.

---

## Chapter 5: Session Continuity

### The HANDOFF

At session end, Claude generates a structured summary:

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

Next Priority:
1. [first thing]
```

### Session Protocol

**Ending:**
1. Say `HANDOFF`
2. Save generated summary locally

**Starting:**
1. Paste HANDOFF
2. Say `CONTINUE`
3. Claude reconstructs context

---

# PART 2: CLAUDE-SPECIFIC SETUP

---

## Chapter 6: Claude Pro — Project Knowledge Integration

### What is Project Knowledge?

Claude Pro ($20/mo) offers Projects—persistent workspaces where you can:
- Upload reference documents
- Maintain context across conversations
- Share projects with collaborators

### Setting Up AIXORD in Project Knowledge

**Step 1: Create a Project**

1. Open Claude (claude.ai)
2. Click "Projects" in sidebar
3. Create new project: "My AIXORD Project"

**Step 2: Upload Governance**

Add these files to Project Knowledge:
- `AIXORD_CLAUDE_DUAL.md` (or your variant)
- Your current `HANDOFF.md`
- Relevant `SCOPE` files

**Step 3: Configure Project Instructions**

In Project settings, add:

```
This project uses AIXORD governance.
Reference the uploaded AIXORD files for authority rules.
Always check HANDOFF.md for current state before responding.
```

### Benefits

- Governance is always loaded
- Claude references your files automatically
- No need to paste governance every session
- State persists across conversations

### Limitations

- Project Knowledge has upload limits
- Files must be manually updated
- Not integrated with file system

---

## Chapter 7: Claude Code — File System Access & Automation

### What is Claude Code?

Claude Code is a CLI tool that:
- Runs in your terminal
- Has full file system access
- Can execute commands
- Integrates with your IDE

### Installing Claude Code

```bash
npm install -g @anthropic-ai/claude-code
```

Or follow installation at: claude.ai/claude-code

### AIXORD Configuration

Create a `CLAUDE.md` file in your project root:

```markdown
# AIXORD Commander Configuration

You are the Commander in an AIXORD-governed project.

## Mode: EXECUTION

Decisions are frozen. Execute specifications exactly.

## Active Scope: [current scope]

## Rules:
- Read SCOPE files before implementing
- Follow specifications exactly
- Report progress after each step
- HALT if anything is unclear

## Current HANDOFF:
[Paste or reference current handoff]
```

Claude Code reads this file automatically.

### Capabilities

Claude Code can:
- Read and write files
- Run terminal commands
- Create directories
- Execute build processes
- Run tests

### Limitations

Claude Code should NOT:
- Make strategic decisions
- Change specifications
- Add features not specified
- Skip documentation

---

## Chapter 8: The Dual Workflow — Web = Architect, Code = Commander

### The Perfect Match

AIXORD's authority model maps perfectly to Claude's tools:

| AIXORD Role | Claude Tool | Function |
|-------------|-------------|----------|
| Architect | Claude Web (claude.ai) | Strategy, specification |
| Commander | Claude Code (CLI) | Implementation, execution |

### How It Works

**Phase 1: Architecture (Claude Web)**

1. Open Claude Web with your Project
2. Enter DECISION mode
3. Discuss, research, specify
4. Generate HANDOFF with specifications

**Phase 2: Handoff**

1. Save HANDOFF from Claude Web
2. Copy specifications to SCOPE files
3. Update CLAUDE.md in your project

**Phase 3: Execution (Claude Code)**

1. Open terminal in project directory
2. Claude Code reads CLAUDE.md
3. Enter EXECUTION mode
4. Claude Code implements specifications

**Phase 4: Report**

1. Claude Code completes implementation
2. You verify results
3. Report back to Claude Web
4. Cycle repeats

### Communication Protocol

Claude Web and Claude Code don't talk directly. You are the bridge:

```
Claude Web → HANDOFF → You → CLAUDE.md → Claude Code
Claude Code → Results → You → Status update → Claude Web
```

### Why This Works

- Clear separation of concerns
- Each Claude instance optimized for its role
- No context confusion
- Parallel work possible

---

## Chapter 9: Setting Up Your Claude AIXORD Project

### Directory Structure

```
my-project/
├── CLAUDE.md           # Claude Code configuration
├── MASTER_SCOPE.md     # Project vision
├── state/
│   └── STATE.json      # Current state
├── scopes/
│   ├── SCOPE_AUTH.md   # Feature scope
│   └── SCOPE_UI.md     # Feature scope
└── handoffs/
    ├── HANDOFF_001.md  # Session 1
    └── HANDOFF_002.md  # Session 2
```

### Initial Setup Steps

**1. Create Project in Claude Web**

- New project with descriptive name
- Upload AIXORD_CLAUDE_DUAL.md

**2. Initialize Local Directory**

Create the directory structure above.

**3. Configure Claude Code**

Create CLAUDE.md with Commander instructions.

**4. First Session**

- Claude Web: Define vision, initial decisions
- Generate first HANDOFF
- Save to handoffs/HANDOFF_001.md

**5. Begin Execution**

- Update CLAUDE.md with active scope
- Run Claude Code
- Implement first scope

### Maintenance

- Keep HANDOFF files numbered sequentially
- Update CLAUDE.md when active scope changes
- Upload new SCOPE files to Claude Web as needed
- Run Visual Audit for UI features

---

## Chapter 10: Advanced — Parallel AI Instances

### When to Use Parallel Instances

Consider parallel Claude instances when:
- You're waiting for Claude Code to finish
- You want to plan ahead
- Complex project needs simultaneous work

### The Pattern

```
Claude Web Instance 1: Planning SCOPE_BETA
Claude Web Instance 2: Reviewing SCOPE_ALPHA results
Claude Code: Executing SCOPE_ALPHA
```

### Coordination Rules

1. Each instance works on ONE scope only
2. Never have two instances on same scope
3. Human coordinates all handoffs
4. Document which instance does what

### Practical Example

```
10:00 — Start Claude Code on SCOPE_AUTH implementation
10:05 — While Code runs, open Claude Web
10:06 — In Web, start specifying SCOPE_UI
10:30 — Code finishes SCOPE_AUTH
10:31 — Review results, update state
10:32 — Give SCOPE_UI specs to Code
10:33 — In Web, start research for SCOPE_API
```

You've doubled throughput without confusion.

### Warnings

- More instances = more coordination overhead
- Don't parallelize until single-instance is smooth
- Always know which instance owns which scope

---

## Appendix A: Quick Reference

### Mode Commands

| Command | Effect |
|---------|--------|
| `ENTER DECISION MODE` | Open discussion (Web) |
| `ENTER EXECUTION MODE` | Implement specs (Code) |
| `AUDIT` | Read-only review |
| `HALT` | Stop everything |

### Session Commands

| Command | Effect |
|---------|--------|
| `CONTINUE` | Resume from handoff |
| `STATUS` | Report current state |
| `HANDOFF` | Generate session summary |
| `APPROVED` | Accept proposal |

### Dual Workflow Cheat Sheet

| Task | Tool |
|------|------|
| Strategy discussion | Claude Web |
| Specification writing | Claude Web |
| Research | Claude Web |
| File creation | Claude Code |
| Code implementation | Claude Code |
| Command execution | Claude Code |
| Visual audit | Claude Web + screenshots |

---

## Appendix B: Download Your Templates

As a book owner, you have FREE access to the AIXORD Claude Pack templates.

### Your Access Code

```
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│              Access Code: AIXORD-CLAUDE                     │
│                                                             │
│        Enter this code at checkout for FREE download        │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### Download Link

| Product | Regular Price | Your Price | Link |
|---------|---------------|------------|------|
| AIXORD Claude Pack | $9.99 | FREE | https://meritwise0.gumroad.com/l/zpnjv |

### How to Download

1. Click the link above (or type into your browser)
2. Click "I want this!"
3. Enter code: **AIXORD-CLAUDE**
4. Complete checkout ($0.00)
5. Download your ZIP file
6. Extract and start using!

### What's Included

- AIXORD_CLAUDE_DUAL.md (Pro + Code workflow)
- AIXORD_CLAUDE_PRO.md (Pro-only variant)
- AIXORD_CLAUDE_FREE.md (Free tier variant)
- CLAUDE.md template for Code
- Example project structure

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
