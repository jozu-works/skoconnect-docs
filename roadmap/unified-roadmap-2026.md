# SkoConnect Unified Roadmap — Realigned May 2026

## Timeline Context
- **Current school year:** ~8 weeks remaining (ends ~July 2026)
- **Beta period:** Extended through September 2026 (start of new school year)
- **Target:** 3-4 private preparatory schools for initial deployment
- **Blocker:** Company incorporation (blocks payment gateway + Play Store merchant account, does NOT block development)

## Target Schools
- 1 school already engaged
- Prospecting: Portmore Missionary Preparatory, Bright Beginnings Learning Center, El Instituto, Belair
- All private preparatory schools in Jamaica

---

## Project State Assessment (May 5, 2026)

### SkoConnect Mobile App (SkoConnect-Mobile)
**Version:** 1.0.6+7 | **Application ID:** com.skoconnect.skoconnect
**Stack:** Flutter 3.41, Dart 3.11, Firebase (Auth, Firestore, Messaging, Storage, Analytics, Crashlytics, Performance), Riverpod, GoRouter

**Screens Built (19):**
- ✅ Login, Sign-in Help
- ✅ Home, Main App Shell
- ✅ Notice Screen (structured notices)
- ✅ Emergency Screen (broadcast)
- ✅ Forms Screen (digital forms + admin form templates)
- ✅ Events/Calendar
- ✅ Groups Screen
- ✅ Routine Screen
- ✅ Chat Screen
- ✅ Profile Settings, Notification Settings, Language Settings, Privacy/Security
- ✅ About, Help & Support
- ✅ Share Intake (compose screen)

**Services Built (11):**
- ✅ API Client (wired to all Cloud Functions)
- ✅ Analytics Service
- ✅ Biometric Service
- ✅ Notification Service (FCM + local notifications)
- ✅ Session Manager, Token Manager
- ✅ Share Intake (staging, intent bridge, failure UX mapper)
- ✅ Notice Read Service
- ✅ Group Activity Seen Service
- ✅ Notification Preferences

### SkoConnect Cloud Functions
**20 handlers deployed:**
acknowledgments, analytics, auth, emergency, enrollment, events, form-notifications, form-pending, form-reminders, forms, form-submissions, form-templates, groups, health, members, notifications, provision, relationships, request-access

### SkoConnect Admin Web
- ✅ Next.js static export deployed
- ✅ Screens: login, enrollment, events, notices, emergency, forms, form-templates, groups, users, super-admin, analytics, settings, security, privacy, about, reset-password, grade-promotion, EMIS export

### SkoConnect Landing Page
- ✅ Live at skoconnect.com (Next.js 14 + Firebase Hosting)
- ✅ Request Access modal form
- ✅ Mobile responsive
- ✅ Trust messaging refined

---

## Realigned Milestones

### Assessment: Milestone 0 (Setup & Foundation) — COMPLETE ✅
The original Milestone 0 called for: Firebase project, schema, shared types, CI/CD.
All exist and are functional. 20 Cloud Functions deployed, mobile app v1.0.6+7, admin web live, landing page live.

### Milestone 1: Student-Parent Onboarding — MOSTLY COMPLETE ✅
- ✅ Enrollment flow (admin web + mobile)
- ✅ Auth system (Firebase Auth with roles)
- ✅ User management (super-admin, admin screens)
- ✅ Provision service
- ✅ Request access flow
- 🔲 CSV bulk import (verify status)
- 🔲 Parent self-registration portal (verify status)

### Milestone 2: Notice System — COMPLETE ✅
- ✅ Notice creation and delivery
- ✅ Notice read receipts
- ✅ Group targeting
- 🔲 Grade-level targeting (Enhancement — deferred to polish phase)

### Milestone 3: Calendar + Auto-Notifications — COMPLETE ✅
- ✅ Events screen
- ✅ FCM notifications
- ✅ Notification preferences
- ✅ Scheduled notifications via form-reminders, form-notifications
- ✅ Routine screen

### Milestone 4: Emergency Broadcast — COMPLETE ✅
- ✅ Emergency screen
- ✅ Acknowledgments handler
- ✅ Broadcast delivery via FCM

### Milestone 5: Digital Forms — COMPLETE ✅
- ✅ Forms screen
- ✅ Form templates (admin)
- ✅ Form submissions
- ✅ Form notifications and reminders
- ✅ Pending forms tracking

### Milestone 6: Polish, Testing, Beta Launch — IN PROGRESS 🔲
This is where all remaining work sits:

**6a. Play Store Readiness**
- 🔲 Signing keystore creation
- 🔲 Play Store developer account setup (requires incorporation)
- 🔲 Store listing (screenshots, description, content rating)
- 🔲 App signing configuration
- 🔲 Production build testing

**6b. Billing & Payment Integration**
- 🔲 Payment gateway selection (FAC recommended, see research doc)
- 🔲 Business incorporation (Dre's blocker)
- 🔲 Merchant account application
- 🔲 Billing abstraction layer in app
- 🔲 Subscription plan definition
- 🔲 Payment UI integration

**6c. Beta Deployment (Sep 2026 target)**
- 🔲 Beta test plan (3-4 schools)
- 🔲 Onboarding documentation for school admins
- 🔲 Feedback collection mechanism
- 🔲 Support pipeline (help desk or in-app)
- 🔲 Analytics dashboards for Dre to monitor usage

**6d. V1 Enhancements (from CLAUDE.md)**
- 🔲 Notice: Grade-level targeting
- 🔲 Notice: Read receipts dashboard
- 🔲 Admin: Role visibility UI
- 🔲 Admin: User creation audit dashboard
- 🔲 Admin: Suspicious pattern detection

---

## Sprint Plan: Autonomous Execution

### Sprint 1 (Week of May 5) — Current
**Priority: CradleConnect MVP (summer deadline)**
- CradleConnect: Cloud Functions (8 backend functions) — unblocks all mobile testing
- SkoConnect: Play Store prep (keystore, build config, listing assets)

### Sprint 2 (Week of May 12)
- CradleConnect: Tier 1 mobile features (Activities Log, Incident Reports, Notes, Photos)
- SkoConnect: Beta test plan + admin onboarding docs

### Sprint 3 (Week of May 19)
- CradleConnect: Daily Timetable + remaining Tier 1
- CradleConnect: Internal beta prep (wife's daycare)
- SkoConnect: V1 enhancements start (grade-level targeting, read receipts)

### Sprint 4 (Week of May 26)
- CradleConnect: **BETA RELEASE** to wife's daycare
- SkoConnect: V1 enhancements continue
- Business Dev: Pitch deck draft + competitive analysis

### Sprint 5-8 (June)
- CradleConnect: Iterate on beta feedback, Tier 2 features
- SkoConnect: Billing integration (pending incorporation), Play Store submission
- Business Dev: Lead engagement with target schools

### Sprint 9-12 (July-August)
- SkoConnect: Beta deployment to 3-4 schools
- CradleConnect: Public beta / Play Store
- Business Dev: Sales pipeline, pricing finalization

### September 2026
- SkoConnect: Full launch (new school year)
- Payment billing goes live (if incorporation complete)
- Customer success for beta schools

---

## Business Development Pipeline

### Lead Tracker
| School | Status | Contact | Next Action |
|--------|--------|---------|-------------|
| [School 1 - already engaged] | Engaged | TBD | Follow up, schedule demo |
| Portmore Missionary Preparatory | Prospect | TBD | Research, find decision maker |
| Bright Beginnings Learning Center | Prospect | TBD | Research, find decision maker |
| El Instituto | Prospect | TBD | Research, find decision maker |
| Belair | Prospect | TBD | Research, find decision maker |

### Deliverables Needed
- [ ] Pitch deck (school admin version)
- [ ] Feature comparison vs competitors
- [ ] Pricing proposal (per-student monthly? per-school flat rate?)
- [ ] Demo video or walkthrough
- [ ] Case study template (for post-beta)

---

## Payment Gateway Decision (Pending Incorporation)

**Recommendation:** FAC (First Atlantic Commerce) for JMD local payments.
**Fallback:** NCB Global Pay (if already banking with NCB).
**International:** Stripe via US LLC (Stripe Atlas ~$500).

Full comparison: `/home/atlas/skoconnect-docs/research/jamaica-payment-gateways.md`

---

## Escalation Matrix

| Decision | Owner | Examples |
|----------|-------|---------|
| Technical approach | Atlas + Forge | Library choice, architecture patterns |
| Feature scope | Atlas (from GEO input) | What's in/out of beta |
| Pricing | **Dre** | Per-student vs per-school, amount |
| Client relationships | **Dre** | School names, meetings, partnerships |
| Incorporation/legal | **Dre** | Business registration, bank accounts |
| Launch timing | **Dre** | When to go public, which schools first |
| Content/branding | **Dre** | Marketing copy, positioning |

---

*Last updated: May 5, 2026 by Atlas*
*Next review: Sprint 2 kickoff (May 12, 2026)*
