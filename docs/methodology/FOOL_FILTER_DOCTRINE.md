# PMERIT Fool Filter Doctrine

**Version:** 1.0
**Created:** December 25, 2025
**Purpose:** Standard risk mitigation embedded in all PMERIT products
**Legal Basis:** Informed consent, assumption of risk, caveat emptor

---

## Philosophy

> *"There's no perfection in life, but we walk around fire rather than walking through it. Just because something doesn't work for one person doesn't mean it will not work for others."*

**Core Principle:** Absolute prohibition is paternalistic. It excludes capable people who can make informed decisions. PMERIT products empower users while filtering out those who cannot exercise reasonable judgment.

---

## The Fool Filter Mechanism

```
Sophisticated User                    Fool
       │                                │
       ▼                                ▼
  Reads disclaimer                 Clicks through blindly
       │                                │
       ▼                                ▼
  Understands risks                Ignores warnings
       │                                │
       ▼                                ▼
  Makes informed decision          Proceeds anyway
       │                                │
       ▼                                ▼
  BENEFITS from tool               Higher likelihood of misuse
       │                                │
       ▼                                ▼
  Product works as intended        BUT: Signed waiver
                                   limits PMERIT's liability
```

**The doctrine works in PMERIT's favor regardless of user type:**
- Sophisticated users benefit and become advocates
- Fools self-identify by signing waivers they didn't read, limiting liability

---

## Tiered Consent Model

All PMERIT products implement a three-tier access system:

### Tier 1: Open Access
**No special consent needed**

- General information
- Educational content
- Standard templates
- Learning materials

**Examples:**
- "What is an LLC?"
- "How do tax brackets work?"
- "Explain the AIXORD methodology"

### Tier 2: Informed Consent Zone
**User signs acknowledgment + waiver**

- Edge services with full disclosure
- Personalized guidance
- Document preparation
- Analysis and recommendations

**Examples:**
- "Help me understand my options for business structure"
- "Analyze this contract for potential issues"
- "What questions should I ask an attorney?"
- "Help me prepare for small claims court"

### Tier 3: Hard Boundary
**System blocks regardless of consent**

- Representing user in legal proceedings
- Filing documents on user's behalf
- Claiming professional licensure
- Guaranteeing outcomes
- Active criminal matter advice

**Examples:**
- "Represent me in court"
- "File this with the IRS for me"
- "I'm being sued, tell me exactly what to do"

---

## Signature Gate Implementation

### Standard Consent Form

```
┌─────────────────────────────────────────────────────────────┐
│  ACKNOWLEDGMENT & INFORMED CONSENT                          │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  You are requesting assistance that goes beyond general     │
│  information. Please understand:                            │
│                                                             │
│  □ This tool is NOT a licensed professional                 │
│  □ This is NOT professional advice for your situation       │
│  □ Outcomes may vary based on your circumstances            │
│  □ You are responsible for verifying accuracy               │
│  □ Complex matters should involve a licensed professional   │
│                                                             │
│  By proceeding, you acknowledge that you:                   │
│  □ Have read and understood these limitations               │
│  □ Accept full responsibility for how you use this output   │
│  □ Waive claims against PMERIT for reliance on this tool    │
│                                                             │
│  Electronic Signature: ____________________                 │
│  Date: __________  Time: __________  IP: __________         │
│                                                             │
│  [I UNDERSTAND & ACCEPT]          [CANCEL]                  │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

### Requirements for Valid Consent

| Requirement | Purpose |
|-------------|---------|
| Timestamped record | Proves when consent was given |
| IP address logged | Identifies consenting party |
| Plain language | No legalese hiding the meaning |
| Specific checkboxes | User acknowledges each risk individually |
| Confirmation step | "Are you sure?" prevents accidental acceptance |
| Re-consent triggers | Major actions require fresh consent |
| Downloadable copy | User can save their acknowledgment |

---

## Classification Logic

### Block Triggers (Tier 3 — Hard Block)

Detect and block requests containing:
- "Represent me..."
- "File this for me..."
- "Guarantee that..."
- "I'm being prosecuted/sued for..."
- "On my behalf..."
- "As my lawyer/attorney/accountant..."

### Consent Triggers (Tier 2 — Gate Required)

Require signed consent for:
- "Should I..."
- "What's my best option..."
- "Analyze my specific..."
- "What questions should I ask..."
- "Help me prepare..."
- "Draft a custom..."
- "Review my situation..."

### Open Triggers (Tier 1 — No Gate)

Allow freely:
- "What is..."
- "How does [law/process] work..."
- "Help me understand..."
- "Explain..."
- "What are the requirements for..."
- "Fill out this standard form..."

---

## Block Response Template

When Tier 3 request detected:

```
⛔ This request cannot be processed.

[REASON]: This request involves [representing you in legal
proceedings / filing on your behalf / guaranteeing outcomes],
which requires a licensed professional and cannot be delegated
to an AI system.

✅ PMERIT can help you with:
• Understanding general concepts and processes
• Preparing standard document templates
• Learning about common requirements
• Preparing questions for licensed professionals

Would you like me to help you with one of these instead?
```

---

## Consent Response Template

When Tier 2 request detected (before consent):

```
⚠️ This request requires your informed consent.

You're asking for [personalized analysis / specific guidance /
edge-case assistance]. Before proceeding, please understand
that PMERIT provides information and tools, not professional
advice.

[SHOW CONSENT FORM]

If you're comfortable with these limitations, please sign the
acknowledgment to continue.
```

---

## Product-Specific Applications

### AIXORD Framework
- Tier 1: Methodology explanation, general templates
- Tier 2: Custom workflow creation, integration guidance
- Tier 3: N/A (pure methodology product)

### Tax Assistant
- Tier 1: "What is Schedule C?", standard form guidance
- Tier 2: "Analyze my deductions", "What should I claim?"
- Tier 3: "File my taxes for me", "Represent me in audit"

### Legal Assistant
- Tier 1: "What is an LLC?", "Explain contract terms"
- Tier 2: "Review this contract", "Help me form an LLC"
- Tier 3: "Represent me in court", "File this lawsuit"

### Project Assistant
- Tier 1: Methodology, templates, general guidance
- Tier 2: Custom project planning, risk assessment
- Tier 3: N/A (no professional licensure issues)

---

## Positioning Language

### Use This
- "Legal Information Guide"
- "Document Preparation Assistant"
- "Tax Learning Companion"
- "Legal Literacy Tool"
- "Self-Service Legal Resources"
- "AI-Assisted Document Preparation"

### Never Use This
- "AI Lawyer"
- "Robot Attorney"
- "Tax Advisor"
- "Legal Counsel"
- "Professional [X] Services"
- "Licensed [X]"

---

## The DoNotPay Lesson

**Case Study:** DoNotPay was fined $193,000 by the FTC (February 2025) for:
- Marketing as "robot lawyer"
- Not testing whether AI performed at attorney level
- Misleading consumers about capabilities

**PMERIT's Differentiation:**
- Never claim professional licensure
- Always disclose AI limitations
- Implement consent gates
- Block truly prohibited requests
- Position as "assistance" not "advice"

---

## Risk Allocation

| Party | Responsibility |
|-------|----------------|
| **PMERIT** | Accurate information, clear disclaimers, documented consent, blocking prohibited requests |
| **User** | Reading disclaimers, making informed choice, verifying outputs, seeking professional help when needed |
| **System** | Enforcing tier classification, logging consent, blocking Tier 3 requests |

---

## Implementation Checklist

For each PMERIT product:

- [ ] Classify all features into Tier 1/2/3
- [ ] Implement consent gate for Tier 2 features
- [ ] Implement hard block for Tier 3 requests
- [ ] Use approved positioning language
- [ ] Include standard disclaimers
- [ ] Log all consent events
- [ ] Provide downloadable consent copies
- [ ] Test classification logic
- [ ] Document tier assignments

---

## Legal Foundation

This doctrine is grounded in established legal principles:

| Doctrine | Application |
|----------|-------------|
| **Informed Consent** | User understands risks before proceeding |
| **Assumption of Risk** | User accepts responsibility for outcome |
| **Waiver of Liability** | Contractual release of claims |
| **Pro Se Doctrine** | People can represent themselves legally |
| **Caveat Emptor** | Buyer beware, with proper disclosure |
| **Contributory Negligence** | User's failure to read disclaimers reduces claims |

---

## The PMERIT Promise

> *"PMERIT empowers you to handle matters yourself—with full transparency about what AI can and cannot do. We don't hide behind restrictions. We educate you, get your informed consent, and let you decide what's right for your situation."*

---

*Fool Filter Doctrine v1.0*
*Walk around fire, not through it.*
