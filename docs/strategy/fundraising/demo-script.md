# Demo Script for Investor Meetings

*A guided walkthrough of the working product for investor meetings.
Target duration: 5-7 minutes within a 30-minute meeting.
Rehearse this until it feels natural -- never read from the script.*

---

## Before the Demo

### Setup Checklist

- [ ] Streamlit app running locally on your machine
- [ ] Synthetic data loaded (seed=42 for deterministic, consistent results)
- [ ] Browser window open, zoomed to readable size for screen share
- [ ] Terminal hidden (investors don't need to see the backend)
- [ ] Internet connection stable (for screen sharing)
- [ ] Have 2-3 backup screenshots ready in case of technical issues

### Framing (Say This Before You Start)

> "Let me show you what this looks like in practice. What you're about to see
> is a working system -- not a mockup, not a prototype. It's running live against
> structured financial data that mirrors a real accounting firm. We have 24
> questions in our evaluation framework, backed by 120+ automated tests.
> We're iterating toward production accuracy."

---

## The Demo Flow

### Query 1: A Simple Financial Question

**What to type:**
> "What is the cash balance for Summit Peak Consulting?"

**Why this query:** It demonstrates the core use case -- a junior accountant
needs a number without interrupting a partner. It should return a specific
dollar amount with a citation.

**What to say while it processes:**
> "This is the most common question in any accounting firm. 'What's the balance?'
> Today, a junior staff member walks over to a senior, interrupts their work,
> and asks. Or they dig through QuickBooks for 10 minutes. Watch what happens."

**What to highlight in the response:**
- The specific dollar amount (accuracy)
- The citation showing WHERE the data came from (trust)
- The response time (speed vs. manual lookup)

**Talking point:**
> "That took [X] seconds. The same question takes 5-10 minutes through
> the traditional path. Multiply that by 20 questions a day across a
> 15-person firm. That's the value proposition."

---

### Query 2: A Multi-Step Analytical Question

**What to type:**
> "Show me the profit and loss for Riverside Wellness Clinic for January 2025"

**Why this query:** It demonstrates that the system understands accounting
concepts, not just simple lookups. A P&L requires aggregating revenue and
expense accounts -- the AI has to reason about the data structure.

**What to say while it processes:**
> "Now let's try something more complex. A profit and loss statement isn't
> a simple lookup -- it requires understanding account classifications,
> aggregating the right transactions, and presenting them in a format
> an accountant expects."

**What to highlight in the response:**
- The structured P&L format (the AI understands accounting)
- Revenue vs. expense categorization
- The tool-calling trace (expand this) -- show the AI "thinking"

**Talking point:**
> "See that trace? [Point to tool calls.] The system identified this as a
> client-level financial query, routed it to the client specialist agent,
> which called the P&L tool with the right parameters. That's not a
> keyword match -- that's reasoning about accounting concepts."

---

### Query 3: A Staffing / Operations Question

**What to type:**
> "Which employees are in the tax department and what are their billing rates?"

**Why this query:** It shows the system goes beyond financial data into
operational intelligence. This is a question an office manager or partner
would ask, not something you'd find in QuickBooks.

**What to say while it processes:**
> "Here's where it gets interesting. This isn't a financial question -- it's
> an operational one. The system doesn't just know the numbers. It knows
> the people, the departments, the billing rates. This is the 'digital twin'
> part -- it understands how the firm operates."

**What to highlight in the response:**
- Employee names and departments
- Billing rates (operational data)
- The fact that this came from a different tool/agent than the financial queries

**Talking point:**
> "We have 8 specialized tool modules spanning financial data, staffing,
> time and billing, scheduling, tax, payroll, analytics, and documents.
> The AI routes each question to the right specialist. A partner can ask
> about cash balances, staffing, client profitability, and firm policies
> all in the same conversation."

---

### Query 4: A Cross-Client Comparison (If Time Allows)

**What to type:**
> "Which of our clients provides the highest total revenue to the firm?"

**Why this query:** It demonstrates firm-level intelligence that spans
across all clients. This is the kind of question that currently requires
pulling data from multiple sources and building a manual comparison.

**What to say:**
> "This is a firm-level question -- which clients are driving our revenue?
> Today, answering this requires exporting data from QuickBooks, building
> a spreadsheet, and spending an hour on analysis. Here it takes seconds."

---

### Closing the Demo

> "Everything you just saw is working today. The system has 120 automated
> tests, a 24-question evaluation benchmark, and a medallion data architecture
> that can ingest data from any financial or  system.
>
> What we need now is execution capital. This funding lets me go full-time,
> deploy to our alpha customer, and close our first 3-5 paying firms.
> The product works. The market is ready. The question is speed."

---

## Handling Common Demo Questions

### "Is this using GPT-4 / ChatGPT?"

> "No. During development, we run on a local 32-billion parameter model
> for zero inference cost. In production, we use a model routing strategy --
> simple questions go to fast, cheap models; complex reasoning goes to more
> capable models. The architecture is model-agnostic."

### "What happens if the AI gets a number wrong?"

> "Every answer is grounded in retrieved data, not generated from memory.
> The AI queries the database directly and cites its sources. We also have
> a verification step that checks answers against source data. We have 120+
> automated tests and a regression testing framework to catch any degradation.
> We're iterating toward production accuracy."

### "How long does it take to set up a new firm?"

> "20-40 hours for initial setup: connect their QuickBooks, load their
> documents into the knowledge base, configure the agents for their
> terminology. After that, 6-12 hours per month for tuning and support.
> That's our services wrapper -- and it's where the human relationship
> creates switching costs."

### "What if the firm's data is messy?"

> "Garbage in, garbage out is a real concern. Our data pipeline includes
> quality checks at the silver layer. We actually flag data quality issues
> to the firm as a value-add -- 'We found 47 uncategorized transactions
> from January.' Improving their data quality makes the AI better and
> makes us indispensable."

### "What about data security?"

> "Financial data is sensitive by default. We have a cybersecurity advisor
> from BMO with NIST and PCI-DSS expertise. The architecture enforces
> multi-tenant isolation at the data layer -- every query is scoped by
> firm ID. A firm never sees another firm's data. SOC 2 preparation is
> planned for the seed stage."

---

## Technical Failure Backup Plan

If the demo breaks during a live presentation:

1. **Don't panic.** Say: "Live demos -- let me show you what this normally looks like."
2. Switch to pre-recorded screenshots or a screen recording.
3. Walk through the screenshots using the same narrative.
4. Frame it positively: "This is a real system with real complexity. The fact that it usually works at 94% accuracy on 24 questions is the point -- let me show you the evaluation results."

Always have screenshots of successful queries ready as a fallback.
