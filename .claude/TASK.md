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
- [ ] **Research** current Kiro state via `/deep-research` (cited report) — GA, pricing, features, workflow, adoption.
- [ ] Verify research findings against official kiro.dev docs/changelog before writing.
- [ ] Update `README.md` to current reality (correct dates, pricing, features; keep the SDD pedagogy).
- [ ] Add a teenager-friendly explainer (plain language, why-it-matters, demo path).
- [ ] Build the updated PowerPoint deck for the youth presentation.
- [ ] Commit incrementally, push, open PR (public repo → drive to merge once green).

## Status
STARTED 2026-06-26 — branch `claude/refresh-kiro-2026`. Research phase next.

## Resume notes
- Repo files: `README.md` (750 lines), two `.pptx`, one `.png`. No source code — pure teaching material.
- Public repo, default `main`, no branch-protection rulesets → direct push + PR allowed; auto-merge.yml present.
