# TASK — Refresh Kiro teaching material (June 2026)

## End goal
The repo (`Optional-Home-Exercise-Tools-Corner`) is a teaching/reference resource about **AWS Kiro**
(the agentic, spec-driven IDE). The content is ~1 year stale (README dated *November 2025*, describes the
July 2025 public preview). Alexander needs to **present it to teenagers/students again**, so:

1. Bring the README and all docs up to date with Kiro's current (June 2026) reality — GA status,
   pricing, features, spec workflow, anything that changed.
2. Re-frame at least one artifact for a **youth/student audience** (current README is written as an
   "AI-agent contract", which is wrong altitude for teenagers).
3. Produce an **updated PowerPoint** for the presentation (existing: `Kiro_IDE_Orchestrator_Old_FH.pptx`,
   `Kiro_IDE_Orchestrator_NEW_FH.pptx`).

## Plan / checklist
- [x] **Research** current Kiro state via `/deep-research` + primary sources (kiro.dev) — GA, pricing, features.
- [x] Verify findings against official kiro.dev docs/changelog/GA blog (adversarial deep-research run corroborated).
- [x] Update `README.md` to current reality (GA Nov 17 2025, IDE 1.0 Jun 25 2026, credit pricing, CLI/Web,
      subagents/parallel, Auto model agent, MCP governance, fixed dead changelog link; SDD pedagogy preserved).
- [x] Add teenager-friendly explainer — `Kiro-fuer-Jugendliche.md` (bilingual DE/EN).
- [x] Build the youth presentation deck — `Kiro_IDE_Orchestrator_2026_Jugend.pptx` (11 slides, reproducible via `build_deck.py`).
- [ ] Commit deck, push, open PR (public repo → drive to merge once green).

## Status
DONE (content) 2026-06-26 — branch `claude/refresh-kiro-2026`. Opening PR to merge.

## Key verified facts (June 2026)
- Preview 2025-07-14 → **GA 2025-11-17** → latest **IDE 1.0 (2026-06-25)**. 250k+ devs in preview.
- Now: Kiro **IDE + CLI + Web** (app.kiro.dev). Built on Code OSS, powered by Amazon Bedrock; "Auto" model agent.
- Credit pricing: Free $0/50, Pro $20/1k, Pro+ $40/2k, Pro Max $100/5k, Power $200/10k; $0.04 overage.
- Subagents + concurrent spec tasks = parallel (old "one task at a time" limit gone). Web search in chat.
- SSO: AWS IAM Identity Center + Okta + Microsoft Entra ID. MCP registry governance for enterprise.
- Changelog moved: kiro.dev/docs/changelog (404) → kiro.dev/changelog/ide.

## Resume notes
- Repo files: `README.md` (750 lines), two `.pptx`, one `.png`. No source code — pure teaching material.
- Public repo, default `main`, no branch-protection rulesets → direct push + PR allowed; auto-merge.yml present.
