# Scope Order System — Example Workflow

**Purpose:** A complete, real-world example of the Scope Order workflow in action.

---

## Scenario

You're building **TaskTracker**, a simple task management app. You want to add user authentication.

---

## Step 1: Create Empty Scope File

**Director Action:** Create the file `.claude/scopes/SCOPE_AUTH.md` with minimal content:

```markdown
# SCOPE: AUTH

## Status
- Created: 2025-01-15
- State: EMPTY
```

**Commit it:**
```bash
git add .claude/scopes/SCOPE_AUTH.md
git commit -m "feat: Create SCOPE_AUTH for authentication feature"
```

---

## Step 2: Audit Reality

**Director → Claude Code:**
```
AUDIT SCOPE: AUTH
```

**Claude Code Response:**

After examining the codebase, Claude Code populates the AUDIT_REPORT section:

```markdown
# SCOPE: AUTH

## Status
- Created: 2025-01-15
- State: AUDITED
- Audited: 2025-01-15

---

## AUDIT_REPORT

### Current Reality (2025-01-15)

**Existing Auth-Related Code:**
- None found — this is a new feature

**Database Status:**
- Using PostgreSQL via Neon
- No users table exists yet

**Frontend Status:**
- React app with React Router
- No login/signup pages exist
- No auth context or hooks

**Backend Status:**
- Express API running on port 3001
- No auth endpoints exist
- No session/JWT middleware

**Dependencies Available:**
- bcryptjs (installed but unused)
- No JWT library installed

**Recommendations:**
1. Need to add `jsonwebtoken` package
2. Need to create users table in database
3. Need auth context for React frontend

---

## HANDOFF_DOCUMENT
[To be filled by Claude Web]

---

## RESEARCH_FINDINGS
[To be filled by Claude Code after implementation]
```

---

## Step 3: Share with Claude Web

**Director Action:** Copy the AUDIT_REPORT section and share it with Claude Web.

**Director → Claude Web:**
```
Here's the auth audit from Claude Code:

[Paste AUDIT_REPORT content]

Let's brainstorm the auth system. I'm thinking:
- Email/password signup and login
- JWT tokens for API auth
- React context for frontend state
- Sessions stored in database

What do you think?
```

---

## Step 4: Brainstorm with Claude Web

**Claude Web Response:**

"Good foundation! Here are my recommendations:

**Authentication Flow:**
1. User signs up with email/password
2. Password hashed with bcrypt (already installed)
3. JWT issued on login, stored in httpOnly cookie
4. Frontend context tracks auth state

**Database Schema:**
```sql
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  email VARCHAR(255) UNIQUE NOT NULL,
  password_hash VARCHAR(255) NOT NULL,
  created_at TIMESTAMP DEFAULT NOW()
);

CREATE TABLE sessions (
  id SERIAL PRIMARY KEY,
  user_id INTEGER REFERENCES users(id),
  token VARCHAR(255) NOT NULL,
  expires_at TIMESTAMP NOT NULL
);
```

**API Endpoints:**
- POST /api/auth/signup
- POST /api/auth/login
- POST /api/auth/logout
- GET /api/auth/me

**Frontend Components:**
- LoginPage
- SignupPage
- AuthContext + useAuth hook
- ProtectedRoute wrapper

Should I write the full specification?"

**Director:** "Yes, please write the HANDOFF_DOCUMENT."

---

## Step 5: Claude Web Writes Specification

**Claude Web** updates the scope file with detailed specs:

```markdown
## HANDOFF_DOCUMENT

### Feature: User Authentication

**Priority:** P1 - Critical
**Estimated Scope:** Medium (2-3 sessions)

---

### Requirements

#### R1: Database Schema
Create users and sessions tables as specified in brainstorm.

#### R2: Backend Endpoints
| Endpoint | Method | Purpose |
|----------|--------|---------|
| /api/auth/signup | POST | Create new user |
| /api/auth/login | POST | Authenticate, return JWT |
| /api/auth/logout | POST | Invalidate session |
| /api/auth/me | GET | Get current user |

#### R3: Frontend Components
- `src/pages/LoginPage.jsx`
- `src/pages/SignupPage.jsx`
- `src/context/AuthContext.jsx`
- `src/hooks/useAuth.js`
- `src/components/ProtectedRoute.jsx`

#### R4: Security Requirements
- Passwords hashed with bcrypt (cost factor 12)
- JWT expires in 7 days
- httpOnly cookies for token storage
- CSRF protection on auth endpoints

---

### Implementation Order
1. Database schema migration
2. Backend auth endpoints
3. Frontend auth context
4. Login/Signup pages
5. ProtectedRoute integration

---

### Acceptance Criteria
- [ ] User can sign up with email/password
- [ ] User can log in and receive token
- [ ] User can log out
- [ ] Protected routes redirect to login
- [ ] Auth state persists on page refresh
```

**Director Action:** Copy this into the scope file and commit:
```bash
git add .claude/scopes/SCOPE_AUTH.md
git commit -m "feat: Add HANDOFF_DOCUMENT for auth feature"
```

---

## Step 6: Implement with Claude Code

**Director → Claude Code:**
```
SCOPE UPDATED: AUTH
```

**Claude Code reads the spec and responds:**

"I've reviewed the HANDOFF_DOCUMENT for AUTH. Here's my implementation plan:

**Phase 1: Database (This Session)**
1. Create migration for users table
2. Create migration for sessions table
3. Run migrations

**Phase 2: Backend (Next Session)**
1. Install jsonwebtoken
2. Create auth middleware
3. Implement 4 endpoints

**Phase 3: Frontend (Following Session)**
1. Create AuthContext
2. Create useAuth hook
3. Create pages and ProtectedRoute

**Recommendation:** I suggest adding rate limiting to the auth endpoints to prevent brute force attacks. This wasn't in the spec but is best practice.

Should I proceed with Phase 1, and should I add rate limiting?"

**Director:** "Yes to both."

**Claude Code implements Phase 1...**

---

## Step 7: Update Research Findings

After implementation, Claude Code updates the scope:

```markdown
## RESEARCH_FINDINGS

### Session 1 — 2025-01-15

**Completed:**
- [x] Created users table migration
- [x] Created sessions table migration
- [x] Ran migrations successfully

**Files Created:**
- `migrations/001_create_users.sql`
- `migrations/002_create_sessions.sql`

**Decisions Made:**
- Added `email_verified` boolean for future email verification
- Added index on `sessions.token` for faster lookups

**Next Session:**
- Install jsonwebtoken
- Create auth middleware
- Implement endpoints

---

### Session 2 — 2025-01-16

**Completed:**
- [x] Installed jsonwebtoken
- [x] Created auth middleware
- [x] Implemented all 4 endpoints
- [x] Added rate limiting (3 attempts per minute)

**Files Created:**
- `src/middleware/auth.js`
- `src/routes/auth.js`
- `src/utils/rateLimit.js`

**Decisions Made:**
- Used express-rate-limit for rate limiting
- Token stored in httpOnly cookie as planned

**Next Session:**
- Frontend components

---

### Session 3 — 2025-01-17

**Completed:**
- [x] Created AuthContext
- [x] Created useAuth hook
- [x] Created LoginPage and SignupPage
- [x] Created ProtectedRoute
- [x] All acceptance criteria passing

**Files Created:**
- `src/context/AuthContext.jsx`
- `src/hooks/useAuth.js`
- `src/pages/LoginPage.jsx`
- `src/pages/SignupPage.jsx`
- `src/components/ProtectedRoute.jsx`

**Feature Status:** COMPLETE
```

---

## Step 8: Report Back to Claude Web

**Director → Claude Web:**

"Auth feature is complete! Claude Code implemented it over 3 sessions.

Additional work:
- Added rate limiting (3 attempts/min)
- Added email_verified field for future use
- Added index on sessions.token

All acceptance criteria passing. Ready for review."

**Claude Web:** "Excellent! Let's update the MASTER_SCOPE to mark this complete and plan the next feature."

---

## Summary: The Complete Cycle

```
1. DIRECTOR: Created SCOPE_AUTH.md (empty)
2. CLAUDE CODE: "AUDIT SCOPE: AUTH" → populated AUDIT_REPORT
3. DIRECTOR → CLAUDE WEB: Shared audit, brainstormed requirements
4. CLAUDE WEB: Wrote HANDOFF_DOCUMENT with specifications
5. DIRECTOR → CLAUDE CODE: "SCOPE UPDATED: AUTH"
6. CLAUDE CODE: Reviewed, recommended rate limiting, implemented
7. CLAUDE CODE: Updated RESEARCH_FINDINGS per session
8. DIRECTOR → CLAUDE WEB: Shared completion status
```

---

## Key Takeaways

1. **Reality First** — The audit revealed bcrypt was installed but no JWT library
2. **Quality Review** — Claude Code recommended rate limiting (not in original spec)
3. **Session Continuity** — RESEARCH_FINDINGS preserved progress across 3 sessions
4. **Clear Communication** — Each role knew exactly what to do and when

---

*This is how Scope Order v2 works in practice.*
