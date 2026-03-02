# Building a Vault Nervous System
> *How we turned 759 scattered markdown files into a structured cognitive architecture.*
> D1g1z3n × Trey Wadsworth — March 1, 2026

---

## The Problem

759 markdown files. 147 orphans floating in space. A graph view that looked like static on a broken TV. Files existed but didn't *connect*. Every new session meant re-discovering what already existed.

Sound familiar?

## The Architecture

We built a nervous system. Not metaphorically — structurally.

### The Brain: Obsidian
Markdown files are neurons. `[[Backlinks]]` are synapses. Smart Connections (AI-powered semantic search) is the myelin sheath that speeds up signal transmission. The graph view is a literal neural map.

### The Hubs (6 Gravitational Centers)
Instead of letting files organize by folder, we created **hub pages** — one per operational vertical:

| Hub             | Domain                              | Purpose          |
| --------------- | ----------------------------------- | ---------------- |
| 🏠 HUB-Personal | Health, finance, family             | Life management  |
| 📮 HUB-Postal   | Day job                             | Income stability |
| 🔷 HUB-WD       | Business (Wadsworth Digital)        | Revenue growth   |
| 🎸 HUB-WR       | Community (WilmingtonRocks)         | Local presence   |
| 🌴 HUB-PHP      | Side project (Personal Happy Place) | Creative outlet  |
| 🧠 HUB-System   | Infrastructure, agents, tools       | The plumbing     |

Every file links back to its hub. Hubs cross-reference each other. The graph shows clear clusters with visible bridges.

### The Motor System: AI Agents
Five agents, each with a specialized role:

| Agent | Model | Function |
|---|---|---|
| D1g1z3n | Claude Opus | Strategy, orchestration |
| B1lb0 | Llama 3.1 8B (local GPU) | QA, grunt work (free inference) |
| Fr0d0 | Gemini 2.5 Pro | Deep research, analysis |
| S4mW1s3 | Claude Sonnet | Writing, content creation |
| P1pp3n | Gemini 2.0 Flash | Quick tasks, summaries |

Agents are assigned tasks via tags in a central `DAILY-OPS.md`:
```markdown
- [ ] LCC QA check 📅 2026-03-03 🔼 @b1lb0 #wd #qa [[LCC-ARCHITECTURE]]
```

### The Consciousness: Life Command Center
A real-time dashboard (HTML + Flask, served locally) that monitors:
- Financial positions (bank balance, crypto, paper trading)
- Health metrics (weight, blood sugar)
- Server health (CPU, RAM, disk)
- Email, tasks, news
- API costs

### The Task Flow
```
DAILY-OPS.md (task board)
  → Task with assignee + priority + due date + [[project link]]
    → Agent executes against project spec doc
      → Results written with backlinks to source
        → Memory file logged for continuity
```

## The Cleanup Process

### Step 1: Audit
Scanned all 759 `.md` files. Classified each as connected (has incoming or outgoing `[[links]]`) or orphan (none).

**Result:** 116 connected, 147 orphans.

### Step 2: Categorize
Mapped every orphan to a vertical (Personal, WD, WR, PHP, Postal, System) or marked as EXCLUDE (READMEs, code docs).

### Step 3: Create Hub Pages
Built 6 hub pages with curated links to their most important files. These became the gravitational centers of the graph.

### Step 4: Batch-Link
Script that walks every `.md` file and appends a footer with `[[HUB-xxx]]` backlinks based on directory path and content classification.

### Step 5: Chain Memory Files
Added `← [[Previous]] | [[Next]] →` navigation to all 27 daily memory files, creating a chronological chain.

### Step 6: Exclude Noise
Added `userIgnoreFilters` to `.obsidian/app.json` to hide READMEs, CHANGELOGs, and code documentation from the graph.

**Final result:** 249 connected, 0 orphans.

## The Three-Layer Tagging System

| Layer | Mechanism | Purpose | Example |
|---|---|---|---|
| Projects/Resources | `[[Links]]` | Graph connectivity, navigation | `[[Pour Fellas]]` |
| Categories/Verticals | `#tags` | Filtering, cross-cutting queries | `#wd #qa #health` |
| Assignees | `@name` | Task routing, delegation | `@b1lb0 @trey` |

**Rule of thumb:** If it deserves its own page → `[[Link]]`. If it's a filter → `#tag`. If it's a person/agent → `@convention`.

## The Daily Discipline

The structure is worthless without maintenance. Daily commitments:

**Human:**
- Write daily notes (the oxygen for the system)
- Log health, financial, and life events as they happen
- Run decisions through the priority framework before building
- Review DAILY-OPS.md morning and evening

**AI Agent:**
- Every file gets `[[backlinks]]` — no orphan nodes
- Memory logged same-day
- Morning briefing pulls from DAILY-OPS.md
- Periodic graph audit for drift

## The Insight

> *"Markdown files are the real oxygen of LLMs."* — Matt Berman

The more you write, the more context the agents have, the more connections surface, the better decisions you make. It's compound interest on human thought.

The moat isn't the technology. Obsidian is free. The AI models are commoditizing. The moat is **the discipline of daily writing and reflection** that feeds the system.

99.99% of people won't do this. That's the alpha.

## Inspiration
- [How I use Obsidian + Claude Code to run my life](https://www.youtube.com/watch?v=6MBq1paspVU) — Matt Berman × Internet Vin
- [The Commoditization of Intelligence](https://wadsworth.digital/power-paradigms) — Wadsworth Digital

---

*Built in one day. Maintained every day after.*

*Questions, ideas, collaboration: [billy-digizen-shared](https://github.com/BillyAmerica/billy-digizen-shared)*
