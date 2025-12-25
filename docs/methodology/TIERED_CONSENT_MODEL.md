# Tiered Consent Model

**Version:** 1.0
**Created:** December 2025
**Origin:** PMERIT Brainstorm Session
**Purpose:** Risk mitigation for AI-powered professional service products

---

## Philosophy

> "There's no perfection in life, but we walk around fire rather than walking through it. Just because something doesn't work for one person doesn't mean it will not work for others."

Absolute prohibition is paternalistic and excludes capable people who can make informed decisions. The legal system itself recognizes this through:
- Informed consent
- Assumption of risk
- Pro se representation (representing yourself)

---

## The Three Tiers

```
+---------------------------------------------------------------+
|  TIER 1: OPEN ACCESS                                          |
|  General information, templates, education                    |
|  No special consent needed                                    |
+---------------------------------------------------------------+
|  TIER 2: INFORMED CONSENT ZONE                                |
|  Edge services with full disclosure                           |
|  User acknowledges limitations + signs waiver                 |
|  "I understand this is not legal/tax/professional advice"     |
+---------------------------------------------------------------+
|  TIER 3: HARD BOUNDARY                                        |
|  Truly prohibited (e.g., court representation)                |
|  System blocks regardless of consent                          |
+---------------------------------------------------------------+
```

---

## Legal Basis for Tier 2

| Concept | Application |
|---------|-------------|
| Informed Consent | User understands risks, proceeds anyway |
| Assumption of Risk | User accepts responsibility for outcome |
| Waiver of Liability | Contractual release of claims |
| Pro Se Doctrine | People can represent themselves legally |
| Caveat Emptor | Buyer beware, with proper disclosure |

---

## Tier Classification by Service Type

### Tax Services Example

| Service | Without Consent | With Signed Consent |
|---------|-----------------|---------------------|
| "What are the 1040 requirements?" | Tier 1 | Tier 1 |
| "Help me fill out Schedule C" | Tier 2 | Tier 2 |
| "What deductions should I take?" | Blocked | Tier 2 |
| "File my taxes for me" | Tier 3 | Tier 3 |
| "Represent me in an audit" | Tier 3 | Tier 3 |

### Legal Services Example

| Service | Without Consent | With Signed Consent |
|---------|-----------------|---------------------|
| "What is an LLC?" | Tier 1 | Tier 1 |
| "Help me understand this contract" | Tier 2 | Tier 2 |
| "What questions should I ask an attorney?" | Tier 2 | Tier 2 |
| "Draft a custom contract for my situation" | Blocked | Tier 2 (with heavy disclaimer) |
| "Represent me in court" | Tier 3 | Tier 3 |
| "File documents on my behalf" | Tier 3 | Tier 3 |

---

## Tier 2: Signature Gate Implementation

```
+---------------------------------------------------------------+
|  ACKNOWLEDGMENT & CONSENT                                     |
+---------------------------------------------------------------+
|                                                               |
|  You are requesting assistance that goes beyond general       |
|  information. Please understand:                              |
|                                                               |
|  [ ] This tool is NOT a licensed professional                 |
|  [ ] This is NOT professional advice for your situation       |
|  [ ] Outcomes may vary based on your circumstances            |
|  [ ] You are responsible for verifying accuracy               |
|  [ ] Complex matters should involve a licensed professional   |
|                                                               |
|  By proceeding, you acknowledge that you:                     |
|  [ ] Have read and understood these limitations               |
|  [ ] Accept full responsibility for how you use this output   |
|  [ ] Waive claims against PMERIT for reliance on this tool    |
|                                                               |
|  Signature: ____________________  Date: __________            |
|                                                               |
|  [I UNDERSTAND & ACCEPT]     [CANCEL]                         |
|                                                               |
+---------------------------------------------------------------+
```

---

## Tier 3: Hard Boundaries (Never Allow)

Even with consent, these create unacceptable risk:

- Representing user in actual legal proceedings
- Filing documents on user's behalf with courts/agencies
- Claiming to be a licensed professional
- Guaranteeing outcomes
- Advising on active criminal matters
- Making medical diagnoses
- Providing specific investment advice (fiduciary level)

---

## Strengthening Waivers

To make user signatures legally meaningful:

| Requirement | Purpose |
|-------------|---------|
| Timestamped record | Store signature + IP + timestamp |
| Plain language | No legalese hiding the meaning |
| Specific acknowledgments | Checkbox each risk, not blanket acceptance |
| Cooling off option | "Are you sure?" confirmation |
| Re-consent for major actions | One signature doesn't cover everything |
| Downloadable copy | User can save their signed acknowledgment |

---

## Risk Allocation

| Party | Responsibility |
|-------|----------------|
| PMERIT | Accurate information, clear disclaimers, documented consent |
| User | Reading disclaimers, making informed choice, verifying outputs |
| System | Blocking Tier 3 requests, logging consent |

---

## Product Messaging

This becomes a **feature**, not a limitation:

> "PMERIT empowers you to handle professional matters yourself—with full transparency about what AI can and cannot do. We don't hide behind restrictions. We educate you, get your informed consent, and let you decide what's right for your situation."

---

## The "Fool Filter"

The consent process itself filters users:

```
Sophisticated User              Fool
       |                          |
       v                          v
  Reads disclaimer           Clicks through blindly
       |                          |
       v                          v
  Makes informed             Ignores warnings
  decision                        |
       |                          v
       v                   Higher likelihood
  Benefits from            of misuse/harm
  the tool                        |
                                  v
                          BUT: Signed waiver
                          limits your liability
```

---

## Implementation in Products

### Guardrail Architecture

```
+---------------------------------------------------------------+
|                    USER REQUEST                                |
+---------------------------------------------------------------+
                          |
                          v
+---------------------------------------------------------------+
|              CLASSIFICATION LAYER                              |
|  AI analyzes request against permitted/prohibited list         |
+---------------------------------------------------------------+
                          |
          +---------------+---------------+
          v               v               v
     TIER 1          TIER 2          TIER 3
     (Open)          (Consent)       (Block)
          |               |               |
          v               v               v
     Process &       Show Gate &      BLOCK
     Respond         Get Signature    + Educate
```

### Positioning Language

**Use:**
- "Legal Information Guide"
- "Document Preparation Assistant"
- "Tax Learning Companion"
- "Legal Literacy Tool"

**Avoid:**
- "AI Lawyer"
- "Robot Attorney"
- "Tax Advisor"
- "Legal Counsel"

---

## References

- DoNotPay FTC Fine: $193,000 for marketing as "robot lawyer"
- Origin: Chat_brainstorm_products.txt
- Related: GUARDRAIL_ARCHITECTURE in Chat-Histories

---

*Tiered Consent Model v1.0 - Walk Around Fire, Not Through It*
