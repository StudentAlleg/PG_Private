# Demo Playbook

> **Status (2026-03-06):** This playbook was written for the Phase 0 Streamlit prototype. The system now runs on FastAPI + React with 27 tools across 9 modules. This document needs to be rewritten for the production system before any demos occur. All GTM activity is paused pending R22 resolution — see [Risk Register](risk-register.md).
>
> How to demonstrate the existing Project Green prototype to generate
> interest from accounting firm owners. This playbook works with what
> we have today -- the Streamlit chat UI, 10 tool modules, and synthetic
> data for "Greenfield Accounting LLC." No future features required.
>
> **Date**: February 2026

---

## What We're Showing

The demo shows a working AI assistant that answers real accounting
questions using real data queries. The audience should walk away thinking:
"If this could work with MY firm's data, that would be incredibly useful."

### What the Prototype Can Do Today

| Capability | Example |
|-----------|---------|
| Account balances | "What is the current cash balance?" |
| Journal entry search | "Show me all entries for the Rent account in January" |
| Trial balance | "Show me the trial balance" |
| Monthly P&L | "What was profit last month?" |
| Transaction lookup | "Show me journal entry #5" |
| Conversational follow-up | "Break that down by account" (after a broad question) |

### What It Cannot Do Today (And How to Handle It)

| Limitation | How to Address |
|-----------|----------------|
| Only works with synthetic data | "This is sample data. When connected to your QuickBooks, it would use your real numbers." |
| No document Q&A (RAG) | "The next version will also answer questions about your SOPs and policies -- not just financial data." |
| Tax/payroll agents not yet built | "We have firm-level, client-level, and document specialists. Tax and payroll agents are placeholders for Phase 1+." |
| No multi-firm support | Don't mention this. It's an infrastructure detail, not a demo concern. |
| Runs locally | Frame as a feature: "This runs entirely on your hardware. Your data never leaves your office." |

---

## Demo Narrative: The 10-Minute Live Demo

### Setup (Before the Demo)

Checklist:

- [ ] Ollama is running (`ollama serve`)
- [ ] Qwen3:32B model is loaded (`ollama list` should show it)
- [ ] Lakehouse is initialized with synthetic data (`python scripts/seed_synthetic.py`)
- [ ] Streamlit app is running (`streamlit run src/projectgreen/api/chat_app.py`)
- [ ] Browser is open to the Streamlit app (typically `http://localhost:8501`)
- [ ] Clear any previous conversation (use the "Clear Conversation" button)

### The Flow

#### Opening (1 minute) -- Set the Context

Don't start with the product. Start with the problem.

> "Let me paint a picture. It's 2 PM on a Tuesday. A junior accountant
> needs to know the cash balance for a client. They could dig through
> QuickBooks, or they could walk over and interrupt a senior who's in
> the middle of a tax return. Which one do they actually do?"
>
> [Pause. Let them answer. They'll say "interrupt the senior."]
>
> "Exactly. Now imagine they could just ask. Like this."

#### Question 1 (2 minutes) -- The Easy Win

Type: **"What is the current cash balance?"**

What happens: The agent calls `get_account_summary`, retrieves the real
balance from the data, and presents it clearly.

What to say:

> "Watch what happens. The AI understands the question, decides which
> data to look up, queries the actual ledger, and gives a specific
> number. Not a guess -- the real balance from the books."

If the audience is technical or curious, expand the trace panel to show
the tool calls. If they're not technical, skip the trace and focus on
the answer.

#### Question 2 (2 minutes) -- Show Data Depth

Type: **"Show me the trial balance"**

What happens: The agent calls `get_trial_balance` and presents a
formatted trial balance with debits and credits.

What to say:

> "This is the full trial balance, pulled from the general ledger in
> real time. If a journal entry was posted 5 minutes ago, the next
> time someone asks this question, it's reflected."

#### Question 3 (2 minutes) -- Show Intelligence

Type: **"What was our profit last month?"** or **"Show me the monthly P&L"**

What happens: The agent calls `get_monthly_pl` and summarizes revenue,
expenses, and net income by month.

What to say:

> "Notice it understood 'last month' without me specifying a date. And
> it's pulling from the same data your team would use if they ran a
> report in QuickBooks -- but the answer comes in 20 seconds instead
> of 5 minutes of clicking through menus."

#### Question 4 (2 minutes) -- Show Specificity

Type: **"Show me all rent expenses in January"**

What happens: The agent calls `query_ledger` with filters for the rent
account and January date range, returning specific journal entries.

What to say:

> "This is where it gets really useful for day-to-day work. Instead
> of opening QuickBooks, navigating to the right report, filtering by
> date and account -- your team just asks. And the answer includes
> the actual journal entries, not just a summary."

#### Closing (1 minute) -- Plant the Seed

> "Everything you just saw runs on a local computer. No cloud, no
> subscriptions, no data leaving the building. This is a prototype --
> it's running on sample data. The next step is connecting it to a
> real QuickBooks instance so it answers with your actual numbers."
>
> "The question I'm exploring with firm owners is: if your team could
> ask questions like this -- about your data, your processes, your
> policies -- what would that change about how you run your firm?"

Then listen. The best demos end with the audience talking, not you.

---

## Demo Narrative: The 3-Minute Video Recording

For async distribution (email, LinkedIn, website). Record a screen
capture with voiceover.

### Script

**[Screen: Streamlit app, empty chat]**

> "This is a prototype AI assistant built specifically for accounting
> firms. It connects to the firm's ledger and answers questions using
> real data. Let me show you what it can do."

**[Type: "What is the current cash balance?"]**

> "A simple question any junior might ask. Instead of looking it up
> in QuickBooks or interrupting a senior, they ask the AI."

**[Wait for response. Highlight the specific number.]**

> "That's the actual balance from the ledger. Not a guess."

**[Type: "Show me the monthly P&L"]**

> "It handles more complex questions too. Monthly profit and loss,
> broken down by revenue and expenses."

**[Wait for response. Let it display.]**

> "This took about 20 seconds. Running on a local machine. No cloud
> required. No data leaves the building."

**[Type: "Show me all rent expenses in January"]**

> "And it can drill down into specific transactions."

**[Wait for response.]**

> "This is sample data. When connected to a real QuickBooks instance,
> every answer uses the firm's actual numbers."
>
> "If you run an accounting firm and you're curious about what AI
> can do for your practice, I'd love to have a conversation."

**[End screen: Contact info]**

### Recording Tips

- Use a clean desktop (hide personal bookmarks, notifications)
- Record at 1080p or higher
- Keep the browser at a readable zoom level (125-150%)
- Don't speed up the AI response time -- the real speed is impressive enough
- Keep the voiceover conversational, not scripted-sounding
- One take is fine. Imperfect is authentic.

---

## Objection Handling

Firm owners will have questions and concerns. Here are the common ones.

### "This is just ChatGPT, right?"

> "No. ChatGPT is a general-purpose AI that doesn't know your firm's
> data. This is built specifically for accounting firms and it queries
> your actual ledger. When it says the cash balance is $3,905, that's
> the real number from your books -- not a guess."

### "Will it replace my staff?"

> "No. This is a tool your staff uses, like how they use QuickBooks or
> Excel. It handles the repetitive lookup questions so your people can
> focus on the work that actually requires their judgment and expertise.
> Your senior accountants should be doing advisory work, not answering
> 'what's the cash balance?' twenty times a week."

### "What about data security?"

> "Great question. The prototype you're seeing runs entirely on a local
> machine. No data goes to the cloud. No external APIs. In a production
> deployment, we'd ensure your data stays within your firm's controlled
> environment. Security is a first-class concern, not an afterthought."

### "How accurate is it?"

> "Our testing shows 94% accuracy on a bank of 24 representative
> accounting questions. For financial data queries -- balances, ledger
> lookups, trial balance -- it's pulling directly from the database,
> so the numbers are exact. Where accuracy matters most (specific
> dollar amounts), the AI doesn't guess. It queries."

### "How much does it cost?"

> "We're still in the early stages of working with firms to figure
> out the right pricing model. I'm more interested in understanding
> whether this solves a real problem for your firm first. If it does,
> we'll figure out the pricing together."

Do NOT commit to specific pricing. The goal is to learn, not to close.

### "When can we try it with our data?"

This is the best possible objection. It means they're interested.

> "We're working on the QuickBooks integration now. I'd love to
> have your firm be one of our early partners. That means you'd
> get early access in exchange for your feedback and a case study.
> Let me follow up with a timeline and what that would look like."

Then follow up within 48 hours with a concrete next step.

### "I'll think about it" / polite non-commitment

> "Totally fair. This is new territory for most firms. If it's
> helpful, I can send you a short summary of what we discussed
> and the demo recording. And if anything changes or you have
> questions later, I'm always available."

Send the summary. Follow up in 30 days. Don't push.

---

## After the Demo

### If They're Interested

1. Send a thank-you message within 24 hours
2. Attach the demo video (if recorded) or a brief written summary
3. Propose a specific next step: "Would you be open to a 30-minute
   AI readiness assessment for your firm? It's free and you'll get
   a useful summary regardless."
4. Schedule the next meeting before leaving the current one if possible

### If They're Lukewarm

1. Send a brief thank-you. No pressure.
2. Add them to the LinkedIn content audience (follow / connect)
3. Follow up in 30-60 days with a relevant piece of content
4. They may not be ready today. They might be ready in 6 months.

### If They're Not Interested

1. Thank them for their time. Mean it.
2. Ask: "Who else should I be talking to? Do you know other firm
   owners who might find this interesting?"
3. A "no" on the product can still produce a referral.

### Always Record What You Learned

After every demo, write down:

- What questions did they ask?
- What seemed to excite them most?
- What concerned them?
- What did they say about their own firm's challenges?
- Would they be a good fit for the product? Why or why not?

This information is more valuable than any amount of market research.

---

## Demo Variations

### The "Hallway Demo" (2 minutes, phone or laptop)

For chance encounters at events or informal meetings. No Streamlit
needed -- just describe what the product does and show the demo video
on your phone.

> "We're building an AI assistant for accounting firms. Here, let me
> show you a 90-second clip."
>
> [Show the pre-recorded demo video]
>
> "If you know any firm owners who might be interested, I'd love an
> introduction."

### The "Conference Talk" Demo (embedded in a presentation)

For speaking slots at CPA society events or accounting conferences.
Structure the talk as educational ("How AI Is Changing Firm Operations")
and include the demo as one example.

> "Let me show you what's possible today, not in theory, but actually
> running on a laptop right here."
>
> [Run 2-3 questions live]
>
> "This is one example. The broader point is that AI can do for
> knowledge work what spreadsheets did for calculations."

### The "Zoom Demo" (10 minutes, screen share)

Same as the 10-minute live demo, but share your screen. Tips:

- Test screen sharing before the call
- Use a clean browser window (no extra tabs)
- Keep the Streamlit app at a readable size
- Have Ollama running before the call starts (model loading takes time)
- Have a backup plan if the model is slow (show pre-recorded video)

---

## Technical Checklist for Demo Readiness

Run through this before any demo to ensure a smooth experience.

| Check | Command / Action | Expected Result |
|-------|-----------------|-----------------|
| Ollama running | `ollama list` | Shows qwen3:32b |
| Model loaded | `ollama run qwen3:32b "test"` | Response within 5 seconds |
| Synthetic data seeded | `python scripts/seed_synthetic.py` | No errors |
| Streamlit running | `streamlit run src/projectgreen/api/chat_app.py` | App opens in browser |
| Test query works | Ask "What is the cash balance?" | Returns a specific dollar amount |
| Response time acceptable | Time a query | Under 30 seconds |
| Clear conversation | Click "Clear Conversation" in sidebar | Chat history clears |

If anything fails, troubleshoot before the demo. A broken demo is worse
than no demo.
