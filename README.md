# Zubair Zafar

**Founding Engineer at Andever AI (Stealth)** · San Francisco · **7x Hackathon Winner** 

I'm the first engineer at a stealth AI startup, where I own the product from architecture to deploy. Most of my work sits where LLM agents meet systems that can't be wrong: approval gates, deterministic checks around model output, eval harnesses, and MCP servers that other agents call.

[Portfolio](https://zubair480.github.io) · [LinkedIn](https://linkedin.com/in/zubair480) · [Email](mailto:zubairzafar480@gmail.com)

---

### What I'm building now

**Andever AI (Stealth)**: sole engineer, designed and built the platform from an empty repo.

- TypeScript monorepo (Node 22, pnpm) split into a core engine, a provider-agnostic LLM layer with a deterministic fallback, and an MCP server over stdio and streamable HTTP
- Human-approval gate enforced in the core engine rather than the UI, so no transport can release unapproved output; the deterministic and LLM paths share the same ranking, citation and safety logic
- AES-256-GCM encrypted store with key rotation and delete-on-request; bearer tokens or OAuth 2.1 (PKCE, dynamic client registration) on the HTTP transport
- 787 tests, 34/34 blind hash-locked eval tasks, p95 under 500 ms per tool, and 1,240 fuzzed inputs per transport with zero crashes; CI runs lint, typecheck, tests, build and evals
- Profiled an earlier Python service down from 803 MB to 88 MB of memory and a 9.5 s workload to 0.08 s by moving heavy dependencies to build time, so it fits a 512 MB instance

---

### Selected work

| Project | What it does | Result |
|---|---|---|
| [RefundGuard](https://github.com/zubair480/refundguard) | Release gate for agents that hold a wallet. 11 adaptive scam personas attack the agent while 3 honest customers act as the control; every ledger movement is replayed against policy in code, and an LLM judge's findings count only if they quote the agent verbatim | v1 leaked $310; v3 held 0 of 11 breaches with all honest customers served |
| [Thermal Crusoe](https://github.com/zubair480/crusoe-hackathon) | 3D thermal twin of a motor control center in three.js that finds the overheating joint and drafts the inspection report. I owned the Next.js APIs, shared contracts and integration (team of 4) | 180-request eval at about 681 ms median |
| Attest | A bank's agent questions a vendor's agent on security controls. Answers count only when evidence backs them: a deterministic severity counter and an LLM relevance judge both have to agree, and every decision leaves a receipt with the sha256 of its raw evidence | Four evidence collectors, judgments cached on the evidence digest |
| RecallRadius | Neo4j issue graph for EV assembly linking parts, suppliers, causes and fixes. I owned the contracts, APIs and integration tests (team of 3) | 114 tests, 23/23 acceptance against Aura |
| [Redline](https://github.com/zubair480/Redline) | Prompt-injection scanner that models an agent's tools as a graph and finds paths from untrusted input to privileged action that cross no guard. I built the scan pipeline, row-level-security auth and fix endpoint | |
| [Successor](https://github.com/zubair480/mongo_db_hackathon) | Captures a retiring engineer's troubleshooting knowledge. I owned retrieval (Atlas Search and Vector Search with rank fusion) and a LangGraph executor checkpointed to Mongo | |
| MCP Auditor | Six parallel probers test live MCP servers against the SAFE-MCP catalog; a clean negative control must return zero findings | Contributor |

---

### 🏆 7x Hackathon Winner

| Place | Project | Event |
|---|---|---|
| 1st | RefundGuard | The Executable World, SF |
| 1st | Thermal Crusoe ($5,000, team) | Crusoe x The AI Conference hack day, SF |
| 1st | Smart CPM Parser | Amadeus / Etihad Green Development Challenge |
| 2nd | Attest (solo) | Agent Native Builders, Cloudflare SF |
| 2nd | ROOT (team) | CrewAI Hackathon, SF |
| 2nd | Clip Police (team) | Auth0 x Stripe Hackathon, Okta SF |
| 2nd | RecallRadius (team) | B.E.L.L.E x Qoder x Neo4j, SF |

The Amadeus win became an internship at Etihad, where I shipped the parser to production and cut cargo data-entry errors by 95%.

---

### Before Andever AI

- **Software Engineer (Graduate Assistant), Eastern Illinois University.** Rewrote a 2006-era PHP system in Laravel for 7,000+ users with SSO and role-based access, cutting API response time 65% through query and index work
- **Graduate Research Assistant, EIU.** YOLOv8 + PyTorch classifier on 80,000+ MRI scans, 97.2% test accuracy
- **Backend Software Engineer, WPBrigade.** Maintained 5+ production plugins with 15,000+ active installs and led reviews for a team of 5
- **M.S. Computer Information Technology**, EIU, 4.0 GPA, fully funded scholarship

---

### Stack

**Languages:** TypeScript, Python, PHP, JavaScript, SQL
**Agents and LLMs:** MCP (stdio, streamable HTTP), LangGraph, CrewAI, eval harnesses, LLM-as-judge, vLLM, Modal
**Backend:** Node.js, FastAPI, Flask, Django, Laravel, Next.js, Convex
**Data:** Postgres, MongoDB Atlas, Neo4j, MySQL, SQLite, Supabase
**Infra:** Cloudflare Workers and Durable Objects, Render, Docker, GitHub Actions
**ML:** PyTorch, YOLOv8, scikit-learn, MuJoCo

---

### Outside of shipping

- Section Leader for Stanford's Code in Place, teaching Python
- Hackathon mentor at Lablab.ai
- 460+ LeetCode problems; Google Code Jam, Meta Hacker Cup and Advent of Code
