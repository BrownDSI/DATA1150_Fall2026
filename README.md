# DATA1150_Fall2026
Data Science Fellows Fall 2026 Project Materials
# DATA 1150 Project Repository

This repository is your team's home base for your DATA 1150 project. Everything directly tied to your project lives here: meeting notes, planning, documentation, code, work in progress, and final deliverables. You have the whole semester to work on this, and it does not have to be in this sample repo's specific format or template but we expect that all your work will be present and well organized.

**Read this first:** Never commit raw, sensitive, or identifiable data (student records, course evaluations, chat transcripts, credentials, API keys). 

---

## Getting started 

### 1. Fork and clone

1. Click **Fork** at the top right of this repo on GitHub.
2. Clone your fork to your computer:
   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
   cd <repo-name>
   ```
3. Add the course repo as `upstream` so you can pull in fixes from the course team:
   ```bash
   git remote add upstream https://github.com/<course-org>/<template-repo-name>.git
   ```

### 2. Fill in your project charter

Open [`PROJECT.md`](PROJECT.md) and fill it in with your partner during or right after your kickoff meeting: goals, deliverables, timeline, communication preferences, required tools, and constraints. Treat this as the shared source of truth and update it when scope changes.

### 3. Log your kickoff meeting

Copy `meetings/_TEMPLATE.md` to `meetings/YYYY-MM-DD-kickoff.md` and fill it in.

---

## Folder guide

| Folder / file | What goes here |
|---|---|
| `PROJECT.md` | Project charter: partner, goals, deliverables, timeline, constraints |
| `meetings/` | One file per meeting, named `YYYY-MM-DD-topic.md` |
| `planning/` | `roadmap.md` (milestones) and `weekly-log.md` (done / blocked / next) |
| `docs/` | Decision log, user guides, handoff notes, and reference materials |
| `docs/user-guide/` | Instructions written for your partner or non-technical users |
| `docs/handoff.md` | What your partner needs to keep this project running after the term |
| `data/` | Data folders (see the privacy rules below) |
| `src/` | Scripts, pipeline code, and utilities |
| `notebooks/` | Exploratory analysis (Jupyter, Quarto, etc.) |
| `work-in-progress/` | Drafts that are not ready to share as deliverables |
| `deliverables/` | Final, partner-facing outputs, with a README indexing what is here |

**This structure is a starting point.** Delete folders you do not need (for example, a syllabus project may never use `src/`) and add ones you do. If you restructure significantly, update this README so a new reader can still find things.

---

## Data and privacy rules

Several projects involve sensitive information, such as student reflections, chat transcripts, or course evaluations. Follow these rules:

- `data/raw/` and `data/interim/` are **gitignored**. Do not remove them from `.gitignore`.
- Only commit data to `data/processed/` if you are sure it is de-identified and your partner has approved it.
- Use `data/sample/` for **synthetic or fake** examples so others can run your code without real data.
- Never commit passwords, API keys, tokens, or `.env` files.
- Follow your partner's rules on approved tools. Some data may not be uploaded to non-sanctioned AI tools. When in doubt, ask your partner and the TA **before** using the data with any external tool.

---

## Day-to-day workflow

1. **Pull** the latest changes before you start working:
   ```bash
   git pull
   ```
2. **Work on a branch** for anything larger than a quick edit:
   ```bash
   git checkout -b short-descriptive-name
   ```
3. **Commit early and often** with clear messages:
   ```bash
   git add <files>
   git commit -m "Add extraction script for PDF evaluations"
   ```
4. **Push** and open a **pull request** into your main branch. If you are on a team, ask a teammate to review it. If you are solo, review your own diff before merging.
5. **Update your logs.** After each meeting, add notes to `meetings/`. Each week, add a short entry to `planning/weekly-log.md`.

---

## Conventions

- **File names:** lowercase with hyphens, and dates in `YYYY-MM-DD` format (e.g., `2026-10-14-weekly-checkin.md`).
- **Meeting notes:** always include attendees, decisions made, and action items with owners and due dates.
- **Decisions:** record important choices and the reasoning in `docs/decisions.md`. Future you and your partner will thank you.
- **Documentation:** write for someone who was not in the room. Assume your partner may hand this project to a non-technical colleague.
- **Deliverables:** move work from `work-in-progress/` to `deliverables/` only when your partner has seen it or it is ready for review, and update `deliverables/README.md` with its status.

---

## End of term checklist

- [ ] `PROJECT.md` is up to date and reflects what was actually delivered
- [ ] Final deliverables are in `deliverables/` and indexed in its README
- [ ] `docs/user-guide/` is complete and has been tested by someone who did not write it
- [ ] `docs/handoff.md` says where final versions live (repo, shared drive, Kodiak, partner's system, etc.) and who owns them
- [ ] No sensitive data or credentials are in the repo or its history
- [ ] Code runs from a clean clone, with setup instructions in `src/README.md` or below
- [ ] Partner has confirmed they can access everything they need

---

## Setup instructions (edit for your project)

_Replace this section with the steps to run your code: required software, how to install dependencies, and how to run your main script or notebook._

```bash
# Example
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python src/main.py
```

---

## Project summary (edit for your project)

_Replace this with two or three sentences describing your project, your partner, and what you are building. Link to `PROJECT.md` for details._


---

## Getting help

- Stuck on Git or GitHub? Ask the TA
- Unsure whether something is safe to commit? **Ask first.**
- Need to change the scope of your project? Discuss it with your partner, then record the change in `PROJECT.md` and `docs/decisions.md`.
