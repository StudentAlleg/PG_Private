# Legal Prerequisites for Fundraising

*These items MUST be completed before any investor conversation. No exceptions.
Each item has a status checkbox, responsible party, estimated cost, and deadline.*

---

## Checklist

### 1. Find a Startup Attorney

- [ ] **Status:** Not started
- **Responsible:** Mike
- **Budget:** $3K-$8K for initial engagement (entity formation + first set of agreements)
- **Deadline:** Week 1-2

**Requirements:**
- Specializes in Delaware C-Corp formation, SAFEs, cap tables, and early-stage startup law
- Experience with employment agreement review (critical given the confidentiality agreement)
- Familiar with 83(b) elections and founder equity structuring

**Where to look:**
- [Clerky](https://clerky.com) -- self-service incorporation optimized for startups ($799+ for formation). Handles stock issuance, advisor agreements, and SAFEs. Used by thousands of YC companies. Cost-effective for straightforward formation.
- [Cooley GO](https://www.cooleygo.com) -- free document generators from a top startup law firm. Good for understanding what standard docs look like before hiring.
- South Florida startup attorneys -- search Florida Bar directory for "startup" or "venture capital" practice areas. Ask advisory board for referrals.
- [Gunderson Dettmer](https://www.gunder.com) and [Wilson Sonsini](https://www.wsgr.com) both have startup programs with deferred fee arrangements for funded companies.

**What to avoid:**
- LegalZoom and similar -- not sufficient for VC-grade incorporation. Documents won't pass investor diligence.
- General practice attorneys who don't specialize in startups. The nuances of 83(b) elections, SAFE conversions, and cap table math require specific expertise.

---

### 2. Form Delaware C-Corp

- [ ] **Status:** Not started
- **Responsible:** Mike + Attorney
- **Budget:** $800-$3,000 (formation + registered agent + state fees)
- **Deadline:** Week 2-3

**Why Delaware:** Virtually all VC-backed startups incorporate in Delaware. Investors expect it. The legal precedent is well-established. The Court of Chancery specializes in corporate disputes. Incorporating elsewhere creates unnecessary friction.

**Documents needed:**
- Certificate of Incorporation
- Bylaws
- Initial Board Resolutions (appointing officers, authorizing stock issuance)
- Stock Purchase Agreements (for founder shares)
- Action by Incorporator

**Additional steps:**
- [ ] Apply for EIN (IRS, free, online)
- [ ] Foreign qualification in Florida (since the company operates in FL but is incorporated in DE)
- [ ] Open a business bank account
- [ ] Set up a registered agent in Delaware (required; ~$50-$150/year)

**Company name:** TBD -- needs to be decided before filing. Check availability on the [Delaware Division of Corporations](https://icis.corp.delaware.gov/ecorp/entitysearch/namesearch.aspx) site and with the USPTO for trademark conflicts.

---

### 3. Review Employment Agreement

- [ ] **Status:** Attorney briefing document prepared; attorney consultation pending
- **Responsible:** Mike + California Attorney
- **Budget:** $2,000-$5,000 (attorney review, written opinion, potential negotiation support)
- **Deadline:** Week 1-2 (URGENT -- blocks everything else)

**Context:** Mike has a confidentiality and materials agreement with Parr3 LLC (current employer, a music/entertainment industry accounting firm with 60 accountants and 90 HNW clients). The agreement is governed by California law (per the arbitration agreement).

**Key provisions identified (from legal review):**
- **IP Assignment (Section 5):** Assigns work product to employer, but explicitly incorporates California Labor Code Section 2870, which carves out inventions developed on the employee's own time, with own equipment, not relating to employer's business.
- **Liquidated Damages:** $100,000 per breach (not $1M as originally believed).
- **Non-Compete (Section 6(b)):** Restricts competitive activity during employment. Likely unenforceable under California Business & Professions Code Section 16600 (non-competes void in California, strengthened by SB 699 and AB 1076).
- **Non-Solicitation (Section 6(c)):** Restricts soliciting employer's employees and clients for 12 months post-employment.

**Strong facts for Mike:**
- Project Green developed entirely on own time, own equipment (separate PC, monitors, power supply)
- Parr3 explicitly rejected AI product development when Mike pitched it (mid-2025)
- Parr3 is a music/entertainment accounting firm; Project Green targets general accounting firms
- California law strongly protects employee inventions under these circumstances

**Attorney briefing document:** See `Legal Documents/attorney-briefing.md` for the complete briefing with all provisions, facts, timeline, and specific legal questions.

**Questions the attorney must answer:**

1. Does Project Green fall within the Section 2870 carve-out for employee inventions?
2. Is Section 6(b) (non-compete during employment) enforceable under California law?
3. What is the practical risk of the $100K liquidated damages clause?
4. What are Mike's post-employment obligations under the non-solicitation clause?
5. Can the attorney provide a written opinion suitable for investor diligence?
6. Can the attorney represent Mike in a potential negotiation with Parr3 for investment and IP acknowledgment?

**Risk assessment:**
- The facts and California law strongly favor Mike. The Section 2870 carve-out was explicitly included in the agreement.
- If Parr3 invests in Project Green (Stage 1 strategy), the employment agreement issue is resolved by mutual agreement rather than adversarial interpretation.
- A clean legal opinion is essential before any investor conversation.

---

### 4. Formalize Owen's Equity

- [ ] **Status:** Not started
- **Responsible:** Mike + Attorney
- **Budget:** Included in entity formation

**Structure:**
- 2,500,000 shares of common stock (25% of initial 10M authorized shares)
- 4-year vesting schedule, 1-year cliff
- Vesting means: Owen earns shares over time. If he leaves before 1 year, no shares vest. After the cliff, shares vest monthly over the remaining 3 years.
- This protects both parties: Owen knows he's getting 25%, and the company is protected if the relationship doesn't work out.

**Why vesting matters for investors:**
- VCs will NOT invest in a company where a 25% equity holder has no vesting. If Owen walked away on day one with 25%, that's dead equity the company can never recover.
- Vesting is standard and expected. It's not a sign of distrust -- it's good governance.

**83(b) election:**
- [ ] MUST be filed with the IRS within 30 days of stock grant
- This election means Owen pays tax on the stock's value at grant date (essentially $0 for a new company) rather than as it vests (when it could be worth much more)
- Missing this deadline has severe tax consequences. It cannot be extended.

---

### 5. Formalize Advisor Agreements

- [ ] **Status:** Not started
- **Responsible:** Mike + Attorney
- **Budget:** Included in entity formation (use standard FAST agreement template)

**Terms for each advisor:**
- 0.25% equity each (6 advisors = 1.5% total)
- 2-year vesting, no cliff
- Standard advisor agreement using the [Founder/Advisor Standard Template (FAST)](https://fi.co/fast) from the Founder Institute
- IP assignment clause -- any work product advisors create for the company belongs to the company
- Confidentiality obligations

**Advisors to formalize (6):**

| # | Domain | Key Qualification |
|---|--------|-------------------|
| 1 | Cybersecurity / Compliance | Sr Cybersecurity Analyst, BMO; US Navy veteran; NIST, PCI-DSS expertise |
| 2 | AI / Engineering | Deep AI and coding expertise; entrepreneurial mindset |
| 3 | Marketing / GTM Strategy | Marketing strategy and go-to-market specialist |
| 4 | [Domain TBD] | Trusted problem-solver, willing to learn |
| 5 | [Domain TBD] | Grounded observations, solid judgment |
| 6 | [Domain TBD] | [To be confirmed] |

---

### 6. IP Assignment to the Entity

- [ ] **Status:** Not started
- **Responsible:** Mike + Attorney
- **Budget:** Included in entity formation

**Actions required:**
- Mike assigns all Project Green IP (code, documentation, designs, trademarks) to the new C-Corp via a Technology Assignment Agreement
- Owen's existing work-for-hire agreement needs to be updated to assign IP to the C-Corp (currently assigns to Mike personally)
- Confirm that no third-party IP is incorporated without proper licensing
- Confirm that all open-source dependencies are permissively licensed (per AGENTS.md, they are)
- Advisor agreements include IP assignment for any contributions

---

### 7. SAFE Document Preparation

- [ ] **Status:** Not started (prepare after entity formation)
- **Responsible:** Attorney
- **Budget:** $500-$1,500 (or free via Clerky/Y Combinator standard SAFE)

**Stage 1 (Friends Round) SAFE terms:**
- Use the [Y Combinator standard SAFE](https://www.ycombinator.com/documents) -- post-money SAFE with valuation cap
- Valuation cap: $3M-$3.5M (negotiable; this is the friends round)
- No discount rate (keep it simple)
- Pro-rata rights: include for Parr3 (strategic investor, likely $50K+ check)
- MFN (Most Favored Nation) clause: standard in multi-SAFE rounds

**Stage 2 (Pre-Seed) SAFE terms:**
- Same YC standard post-money SAFE
- Valuation cap: $6M-$8M (justified by revenue at that point)
- Pro-rata rights: optional, may include for larger checks ($100K+)
- MFN clause: standard

---

## Estimated Total Legal Cost

| Item | Estimated Cost |
|------|---------------|
| Entity formation (Clerky or attorney) | $800-$3,000 |
| Employment agreement review | $500-$1,500 |
| Equity agreements (Owen + advisors) | $1,000-$2,000 |
| SAFE preparation | $0-$1,500 |
| Registered agent (annual) | $50-$150 |
| State fees (DE + FL foreign qualification) | $300-$600 |
| **Total** | **$2,650-$8,750** |

This is a necessary investment. No serious investor will engage without a clean entity, clear cap table, and proper legal structure.

---

---

## Strategic Sequencing (Updated 2026-03-06)

**Go-to-market is deliberately paused until the Parr3 employment agreement resolves.** This is the single blocking dependency for entity formation, fundraising, and public product activity.

**Required sequence:**

1. Grey Ocean delivers written legal opinion on the employment agreement (in progress)
2. Mike has the Parr3 conversation (leave-behind prepared, partnership proposal structured)
3. Resolution: either Parr3 invests (mutual agreement) or Mike proceeds independently (clean legal opinion)
4. Entity forms (Delaware C-Corp)
5. IP assigns to the C-Corp with clean chain of custody
6. Advisor agreements formalized (FAST template), Owen equity formalized (vesting + 83(b))
7. Go to market

**What continues in parallel:** Product development (Sprint 13.2+), team building (Kris NDA/IP signed, advisor relationships active), legal infrastructure (agreements drafted and ready for entity), alpha customer relationship maintenance.

**Rationale:** Visible competitive activity before resolution strengthens Parr3's position, makes investor diligence impossible, and risks the $100K liquidated damages clause. The legal position is strong (Section 2870, CA B&P Code 16600) but unresolved. Discipline now protects everything built later. See Risk Register R22.

---

*Update this checklist as items are completed. Target: all items checked before
first investor conversation.*
