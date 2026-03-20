# Risk Register and Mitigations

Every material risk, rated by probability and impact, with mitigation strategies and early warning indicators.

## Risk Rating Key

- **Probability:** H (High, >60%), M (Medium, 20-60%), L (Low, <20%)
- **Impact:** H (existential or major pivot required), M (significant delay or cost), L (manageable setback)

## Competitive Risks

### R1: Big Four Build a Competing Product for SMB

| Dimension | Assessment |
|-----------|-----------|
| **Probability** | Low |
| **Impact** | High |
| **Rationale** | The Big Four ($9.5B AI investment) are focused on their own practices and large clients. SMB is not their market. But if one decides to productize downmarket, they have resources we cannot match. |
| **Mitigation** | Move fast. Accumulate firm-specific data moats that a new entrant cannot replicate. Build deep integration depth. The Big Four move slowly; by the time they productize for SMB, we should have 50+ firms with switching costs. |
| **Early warning** | Deloitte, PwC, EY, or KPMG announce a SMB-targeted AI product; any Big Four firm acquires an AI accounting startup. |

### R2: ERP Incumbents (Intuit/QuickBooks) Add Agent Capabilities

| Dimension | Assessment |
|-----------|-----------|
| **Probability** | High |
| **Impact** | Medium |
| **Rationale** | Intuit will absolutely add AI features to QuickBooks. They already have basic AI in QBO. However, they are constrained to their own data (QBO only), their own ecosystem, and their own UI. They cannot be the multi-system intelligence layer. |
| **Mitigation** | Position as the overlay that connects ALL firm systems, not just QBO. Our multi-system, multi-agent architecture is something Intuit structurally cannot build (they won't integrate with Xero or competing payroll systems). |
| **Early warning** | Intuit announces agentic AI features in QBO; Intuit acquires an AI accounting startup; QBO launches a "firm-wide AI assistant." |

### R3: Well-Funded Startup Beats Us to Market

| Dimension | Assessment |
|-----------|-----------|
| **Probability** | Medium |
| **Impact** | Medium-High |
| **Rationale** | 60+ funded startups, $1.2B+ raised in this space. Gravis AI is the closest competitor (AI ERP for service businesses). A startup with $10M+ in funding could build faster. |
| **Mitigation** | Speed. Our small team is an advantage -- no board meetings, no consensus-building, no enterprise sales cycles. We ship in days, not quarters. Also: most funded startups are building point solutions (AP only, close only). Our multi-domain approach is a different bet. |
| **Early warning** | Gravis AI or similar announces accounting firm customers; a competitor raises a large round specifically for professional services AI. |

### R4: Horizontal AI (ChatGPT, Claude) Becomes "Good Enough"

| Dimension | Assessment |
|-----------|-----------|
| **Probability** | Medium |
| **Impact** | Medium |
| **Rationale** | Firms may decide that ChatGPT + their own prompts is sufficient. No need for a specialized product. |
| **Mitigation** | Generic AI cannot access firm-specific data, enforce access control, or integrate with QBO/Xero/Gusto. The moment a firm needs to ask "What was account 1000's balance last month?" using THEIR data, generic AI fails. Our demo must make this gap visceral. |
| **Early warning** | Firms report that ChatGPT/Claude is meeting their needs; declining interest in specialized tools in industry surveys. |

## Technical Risks

### R5: LLM Reliability for Financial Data

| Dimension | Assessment |
|-----------|-----------|
| **Probability** | Medium |
| **Impact** | High |
| **Rationale** | LLMs hallucinate. A hallucinated number in a financial context is not an annoyance -- it's a liability. If the AI says account 1000 has a balance of $50,000 when it's actually $30,000, that's a material error. |
| **Mitigation** | (1) Ground every answer in retrieved data (RAG), never pure generation. (2) Mandatory citations on all financial responses. (3) Confidence scoring -- if the agent isn't sure, it says so. (4) Verifier node in the graph that checks answers against source data. (5) Benchmarking framework to continuously measure accuracy. |
| **Early warning** | Accuracy below 95% on financial fact queries in benchmarks; beta firm reports incorrect numbers. |

### R6: Data Quality from Vendor APIs

| Dimension | Assessment |
|-----------|-----------|
| **Probability** | Medium |
| **Impact** | Medium |
| **Rationale** | Garbage in, garbage out. If a firm's QuickBooks data is messy (miscategorized transactions, missing entries), the AI's answers will reflect that mess. |
| **Mitigation** | (1) Silver layer transformation includes data quality checks. (2) Flag data quality issues to the firm as a service ("We found 47 uncategorized transactions from January"). (3) Start with firms that have reasonably clean books. (4) Data quality improvement becomes a value-add, not just a prerequisite. |
| **Early warning** | High error rates during beta; firm's QBO data is significantly messier than expected. |

### R7: Integration Complexity Exceeds Estimates

| Dimension | Assessment |
|-----------|-----------|
| **Probability** | Medium |
| **Impact** | Medium |
| **Rationale** | Each vendor API has quirks: rate limits, pagination, incomplete documentation, breaking changes. ADP requires a partner agreement. ProConnect has limited public API. Integration takes longer than expected -- always. |
| **Mitigation** | (1) Start with one integration (QBO) and prove it end-to-end before adding more. (2) Use QBO sandbox for development. (3) Budget 2x estimated time for each integration. (4) MCP server architecture means integrations are isolated -- one failing doesn't break others. |
| **Early warning** | QBO integration takes more than 4 weeks; unexpected API limitations that block key use cases. |

### R8: DuckLake Maturity Risk

| Dimension | Assessment |
|-----------|-----------|
| **Probability** | Low-Medium |
| **Impact** | Low |
| **Rationale** | DuckLake is experimental (version 0.x). It could have bugs, breaking changes, or be abandoned. |
| **Mitigation** | (1) DuckLake sits on standard Parquet files -- if DuckLake fails, data is still accessible via any Parquet-compatible tool. (2) Migration to Delta Lake or Iceberg is straightforward since the data format is open. (3) For MVP, the lakehouse could be replaced with plain DuckDB tables if needed. |
| **Early warning** | DuckLake development stalls; critical bugs in 0.x releases; the DuckDB team signals a different direction. |

## Regulatory Risks

### R9: AI Liability for Accounting Advice

| Dimension | Assessment |
|-----------|-----------|
| **Probability** | Medium |
| **Impact** | High |
| **Rationale** | If the AI gives incorrect information that a firm relies on for a client decision, who is liable? State CPA boards, FINRA, and emerging AI regulations are evolving. The legal landscape is uncertain. |
| **Mitigation** | (1) Archetype 1 is internal-only -- no client exposure. (2) Archetype 2 explains but never advises. Hard guardrails. (3) Terms of service clearly disclaim AI output as informational, not professional advice. (4) Citations on every response enable human verification. (5) Engage a lawyer specializing in AI liability before Archetype 2 launch. |
| **Early warning** | State CPA board issues guidance restricting AI use; a competitor faces a liability claim related to AI-generated financial information; FINRA announces new AI-specific rules. |

### R10: Data Privacy Regulations

| Dimension | Assessment |
|-----------|-----------|
| **Probability** | Low-Medium |
| **Impact** | Medium |
| **Rationale** | Client financial data is sensitive. State privacy laws (CCPA, etc.), potential federal privacy legislation, and firm-specific data handling requirements could impose constraints on how we store and process data. |
| **Mitigation** | (1) Data stays in firm-controlled environments where possible. (2) Encryption at rest and in transit from Phase 2. (3) Multi-tenant isolation prevents cross-firm data leakage. (4) Clear data processing agreements with each firm. (5) Design for data deletion -- the firm can remove their data at any time. |
| **Early warning** | New state privacy laws targeting AI/financial data; client firms express data sovereignty concerns during sales process. |

## Market Risks

### R11: Firms Adopt AI Slower Than Expected

| Dimension | Assessment |
|-----------|-----------|
| **Probability** | Medium |
| **Impact** | Medium |
| **Rationale** | Despite 41% adoption rate, many firms are conservative. "We've always done it this way" is a real objection. The jump from 9% to 41% may be overstated by survey methodology. |
| **Mitigation** | (1) Free assessment removes commitment barrier. (2) 30-day pilot reduces risk for the firm. (3) Internal-only Archetype 1 is the least scary AI deployment possible ("it's just for your team, not your clients"). (4) Position as augmentation, never replacement. (5) Focus on firms already feeling pain, not firms that need to be convinced AI is useful. |
| **Early warning** | First 10 sales conversations produce fewer than 3 interested firms; beta firm doesn't adopt product into daily workflow. |

### R12: PE Cycle Timing

| Dimension | Assessment |
|-----------|-----------|
| **Probability** | Medium |
| **Impact** | Low-Medium |
| **Rationale** | The PE exit wave thesis depends on interest rates normalizing. If rates stay high or PE holds longer, the Archetype 3 opportunity delays. |
| **Mitigation** | Archetype 3 is Phase 4 (2028+). The business must be viable on Archetypes 1 and 2 alone. PE is upside, not the core bet. If PE timing shifts, we still have a product that firms buy for operational improvement. |
| **Early warning** | Fed signals prolonged high rates; PE-backed firm pipeline doesn't develop by Phase 3. |

## Execution Risks

### R13: Two-Person Team Capacity

| Dimension | Assessment |
|-----------|-----------|
| **Probability** | High |
| **Impact** | High |
| **Rationale** | Mike and Owen are building the product, doing sales, onboarding firms, providing support, and developing strategy. This is the single biggest constraint on everything. |
| **Mitigation** | (1) Ruthless prioritization -- only work on the next milestone. (2) One firm, one use case, one interface at MVP. No feature creep. (3) Automate everything possible (CI/CD, testing, monitoring). (4) Use AI tools aggressively for development productivity (Cursor, Claude, etc.). (5) First hire decision at 10-15 firms. |
| **Early warning** | Missed milestone dates; quality degradation; burnout indicators; unable to respond to customer issues within 24 hours. |

### R14: Owen's Split Focus

| Dimension | Assessment |
|-----------|-----------|
| **Probability** | High |
| **Impact** | Medium |
| **Rationale** | Owen's 2026 goal includes landing full-time employment for skills development and capital. This means Project Green gets part-time engineering attention during a critical build phase. |
| **Mitigation** | (1) Acknowledged in the plan -- this is by design, not a surprise. (2) Owen's main-branch work provides the stable foundation. (3) Mike's rapid prototyping can move independently of Owen. (4) Architecture is modular -- work can be parallelized. (5) Owen's FT employment generates capital that can fund Project Green infrastructure. |
| **Early warning** | Owen's availability drops below 10 hours/week; critical path items blocked on Owen's schedule. |

### R15: Technology Complexity Overwhelm

| Dimension | Assessment |
|-----------|-----------|
| **Probability** | Medium |
| **Impact** | Medium |
| **Rationale** | The full vision involves: LangGraph, MCP, DuckLake, RAG, vector databases, OpenTelemetry, multiple vendor APIs, Microsoft Agents SDK, RBAC, multi-tenancy. That's a lot of technology for two people. |
| **Mitigation** | (1) Phase the complexity. Phase 0 is LangGraph + DuckDB + QBO + ChromaDB -- four technologies, not fifteen. (2) Use the simplest version of everything (DuckLake not Databricks, ChromaDB not Pinecone, local not cloud). (3) Each phase adds complexity only after the previous phase is stable. (4) The existing prototype and test suite are a strong foundation. |
| **Early warning** | Phase 0 takes longer than 3 months; more than 2 technologies in active integration simultaneously; test suite begins failing. |

## Platform Risks

### R16: Microsoft/Google Change SDK Terms

| Dimension | Assessment |
|-----------|-----------|
| **Probability** | Low |
| **Impact** | Medium |
| **Rationale** | Platform risk is inherent in building on someone else's SDK. Microsoft could change M365 Agents SDK pricing, capabilities, or terms. Google could do the same with Workspace Studio. |
| **Mitigation** | (1) MCP-based core is platform-independent. The surface layer is thin and replaceable. (2) Standalone web UI is always available as a fallback. (3) Avoid deep platform-specific dependencies in core logic. |
| **Early warning** | Microsoft announces significant pricing changes for M365 Agents SDK; SDK deprecation notices; competing platform becomes more attractive. |

### R17: Vendor API Deprecation or Pricing Changes

| Dimension | Assessment |
|-----------|-----------|
| **Probability** | Low-Medium |
| **Impact** | Medium |
| **Rationale** | QuickBooks, Gusto, or other vendors could restrict API access, increase pricing, or deprecate endpoints. Intuit has a history of API changes. |
| **Mitigation** | (1) Abstract vendor APIs behind MCP servers -- if an API changes, only the MCP server needs updating. (2) Cache data in the lakehouse -- agents don't query APIs directly. (3) Support multiple vendors per category (QBO + Xero) so no single vendor is a single point of failure. |
| **Early warning** | Vendor announces API version deprecation; new API pricing tiers; reduced rate limits; developer community reports access issues. |

### R18: LLM Pricing Increases

| Dimension | Assessment |
|-----------|-----------|
| **Probability** | Low (prices are trending down) |
| **Impact** | Low-Medium |
| **Rationale** | LLM pricing has been dropping consistently, but a reversal is possible if demand outpaces supply or a provider changes strategy. |
| **Mitigation** | (1) Multi-provider support (OpenAI, Anthropic, Google, local models). (2) Benchmarking framework enables rapid cost/quality comparison. (3) Local model fallback for cost-sensitive queries. (4) Caching reduces total API calls. (5) Current margins (86-98%) provide large buffer for price increases. |
| **Early warning** | Any major LLM provider announces price increases; cost-per-query trends upward in benchmarking reports. |

## Alpha Customer Risks

### R19: Product Readiness Gap for Alpha Delivery

| Dimension | Assessment |
|-----------|-----------|
| **Probability** | High |
| **Impact** | High |
| **Rationale** | The production readiness audit scored the codebase at 3/10. Critical issues include SQL injection vulnerabilities, no authentication, weak error handling, and no deployment infrastructure. The alpha customer cannot use the system until these are addressed. |
| **Mitigation** | (1) Prioritize security hardening (SQL injection, auth, input validation) as the first production sprint. (2) Implement error handling and resilience before customer onboarding. (3) Deploy with Docker for consistent environment. (4) Use the production readiness audit as the remediation checklist. |
| **Early warning** | Security audit items not resolved within 3 weeks; alpha customer onboarding delayed past 6 weeks from agreement date. |

### R20: Alpha Customer Expectations Exceed Delivery Capacity

| Dimension | Assessment |
|-----------|-----------|
| **Probability** | Medium |
| **Impact** | High |
| **Rationale** | The customer may expect a polished product. What we can deliver in the near term is a functional but rough alpha. If the gap between expectations and reality is too large, the customer loses confidence and the engagement fails. |
| **Mitigation** | (1) Set clear expectations during onboarding: this is an alpha, they will encounter limitations. (2) Define a narrow initial scope (e.g., "ask questions about your QBO data" not "run your entire firm"). (3) Weekly check-ins to surface misalignment early. (4) Fast response to reported issues (24-hour SLA). |
| **Early warning** | Customer expresses frustration in first two weeks; feature requests outside the roadmap; staff stop using the tool. |

### R21: Alpha Engagement Consumes All Development Capacity

| Dimension | Assessment |
|-----------|-----------|
| **Probability** | Medium-High |
| **Impact** | Medium |
| **Rationale** | Supporting a live customer (bug fixes, feature requests, check-ins) while also hardening the platform is a heavy load for a small team. The risk is that customer support crowds out the systematic improvements the platform needs. |
| **Mitigation** | (1) Timebox customer support to defined windows. (2) Log all issues but batch non-critical fixes into sprints rather than reacting to each one individually. (3) Prioritize platform improvements that directly serve the alpha use case. (4) Be transparent with the customer about the development cadence. |
| **Early warning** | More than 30% of development time spent on ad-hoc customer support; roadmap milestones slipping; customer issues backlog growing faster than resolution rate. |

## Employment & IP Risks

### R22: Parr3 Employment Agreement — IP and Non-Compete Constraints

| Dimension | Assessment |
|-----------|-----------|
| **Probability** | High (this is an active, unresolved constraint) |
| **Impact** | High (existential — affects entity formation, fundraising, and go-to-market timing) |
| **Rationale** | Mike has a confidentiality and materials agreement with Parr3 LLC (California law). Key provisions: IP assignment clause (Section 5, with Section 2870 carve-out), $100K liquidated damages, non-compete during employment (Section 6(b), likely unenforceable under CA B&P Code 16600), and 12-month non-solicitation post-employment. While the legal position is strong (own time, own equipment, employer rejected AI development, Section 2870 explicitly included), the agreement is unresolved. Going to market before resolution creates visible evidence of competitive activity during employment, strengthens Parr3's position if they choose to litigate, and makes investor diligence impossible. |
| **Mitigation** | (1) Attorney engaged (Grey Ocean, fee agreement 3/3/2026) to deliver written legal opinion. (2) Parr3 conversation structured as partnership proposal — investment + first customer + clean transition — giving them a reason to say yes. (3) Leave-behind document prepared with investment terms, deployment proposal, transition plan, and IP acknowledgment framework. (4) All development provably on own time, own equipment, own resources — strengthening 2870 defense with every commit. (5) Go-to-market deliberately paused until resolution. (6) If Parr3 invests, resolves by mutual agreement. If not, proceed with clean legal opinion. |
| **Early warning** | Parr3 expresses hostility to the proposal; attorney identifies unexpected weakness in the 2870 defense; Parr3 retains counsel in response to the conversation; Mike's employment is terminated before the conversation happens. |
| **Strategic sequence** | (1) Grey Ocean legal opinion → (2) Parr3 conversation → (3) Resolution (investment or independent proceed) → (4) Entity formation → (5) IP assignment → (6) Go to market. Steps 1-3 are the critical path. Everything else is infrastructure built in parallel. |
| **Current status (2026-03-06)** | Attorney engaged. Leave-behind prepared. Product build continuing privately. GTM on deliberate hold. |

---

## Risk Summary Matrix

| ID | Risk | Prob | Impact | Priority |
|----|------|------|--------|----------|
| R22 | Parr3 employment agreement / IP constraints | H | H | **Critical — BLOCKING** |
| R19 | Product readiness gap for alpha | H | H | **Critical** |
| R13 | Two-person team capacity | H | H | **Critical** |
| R5 | LLM reliability for financial data | M | H | **Critical** |
| R9 | AI liability for accounting advice | M | H | **Critical** |
| R20 | Alpha customer expectations exceed capacity | M | H | **Critical** |
| R21 | Alpha consumes all dev capacity | M-H | M | **High** |
| R14 | Owen's split focus | H | M | **High** |
| R2 | ERP incumbents add agent capabilities | H | M | **High** |
| R11 | Firms adopt AI slower than expected | M | M | **High** |
| R15 | Technology complexity overwhelm | M | M | **High** |
| R3 | Well-funded startup beats us | M | M-H | **High** |
| R6 | Data quality from vendor APIs | M | M | **Medium** |
| R7 | Integration complexity | M | M | **Medium** |
| R4 | Horizontal AI good enough | M | M | **Medium** |
| R10 | Data privacy regulations | L-M | M | **Medium** |
| R1 | Big Four build competing product | L | H | **Medium** |
| R17 | Vendor API changes | L-M | M | **Medium** |
| R12 | PE cycle timing | M | L-M | **Low** |
| R16 | Platform SDK changes | L | M | **Low** |
| R8 | DuckLake maturity | L-M | L | **Low** |
| R18 | LLM pricing increases | L | L-M | **Low** |

## Top 4 Actions to Reduce Risk

1. **Resolve the Parr3 employment agreement (R22).** This is the single blocking risk. No entity formation, no fundraising, no go-to-market until this resolves. Grey Ocean delivers the legal opinion, Mike has the Parr3 conversation, and the outcome determines the path forward. Everything else is infrastructure built in parallel so that the moment this clears, the company can move immediately.

2. **Continue building the product privately (R19, R13).** The production build continues at full speed — hardening the codebase, completing the frontend, preparing for alpha delivery. Every sprint completed before the Parr3 conversation compresses the timeline between "resolution" and "product in the market." This is not wasted time; it is strategic preparation.

3. **Build the legal and team infrastructure (R22, R13).** Formalize agreements (Kris NDA/IP done, advisor FAST agreements pending entity), prepare entity formation documents, and develop the team. When the gate opens, the company should be ready to incorporate, assign IP, and ship — not start planning.

4. **Set and manage alpha customer expectations (R20).** The alpha engagement is committed but delivery is gated on R22 resolution. Maintain the relationship, keep the customer informed at an appropriate level, and ensure the product is ready to deploy the moment the legal path is clear.
