# System Wiremap & Documentation Federation Framework

**Version:** 1.0  
**Owner:** Atlas  
**Effective Date:** 2026-05-09

## 1) Logical System Wiremap

```text
Dre (Strategy / Final Business Decisions)
   |
Atlas (Portfolio Orchestrator + Governance Control Plane)
   |   | \__ Trello Boards (Human visibility & planning)
   |      - SkoConnect board/domain lists
   |      - CradleConnect board/domain lists
   |
   \__ Hermes Kanban (Machine-enforced execution graph)
          |-- GEO  (specification)
          |-- SAGE (validation / quality)
          |-- FORGE (implementation)
          |-- SCOUT (research)
          |-- LEXI (GTM/messaging)

Execution Outputs -> Repos/Artifacts -> Evidence Gate -> Board Updates
                                    -> Federated Documentation Layer
```

## 2) Control Planes
### Human Plane
- Trello boards, card metadata, sprint visibility, stakeholder reviews.

### Machine Plane
- Kanban dependencies, status transitions, blocker handling, retry/circuit controls.

### Knowledge Plane
- Federated docs on Google Drive + local source mirror.

## 3) Federated Documentation Model
Domains and owning lanes:
1. Infrastructure (Atlas/FORGE)
2. Operating Model & Governance (Atlas/SAGE)
3. Product Delivery (GEO/FORGE)
4. Business Strategy + Lead/Marketing (SAGE/LEXI/SCOUT)

## 4) Doc Contract (Required Metadata)
Every policy/runbook/strategy doc must include:
- Document ID
- Owner
- Decision Authority
- Last Updated
- Review Cadence (weekly/biweekly/monthly)
- Freshness SLA (e.g., <=14 days)
- Upstream dependencies
- Downstream consumers
- Status: Draft | Active | Superseded | Archived

## 5) Governance Artifacts Framework
### Artifact Families
- **Policy**: rules and constraints
- **Runbook**: executable process steps
- **Standard**: format/schema requirements
- **Decision Log**: why a strategic path changed
- **Evidence Pack**: release or validation proof

### Minimum Required Artifacts (vNext)
1. Operating Model vNext (policy baseline)
2. Portfolio Reweight Policy
3. Product Isolation Standard
4. Release Evidence Standard
5. Documentation Freshness Standard
6. Lead/Marketing Operating Cadence Runbook
7. Weekly Portfolio Review Template

## 6) Data Flow (Lifecycle)
1. Intake captured on board
2. Classified in portfolio queue
3. Executed through Kanban graph
4. Evidence captured from implementation
5. Evidence + decisions sync to docs
6. Audit checks freshness/compliance
7. Weekly review consumes dashboard + docs

## 7) Audits and Controls
### Daily Controls
- Blocker aging report
- WIP cap compliance
- Cross-product contamination check

### Weekly Controls
- Policy compliance scan
- Documentation freshness scan
- Lane throughput and slip analysis
- Strategic drift review against Dre priorities

## 8) Google Drive Structure (Operational)
Recommended canonical location under SkoConnect Drive root:
- `Operations/Governance/`
  - `Operating Model/`
  - `Policy Library/`
  - `Runbooks/`
  - `Decision Logs/`
  - `Weekly Portfolio Reviews/`
- `Business/Strategy/`
  - `GTM/`
  - `Lead Engine/`
  - `Campaign Ops/`

## 9) Templates (Short)
### Weekly Portfolio Review
- Shipped this week
- In progress by lane
- Blocked + owner + ETA
- Risk register delta
- Decisions needed from Dre
- Next-week reweight recommendation

### Documentation Freshness Report
- Doc name
- Owner
- Last update age
- SLA breach (Y/N)
- Action required

## 10) Adoption Plan
- Week 1: establish folder structure + publish baseline docs
- Week 2: wire weekly review + freshness audit
- Week 3: enforce doc contract on all new strategic docs
- Week 4: retrofitted critical legacy docs to contract
