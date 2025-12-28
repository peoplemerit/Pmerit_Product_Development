# AIXORD for Copilot Users

## IDE-Integrated AI Governance for Developers

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

To developers who want AI assistance without chaos.

This framework exists because chaos is optional.

---

## Table of Contents

**PART 1: FOUNDATION**

- Chapter 1: Introduction to AIXORD
- Chapter 2: The Authority Model (Code Context)
- Chapter 3: Mode Discipline for Coding
- Chapter 4: HALT Conditions in Development
- Chapter 5: Session Continuity with Version Control

**PART 2: COPILOT-SPECIFIC SETUP**

- Chapter 6: Copilot Chat — Applying AIXORD
- Chapter 7: IDE Integration Patterns
- Chapter 8: Code Review with AIXORD Principles
- Chapter 9: Combining Copilot with Other AI Tools

**APPENDICES**

- Appendix A: Quick Reference
- Appendix B: Download Your Templates

---

## Preface

GitHub Copilot and Microsoft Copilot are AI assistants designed for developers. They live in your IDE, understand your codebase, and generate code in context.

But inline suggestions without governance lead to chaos—code you didn't ask for, assumptions you didn't approve, and features that don't match your design.

AIXORD gives Copilot the structure it needs. You'll learn how to use project instructions, Copilot Chat with AIXORD discipline, and integrate with version control for true session continuity.

Keep building. Stay disciplined.

— Idowu J Gabriel, Sr.

---

# PART 1: FOUNDATION

---

## Chapter 1: Introduction to AIXORD

### What is AIXORD?

AIXORD (AI Execution Order) is a governance framework for AI collaboration. For developers using Copilot, it means:

- **Clear authority** — You decide WHAT code to write, Copilot suggests HOW
- **Explicit modes** — Either designing OR implementing
- **Written records** — Specifications before code

### The Code Equation

```
SPEC = Documentation = Implementation = Working System
```

For developers: Your specification IS the system. Copilot implements the spec; it doesn't decide what to build.

### Why AIXORD with Copilot?

Copilot excels at:
- Code completion in context
- Pattern recognition from your codebase
- Quick implementations

AIXORD amplifies these strengths by ensuring Copilot implements what you actually want.

---

## Chapter 2: The Authority Model (Code Context)

### Developer Authority

You are the Director of your codebase:

- You design the architecture
- You approve all significant code
- You decide what features exist

### Copilot Authority

Copilot is your implementation assistant:

- Suggests code implementations
- Follows patterns in your codebase
- Offers completion options

### The Code Authority Contract

| Decision | Who Decides |
|----------|-------------|
| What features to build | You (Director) |
| Which files to create | You (Director) |
| Architecture decisions | You (Director) |
| Implementation details | Copilot (suggests), You (approve) |
| Code patterns | Copilot (follows codebase), You (establish) |

### The Golden Rule

Copilot suggests. You accept, modify, or reject. Tab is approval.

---

## Chapter 3: Mode Discipline for Coding

### DECISION Mode (Design)

Design and architecture phase.

- Sketch out what you're building
- Define interfaces and contracts
- Write specifications in comments or docs
- No implementation yet

**Marker:** Create `// DECISION MODE` comment or design doc

### EXECUTION Mode (Implementation)

Implementation phase with frozen design.

- Follow specifications exactly
- Copilot assists with implementation
- No new features added
- No architecture changes

**Marker:** Create `// EXECUTION: [feature name]` comment

### AUDIT Mode (Review)

Code review phase.

- Compare implementation to specification
- Find gaps
- Document discrepancies
- No changes during audit

**Marker:** `// AUDIT: checking [feature]`

### The Discipline in Code

```javascript
// DECISION MODE: User Authentication
// - OAuth 2.0 with Google
// - JWT for session tokens
// - 24-hour expiry
// END DECISION

// EXECUTION: OAuth Implementation
function setupOAuth() {
    // Copilot assists with implementation
    // following the specification above
}
// END EXECUTION
```

---

## Chapter 4: HALT Conditions in Development

### When to Stop and Think

| Condition | Action |
|-----------|--------|
| Copilot suggests unexpected architecture | HALT, review suggestion |
| Code doesn't match specification | HALT, check spec |
| New dependency suggested | HALT, evaluate |
| Security-sensitive code generated | HALT, review carefully |
| "This seems wrong" feeling | HALT, investigate |

### HALT in Practice

When Copilot suggests something unexpected:

1. Don't accept (don't press Tab)
2. Escape to dismiss
3. Review what was suggested
4. Decide if it matches your spec
5. Either accept with modifications or reject

### The Three-Strike Rule

If Copilot gives unhelpful suggestions three times:

1. Stop trying
2. Write the code manually
3. Or clarify your specification
4. Or use Copilot Chat to discuss

---

## Chapter 5: Session Continuity with Version Control

### Git as Your HANDOFF System

Git commits ARE your session HANDOFFs:

```bash
git commit -m "DECISION: Auth module architecture

Decisions:
- D-001: OAuth 2.0 with Google/GitHub
- D-002: JWT with 24hr expiry
- D-003: PostgreSQL for user storage

Status: SPECIFIED, ready for EXECUTION"
```

### Branch Strategy for AIXORD

```
main
└── feature/auth
    ├── auth-decision     (specification commits)
    └── auth-execution    (implementation commits)
```

### Commit Message Format

```
[MODE]: Brief description

Decisions:
- D-XXX: Decision made

Status: [SPECIFIED/IN_PROGRESS/COMPLETE]

Notes:
- Any important context
```

### Example Workflow

```bash
# Start with specification
git checkout -b feature/auth
# Write specs, commit
git commit -m "DECISION: Auth module specification"

# Implementation
git checkout -b auth-execution
# Implement with Copilot assistance
git commit -m "EXECUTION: OAuth setup complete"
git commit -m "EXECUTION: JWT implementation"

# Merge when complete
git checkout feature/auth
git merge auth-execution
git commit -m "COMPLETE: Auth module"
```

---

# PART 2: COPILOT-SPECIFIC SETUP

---

## Chapter 6: Copilot Chat — Applying AIXORD

### What is Copilot Chat?

Copilot Chat is conversational AI in your IDE:
- VS Code: Sidebar panel
- JetBrains: Tool window
- CLI: `gh copilot`

### AIXORD Chat Pattern

**Starting a Task:**

```
I'm working under AIXORD governance.

MODE: DECISION
SCOPE: User authentication

I need to design an auth system with:
- OAuth 2.0 (Google, GitHub)
- JWT sessions
- Role-based access

Propose an architecture.
```

**Reviewing Proposal:**

After Copilot proposes:
- Say `APPROVED` if acceptable
- Say `MODIFY: [specific changes]` if needs adjustment
- Say `REJECTED: [reason]` if wrong approach

**Moving to Implementation:**

```
MODE: EXECUTION
SCOPE: Auth (approved specification above)

Implement the OAuth setup function.
Show code for src/auth/oauth.ts
```

### Chat Commands

| Command | Effect |
|---------|--------|
| `/explain` | Understand existing code |
| `/fix` | Debug with AIXORD context |
| `/tests` | Generate tests for spec |
| `/doc` | Generate documentation |

### AIXORD + Chat Example

```
You: MODE: EXECUTION. Implement login function per spec:
- Validate email format
- Check user exists in DB
- Return JWT on success
- Return error on failure

Copilot: [Generates implementation]

You: APPROVED. Now implement the logout function.
```

---

## Chapter 7: IDE Integration Patterns

### Project Instructions File

Create `.github/copilot-instructions.md`:

```markdown
# AIXORD Project Configuration

This project uses AIXORD governance for AI-assisted development.

## Authority
- Human developer is Director
- Copilot assists with implementation
- No features without specification

## Current Mode: EXECUTION

## Active Specifications
See /specs/ directory for current specifications.

## Patterns to Follow
- [List your code patterns]
- [Architecture conventions]
- [Naming conventions]

## Do Not
- Add features not in specs
- Change architecture without DECISION mode
- Skip tests
```

### Specification Files

Create `/specs/` directory:

```
/specs/
├── MASTER_SPEC.md       # Project overview
├── SPEC_AUTH.md         # Auth specification
├── SPEC_API.md          # API specification
└── SPEC_UI.md           # UI specification
```

Each spec file:

```markdown
# SPEC: Authentication

## Status: IN_PROGRESS

## Decisions
| ID | Decision | Status |
|----|----------|--------|
| D-001 | OAuth 2.0 | APPROVED |
| D-002 | JWT 24hr | APPROVED |

## Requirements
- User can sign in with Google
- User can sign in with GitHub
- Sessions expire after 24 hours

## Implementation Notes
- Use passport.js for OAuth
- Use jsonwebtoken for JWT

## Files
- src/auth/oauth.ts
- src/auth/jwt.ts
- src/middleware/auth.ts
```

### IDE Workflow

1. Open spec file for context
2. Open implementation file
3. Write `// EXECUTION: [spec section]`
4. Let Copilot assist
5. Review and accept/reject suggestions
6. Update spec status when complete

---

## Chapter 8: Code Review with AIXORD Principles

### Pre-Review Checklist

Before requesting review:

- [ ] Implementation matches specification
- [ ] All spec requirements addressed
- [ ] No features beyond spec
- [ ] Tests exist for requirements
- [ ] Documentation updated

### AIXORD Review Protocol

**Reviewer Actions:**

1. Read specification first
2. Compare code to spec
3. Document discrepancies
4. Use PASS/DISCREPANCY verdicts

**Review Comments:**

```
DISCREPANCY: Spec says 24hr JWT expiry, code shows 48hr
File: src/auth/jwt.ts:45
Required: Change expiresIn from "48h" to "24h"
```

```
PASS: OAuth implementation matches spec D-001
```

### PR Template with AIXORD

```markdown
## AIXORD PR Template

### Specification
- Spec File: /specs/SPEC_AUTH.md
- Decisions Implemented: D-001, D-002

### Mode
- [x] EXECUTION (implementing approved spec)
- [ ] DECISION (specification changes)

### Checklist
- [ ] Implementation matches specification
- [ ] Tests added/updated
- [ ] No features beyond spec
- [ ] Documentation updated

### Screenshots (if UI)
[Add screenshots for visual audit]
```

---

## Chapter 9: Combining Copilot with Other AI Tools

### Multi-Tool Strategy

| Task | Best Tool |
|------|-----------|
| Architecture discussion | Claude/ChatGPT |
| Specification writing | Claude/ChatGPT |
| Implementation | Copilot |
| Code completion | Copilot |
| Complex debugging | Claude Code |
| Code review | Copilot + manual |

### Handoff Between Tools

**From Claude to Copilot:**

1. Specify with Claude (DECISION mode)
2. Claude generates HANDOFF with specs
3. Copy specs to /specs/ directory
4. Implement with Copilot (EXECUTION mode)

**From Copilot to Claude:**

1. Implement with Copilot
2. Hit a complex problem
3. Export relevant code
4. Discuss with Claude
5. Return to Copilot with solution

### Example Multi-Tool Session

```
[Claude Web - 30 min]
DECISION MODE: Design notification system
Result: SPEC_NOTIFICATIONS.md with 5 decisions

[Local IDE + Copilot - 2 hours]
EXECUTION MODE: Implement notification system
Result: Working implementation in 3 files

[Claude Code - 30 min]
AUDIT MODE: Verify implementation matches spec
Result: 2 discrepancies found

[Local IDE + Copilot - 30 min]
EXECUTION MODE: Fix discrepancies
Result: Spec-compliant implementation
```

---

## Appendix A: Quick Reference

### Mode Markers in Code

```javascript
// DECISION MODE: [feature]
// EXECUTION: [feature]
// AUDIT: [feature]
// HALT: [reason]
// APPROVED: [item]
```

### Copilot Chat Commands

| Command | Purpose |
|---------|---------|
| `/explain` | Understand code |
| `/fix` | Debug issues |
| `/tests` | Generate tests |
| `/doc` | Generate docs |

### Git Commit Prefixes

| Prefix | Mode |
|--------|------|
| `DECISION:` | Specification commit |
| `EXECUTION:` | Implementation commit |
| `AUDIT:` | Review findings |
| `COMPLETE:` | Feature done |

### Files to Create

| File | Purpose |
|------|---------|
| `.github/copilot-instructions.md` | Project governance |
| `/specs/MASTER_SPEC.md` | Project overview |
| `/specs/SPEC_*.md` | Feature specs |

---

## Appendix B: Download Your Templates

As a book owner, you have FREE access to the AIXORD Copilot Pack templates.

### Your Access Code

```
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│              Access Code: AIXORD-COPILOT                    │
│                                                             │
│        Enter this code at checkout for FREE download        │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### Download Link

| Product | Regular Price | Your Price | Link |
|---------|---------------|------------|------|
| AIXORD Copilot Pack | $4.99 | FREE | https://meritwise0.gumroad.com/l/jctnyh |

### How to Download

1. Click the link above (or type into your browser)
2. Click "I want this!"
3. Enter code: **AIXORD-COPILOT**
4. Complete checkout ($0.00)
5. Download your ZIP file
6. Extract and start using!

### What's Included

- AIXORD_COPILOT.md governance template
- copilot-instructions.md template
- Spec file templates
- PR template with AIXORD
- Git commit templates

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
