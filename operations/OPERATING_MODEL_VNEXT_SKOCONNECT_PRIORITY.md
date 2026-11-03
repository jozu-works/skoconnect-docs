# SkoConnect Operating Model vNext (SkoConnect-Priority Reweight)

**Version:** 1.0  
**Owner:** Atlas (Orchestration)  
**Decision Authority:** Dre (Founder)  
**Effective Date:** 2026-05-09  

## 1) Purpose
Define the full lifecycle operating model after portfolio reweight: **SkoConnect launch first**, **BizDev strategy protected**, **CradleConnect maintenance-only**.

## 2) Strategic Policy (Active)
- Capacity Weights:
  - **50%** SkoConnect launch-critical
  - **30%** Business strategy / lead-marketing engine
  - **20%** CradleConnect maintenance (P0/P1 only)
- This policy remains active until replaced by Dre.

## 3) Governance Invariants (Never Relaxed)
1. Card-first rule: no execution without card.
2. Kanban middleware enforcement for all pipeline work.
3. Role boundaries:
   - Atlas = orchestration + governance + infra enablement
   - GEO = product definition
   - SAGE = validation and quality authority
   - FORGE = implementation
   - SCOUT = research
   - LEXI = messaging/GTM
4. Release evidence gate before done/shipped.
5. Product isolation: each task must include PRODUCT + REPO.

## 4) End-to-End Lifecycle
### Stage A — Intake
- Capture on correct board/domain.
- Minimum metadata: Objective, ACs, Priority, Owner, Risk, Dependencies.
- Classification tags: Product, Domain, Priority, Deadline risk, Unblock impact.

### Stage B — Portfolio Prioritization
- Atlas computes cross-board score:
  - launch risk,
  - unblock leverage,
  - business leverage,
  - Dre directive weight.
- Card enters weighted queue.

### Stage C — Sprint Admission
- WIP budgets:
  - SkoConnect: 2 active chains
  - BizDev: 1 active chain
  - CradleConnect: 1 maintenance chain
- Admission requires dependencies and gate readiness.

### Stage D — Execution
- Product work chain: GEO -> SAGE -> FORGE.
- Strategy work chain: SCOUT -> SAGE -> LEXI.
- Atlas enforces sequencing and exceptions.

### Stage E — Validation + Evidence
- AC verification required.
- Build/analyze/test evidence attached.
- Risk and rollback notes attached where relevant.

### Stage F — Documentation Sync
- Update federated docs by domain owner.
- Stamp metadata: owner, last-updated, cadence, upstream/downstream links.

### Stage G — Review + Rebalance
- Daily operational digest (portfolio-level).
- Weekly sprint review and policy retune.

## 5) Escalation Matrix
- Dre-only: pricing, client commitments, launch/public timing, legal commitments.
- Atlas-level: cross-board arbitration, WIP reallocation, exception routing.
- SAGE-level: acceptance/readiness quality, gate challenges.

## 6) Multi-Board Coordination Rules
1. One board per product/domain source of work.
2. One task = one product.
3. Cross-product dependencies are link-based handshakes, not mixed implementation.
4. Finish in-flight work unless Dre directs emergency interruption.
5. Queue reorder applies to not-yet-started work first.

## 7) Policy Pack (Operational)
### P-01 Portfolio Reweight Policy
Defines active weights, WIP caps, and rebalance trigger criteria.

### P-02 Product Isolation Policy
Mandates PRODUCT + REPO in every executable task body.

### P-03 Release Evidence Policy
No done/shipped state without verifiable artifacts.

### P-04 Documentation Freshness Policy
Each critical doc has owner, cadence, SLA, stale threshold.

### P-05 Business Strategy Continuity Policy
BizDev lane keeps protected throughput (never treated as overflow).

## 8) KPIs
- Throughput by lane (weekly completed chains)
- On-time delivery ratio
- Blocked-task aging
- Gate pass rate first attempt
- Documentation freshness score
- Strategic output cadence (GTM updates, lead-engine artifacts)

## 9) Implementation Checklist
- [ ] Set active policy weights in operating dashboard/notes
- [ ] Enforce WIP caps in dispatch logic
- [ ] Ensure all new tasks carry PRODUCT + REPO
- [ ] Publish daily digest template
- [ ] Publish weekly rebalance template
- [ ] Attach this doc to governance card and Drive folder
