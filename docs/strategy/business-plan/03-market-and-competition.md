# Section 3: Market Size & Competition

*Business plan section 3 — Project Green*

---

## 1. Market Size

### US Accounting Industry Structure

The US accounting industry comprises **80,000+ firms**. The vast majority are small to mid-sized:

| Segment | Firms | Employees per Firm | Annual Revenue per Firm | Tech Spend (est.) |
|---------|-------|--------------------|-------------------------|-------------------|
| Large (Top 100) | ~100 | 500–50,000+ | $100M–$20B+ | $5M–$500M+ |
| Mid-market | ~2,000 | 50–500 | $5M–$100M | $250K–$5M |
| **Small (target)** | **~78,000** | **2–50** | **$200K–$5M** | **$5K–$100K** |

Total industry revenue is on the order of **$145B+** (US). The AI accounting automation segment is multi-billion today and projected to grow at roughly **40% CAGR** over the next decade. Adoption in accounting jumped from single digits to over 40% in a single year; 77% of firms plan to increase AI investment. The market is in early-stage transformation with real budget and intent to spend.

### TAM / SAM / SOM

Two complementary views:

**Spend potential (all firms that could use AI operational intelligence):**

| Metric | Definition | Value |
|--------|------------|-------|
| **TAM** | All US accounting firms × reasonable annual AI/operational-intelligence spend | ~$8B/year (80,000 firms × ~$100K potential spend) |
| **SAM** | 10–50 person firms on cloud GL (QBO/Xero), open to AI, reachable | ~$2B/year (~20,000 firms × ~$100K) |
| **SOM (Year 1–2)** | Target metros, warm-networkable, active capacity/knowledge pain | ~$5M/year (e.g. 50 firms × ~$100K) |

**Our revenue opportunity at target ACV (~$36K–$48K):**

| Metric | Firms | Blended ACV | Annual Value |
|--------|-------|-------------|-------------|
| **TAM** | ~15,000 (mid-tier, our fit) | ~$36K | ~$540M/year |
| **SAM** | ~6,000 (cloud, AI-open, reachable) | ~$38K | ~$228M/year |
| **SOM (Year 3)** | 50–100 | ~$40K | $2M–$4M/year |
| **SOM (Year 5)** | 200–500 | ~$44K | $8.8M–$22M/year |

The takeaway: even 50 firms at target ACV is a meaningful early-stage business; the market is deep enough to support **$100M+ ARR** at scale. We do not need to win the whole market to build a large, defensible company.

### Target Segment (ICP)

We focus first on **10–50 person accounting firms** that:

- Do both **tax and bookkeeping** (year-round workflow, not tax-only).
- Use **QuickBooks Online** (or equivalent cloud GL) so we can integrate without replacing systems.
- Are in **reachable metros** for founder-led sales and support.
- Have a **managing partner who feels** capacity constraints, knowledge loss, or partner bottleneck.

This segment is large enough to feel the pain of the structural crisis (Section 1), has budget for a solution (IT and managed services spend in the $5K–$100K range), and is underserved by both enterprise vendors (who focus up-market) and point-solution startups (who automate one workflow, not the whole firm). Sub-segments such as **outsourced/virtual firms** (cloud-native, tech-forward, margin pressure) may prove especially receptive and are a natural extension of the same ICP.

---

## 2. Market Dynamics (Forces That Shape Demand)

Five forces reinforce demand for what we build:

1. **PE consolidation** — PE is rolling up accounting firms; one-third of the top 30 US firms may be PE-backed. Portfolio firms need operational clarity, standardization, and margin data. When rates normalize and exits ramp, firms with operational intelligence command premium multiples. The Process Twin (Archetype 3) is the PE product; PE operating partners are a future channel.
2. **CPA workforce crisis** — ~75% of CPAs at retirement age; firms cannot hire their way out. The Staff Copilot (Archetype 1) directly addresses knowledge capture and partner interruption.
3. **AI adoption inflection** — Adoption jumped 4.5× in one year; 82% of early adopters report positive ROI in year one. The window is open; firms are actively evaluating AI.
4. **Big Four investment** — $9.5B committed to AI; they build for their own practices and large clients, not for the 78,000 smaller firms. They create awareness and demand without serving this segment.
5. **Rising client expectations** — Clients expect faster, clearer answers (“Why did my profit drop?”). Advisory is growing faster than compliance. The Explanation Engine (Archetype 2) and a more responsive firm (enabled by Archetype 1) meet this demand.

---

## 3. Competitive Landscape

### Competitive Matrix

| Category | Examples | Approach | Threat to Project Green |
|----------|----------|----------|--------------------------|
| **Enterprise ERP** | Oracle Fusion, SAP Joule, Dynamics 365 | AI on top of large ERP | **Low** — wrong segment, wrong price point |
| **Mid-market ERP** | Acumatica, NetSuite | AI features in cloud ERP | **Low–Medium** — closer to our segment but ERP-centric, not overlay |
| **SMB ERP** | Business Central, Odoo | Copilot-style features for small business | **Medium** — right segment, but generic rather than firm-specific |
| **AI accounting startups** | Truewind, Vic.ai, Numeric, Gravis AI | Point solutions or vertical AI | **Medium–High** — closest competitors; narrow scope or different deployment model |
| **Big Four** | Deloitte, PwC, KPMG, EY | Proprietary tools, consulting | **Low** — different segment; they validate the market and don’t productize for SMB |
| **Horizontal AI** | ChatGPT, Claude, Gemini | General-purpose assistants | **Medium** — firms may try these first; we win when the question requires firm-specific data (e.g. “What was Client X’s AR balance?”) |

### Startup Competitors (Closest Comparables)

| Company | Focus | Our differentiation |
|---------|--------|----------------------|
| **Truewind** | AI bookkeeping automation | Point solution for bookkeeping; we span firm-level financials, client-level, documents, and (long-term) process. |
| **Vic.ai** | Accounts payable automation | AP-specific; we model the entire firm and answer cross-system questions. |
| **Numeric** | Month-end close acceleration | Close-specific; we address the full operational lifecycle and firm knowledge. |
| **Gravis AI** | AI ERP for service businesses | Closest to our vision; they position as ERP replacement. We are overlay—connect to existing systems (QBO, Xero, etc.) and do not require migration. |

### Where Project Green Wins

| Dimension | Typical competitors | Project Green |
|-----------|---------------------|---------------|
| **Data scope** | Single system or one workflow | All firm systems aggregated in a lakehouse; one query can span GL, payroll, documents. |
| **Agent model** | Single copilot or task-specific bot | Multi-agent orchestration with domain specialists (firm, client, document) and routing. |
| **Deployment** | Replace your software or stay inside their app | Overlay on whatever the firm already uses; no rip-and-replace. |
| **User model** | One interface for everyone | Architecture supports role-aware routing and responses (partner vs. associate vs. client). |
| **Long-term value** | Task automation (“do this faster”) | Operational intelligence (“understand your entire firm”); data accumulates and switching cost grows. |

**What we are not:** We are not an ERP. We are not a general-purpose AI. We win when the question requires **live, firm-specific data** or **firm-specific knowledge**—the moment a user asks “What was account 1000’s balance last month?” or “What’s our policy on X?” using their data, generic AI and single-workflow tools fail. That gap is the core of our positioning.

---

## 4. Competitive Moat

What makes Project Green defensible over time:

1. **Firm-specific data accumulation** — Every day the product runs, it gets better at that firm’s terminology, questions, and processes. Migrating to a competitor means losing that accumulated intelligence. Vertical SaaS switching costs for mid-market customers are often in the hundreds of thousands of dollars; we build the same dynamic.
2. **Cross-firm network effects** — With anonymization, we can offer benchmarks: “Firms like yours typically close in X days.” Each new firm improves the value for every existing firm. The first 10–20 firms don’t get much here; at 50+ firms, benchmarking becomes a real moat.
3. **Integration depth** — Deep integrations to QuickBooks, Xero, Gusto, ADP, ProConnect, and document stores are expensive to build and maintain. New entrants must replicate that connectivity.
4. **Services relationship** — The “we build your firm’s AI twin” wrapper creates trust and a human relationship. Relationship-based switching cost compounds with data-based switching cost.
5. **PE channel** — If PE operating partners recommend us to portfolio firms, we get a distribution channel that scales with PE activity: each new acquisition is a potential deployment.

---

## 5. Expansion Markets (Later)

The same architecture—lakehouse, multi-agent orchestration, RAG, overlay deployment—applies to other knowledge-intensive professional service firms. Not part of the initial plan but relevant to long-term TAM:

| Market | Size / growth | Fit |
|--------|----------------|-----|
| Law firms (small) | $4B AI legal tech, ~31% CAGR | High — same knowledge-capture and multi-system pattern |
| Healthcare practices | $36B AI medical billing by 2034 | Medium–high — alpha customer can validate |
| Fractional CFO / FAO | $55B market, ~8% CAGR | Very high — identical “firm data + documents” architecture |
| Financial advisory (RIAs) | ~15,000 firms | Medium — similar client-serving and data pattern |

We do not pursue these before proving the model in accounting. Vertical expansion is a Phase 4+ option once the Process Twin and PE channel are in play.

---

## 6. Timing Window (Recap)

The market window is open but finite (see also Section 1):

- **2025–2026:** Adoption inflection. Firms are evaluating AI; early movers can establish data moats and switching costs.
- **2027–2028:** Consolidation. Incumbents (e.g. Intuit, Microsoft) will ship more capable AI; winners will be those already in production with paying customers.
- **2029+:** Mature market. Late entrants face entrenched competitors with deep integration and accumulated data.

We must have a **working product and paying customers by end of 2026** and be **scaling by 2027** to capture the window. Our first alpha customer (February 2026) is the first step; the next is delivery, conversion, and replication.

---

## Summary

- **Market size:** 80,000+ US accounting firms; ~$8B TAM (spend potential), ~$540M TAM at our ACV; SAM in the hundreds of millions; SOM Year 1–2 in the single-digit millions (tens of firms). Market is large enough for $100M+ ARR at scale.
- **Target segment:** 10–50 person firms, tax + bookkeeping, cloud GL (QBO), reachable, managing partner who feels capacity/knowledge pain. Underserved by both enterprise and point-solution startups.
- **Competition:** Enterprise and mid-market ERP (low threat); AI startups (medium–high, narrow scope or ERP-replacement); Big Four (low, validate demand); horizontal AI (medium—we win on firm-specific data and knowledge).
- **Moat:** Firm-specific data accumulation, cross-firm benchmarking, integration depth, services relationship, PE channel potential.
- **Timing:** Capture the adoption window with product and paying customers by end of 2026; scale in 2027 or cede advantage to incumbents and faster-moving competitors.
