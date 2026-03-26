# Home Staff

**A team of AI personas for running your household — built for Claude Code.**

What people call "emotional labor" is actually executive functioning. Home Staff gives you a team of purpose-built AI personas that handle the cognitive load of running a household — so you can be more present for the people you love.

## What's in the box

Starter persona templates for the domains that eat the most household brain power:

| Persona | Role | Domain |
|---------|------|--------|
| **Chief of Staff** | The coordinator | Daily briefs, priority arbitration, keeps the team aligned |
| **House Manager** | The EA | Calendar, logistics, school, vendors, social planning |
| **Family CFO** | The money brain | Finances, insurance, benefits, tax prep, budget |
| **Health Coach** | The wellness lead | Medical coordination, appointments, sustainable pace |
| **Career Coach** | The life designer | Career strategy, opportunity evaluation, life design |
| **Home Security** | The paranoid friend | Network security, smart devices, family digital privacy |
| **Kitchen Intel** | The dinner solver | Pantry inventory, quick meals from what's on hand, grocery lists |

You don't need all 7. Start with 2-3 that match your biggest pain points.

## Quick start

### 1. Install Claude Code

```bash
npm install -g @anthropic-ai/claude-code
```

### 2. Set up your memory directory

```bash
mkdir -p ~/.claude/projects/-YOUR-PROJECT-PATH/memory
```

### 3. Copy the personas you want

```bash
# Copy all starters
cp personas/*.md ~/.claude/projects/-YOUR-PROJECT-PATH/memory/

# Or just the ones you need
cp personas/house-manager.md ~/.claude/projects/-YOUR-PROJECT-PATH/memory/
cp personas/kitchen-intel.md ~/.claude/projects/-YOUR-PROJECT-PATH/memory/
```

### 4. Create your MEMORY.md index

Copy `memory-index-example.md` to your memory directory as `MEMORY.md` and edit it to list only the personas you're using.

### 5. Personalize

Each persona file has `[CUSTOMIZE]` markers where you should add your own context — family members, location, dietary needs, financial situation, etc. The personas work without customization but get dramatically better with it.

## How it works

- **Persona files** are markdown with frontmatter that Claude reads at session start
- **MEMORY.md** is the index — Claude reads this first to know who's on the team
- **Activation** is by name — say "House Manager, what's on the calendar?" or "Kitchen Intel, what can I make with chicken and rice?"
- **Chief of Staff** ties it all together — runs morning briefs that synthesize across all personas

## Optional: slash commands

For a full morning workflow, check out [claude-burndown](https://github.com/christinebuilds/claude-burndown) which includes `/gm` (morning brief), `/daily-tasks` (email triage), and 16 other commands.

## Optional: Notion Command Center

Home Staff works great from the CLI alone, but if you want a visual hub your whole household can see, connect it to a Notion workspace via MCP.

### Home Stack layout

The **Home Stack** is a single Notion page that serves as your command center, organized by life area:

| Section | What goes here |
|---------|---------------|
| 🧠 **How It Works** | Overview and views (My Week, Overdue, Today, Inbox, Burndown Queue) |
| 📋 **Databases** | Projects, Tasks, and Recurring Tasks databases |
| 🏠 **Home Ops** | Household management and daily operations |
| 💰 **Finance** | Benefits, claims, budgeting |
| 💪 **Health** | Medical prep, wellness, self check-ins |
| 💼 **Career** | Job search, networking, professional growth |
| 🔒 **Security** | Credentials, access audits, supply chain security |
| 🍳 **Kitchen** | Pantry inventory, grocery lists |
| ✍️ **Writing** | Creative projects and publishing |
| 💻 **Code** | Dev projects and tools |
| 🌍 **Kinship Earth** | Environmental data and integrations |
| ⚖️ **Legal** | Legal matters and compliance |
| ☀️ **Daily Briefs** | Archive of morning briefs from `/gm` |

### Automated report routing

When you run automated commands, their outputs get saved to the matching Notion section:

- `/gm` morning briefs → ☀️ Daily Briefs
- `/security-check` → 🔒 Security
- `/nn` burndown → relevant project area
- `/daily-tasks` → 💰 Finance or 💼 Career as appropriate

This gives you a single review surface — no hunting through CLI logs.

### Setup

1. Add the [Notion MCP server](https://github.com/anthropics/claude-code) to your Claude Code config
2. Create a top-level "Home Stack" page in Notion
3. Add Projects, Tasks, and Recurring Tasks databases
4. Organize sections by your own life areas (use the table above as a starting point)

## Philosophy

- **Presence over productivity** — the goal isn't to optimize your household, it's to free up your brain for the things only a human can do
- **Start small** — 2 personas that handle your top pain points beats 7 personas you never configured
- **Your context matters** — a generic AI assistant is fine; one that knows your family, your kitchen, and your financial situation is transformative
- **Name them** — sounds silly, works in practice. Named personas feel like a team, not a chatbot.

## Important disclaimers

Home Staff personas are AI assistants, not licensed professionals. Specifically:

- **The Family CFO is not a financial advisor, CPA, or tax professional.** It can help you organize information and think through decisions, but it is not a substitute for licensed financial, tax, or investment advice. Consult qualified professionals for financial decisions.
- **The Health Coach is not a doctor, therapist, or licensed health provider.** It can help you prepare for appointments and track health goals, but it does not diagnose, treat, or replace professional medical care.
- **Home Security provides general guidance, not certified security auditing.** For serious concerns, consult a professional.
- **No persona provides legal advice.** Period.

Use these tools to *organize your thinking and reduce cognitive load* — not as a substitute for professional expertise. When in doubt, consult a human professional.

## License

MIT — use it however you want.

---

*Built during a Mommy Hackers session by [Christine Su](https://christineiswriting.com).*
