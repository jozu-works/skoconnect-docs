# Jamaican Payment Gateway Comparison — SkoConnect (EdTech SaaS)

## TL;DR — Ranking for SaaS Suitability

| Rank | Gateway | Best For | Verdict |
|---|---|---|---|
| **1** | **First Atlantic Commerce (FAC)** | Local JMD + recurring primitives | 🟢 **Primary Pick** |
| **2** | **Stripe (via foreign entity)** | Best-in-class recurring/subscription | 🟡 **For USD/international** |
| **3** | **NCB Global Pay** | Fast settlement if banking with NCB | 🟡 Strong local fallback |
| **4** | **Wipay** | Fast onboarding, PayFac model | 🟡 Viable newcomer |
| **5** | **JMMB** | Traditional acquiring | 🔴 Dated API, limited SaaS fit |

---

## Detailed Comparison

### 1. JMMB (Jamaica Money Market Bank)

| Criterion | Details |
|---|---|
| **Merchant Account** | Required. Application with business docs, TRN. |
| **API Integration** | Basic REST API + hosted payment page. Developer experience is dated. |
| **Transaction Fees** | **2.5%–3.5%** per txn + possible monthly merchant fee (~JMD $3,000–5,000). |
| **Settlement** | **T+2 to T+3** business days. |
| **Recurring Billing** | **No native support.** Token-on-file possible but entirely DIY. |
| **Incorporation Required** | **Yes** — Jamaican business registration. |
| **SaaS Readiness** | ⭐⭐/5 |

### 2. NCB Global Pay (National Commercial Bank)

| Criterion | Details |
|---|---|
| **Merchant Account** | Required via NCB merchant acquiring division. |
| **API Integration** | Hosted checkout + API. Powered by **Fiserv/First Data** — more modern than JMMB. |
| **Transaction Fees** | **2.5%–3.2%** per txn. Volume discounts negotiable. |
| **Settlement** | **T+1 to T+2** (fastest if merchant banks with NCB). |
| **Recurring Billing** | **Partial.** Tokenization via Fiserv backend. Subscription logic is on you. |
| **Incorporation Required** | **Yes** — Jamaican business + NCB business account. |
| **SaaS Readiness** | ⭐⭐⭐/5 |

### 3. First Atlantic Commerce (FAC) — 🟢 TOP PICK

| Criterion | Details |
|---|---|
| **Merchant Account** | Required — FAC partners with local acquirers (JMMB, NCB). |
| **API Integration** | **Modern REST API.** TokenEx tokenization, 3D Secure 2.0, webhooks, AVS. |
| **Transaction Fees** | **2.5%–3.0%** + JMD $5–10/txn (negotiable). |
| **Settlement** | **T+1 to T+2** depending on acquiring bank partner. |
| **Recurring Billing** | **✅ Strong primitives.** Tokenized card-on-file, CIT/MIT transaction types. |
| **Incorporation Required** | **Yes** (JA or offshore — FAC supports BVI/Cayman entities too). |
| **SaaS Readiness** | ⭐⭐⭐⭐/5 |

### 4. Stripe (via Foreign Entity) — Best Recurring, Indirect

| Criterion | Details |
|---|---|
| **Merchant Account** | **Not needed** — Stripe is merchant of record. |
| **API Integration** | **World-class.** SDKs for everything, Stripe.js, Elements, webhooks. |
| **Transaction Fees** | **2.9% + $0.30 USD** per txn. FX conversion adds cost for JMD cardholders. |
| **Settlement** | **T+2** automatic. |
| **Recurring Billing** | **✅✅ Gold standard.** Full subscription engine. |
| **Incorporation Required** | **Not in Jamaica** — requires foreign entity (US LLC via Stripe Atlas ~$500). |
| **SaaS Readiness** | ⭐⭐⭐⭐⭐/5 — **But:** local-issued cards may face cross-border issues. |

---

## Recommendation: Hybrid Approach

| Layer | Gateway | Rationale |
|---|---|---|
| **Local JMD payments** | **FAC** | Caribbean-native, JMD, tokenization, 3DS2 |
| **International USD** | **Stripe** (US LLC) | Full subscription engine, best DX |
| **Billing abstraction** | Custom layer in SkoConnect | Routes to FAC or Stripe based on currency |

### Action Items (Post-Incorporation)
1. Contact FAC — Request EdTech SaaS merchant onboarding package
2. Evaluate Stripe Atlas — US LLC incorporation (~$500, 1–2 weeks)
3. Design billing abstraction layer in SkoConnect
4. Survey target schools — Card vs bank-transfer preference
