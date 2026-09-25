# DATA 1150 Project Repository

This repository is your team's home base for your DATA 1150 project. Everything directly tied to your project lives here: meeting notes, planning, documentation, code, work in progress, and final deliverables.

---

## Getting started (first week)

### 1. Create your own repo from the template

1. Open the template (YOU ARE HERE)
2. Click the green **Use this template** button, then **Create a new repository**.
3. Set **Owner** to your own GitHub account and give the repo a clear name (e.g., `data1150-yourname-projectname`).
4. **Set visibility to Private.** This is required. Your project may involve sensitive material and partner information, so never make this repo public without Linda's approval.
5. Click **Create repository**, then clone it:
   ```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   cd <your-repo-name>
   ```

> This is a copy of the template, not a fork, so there is nothing to sync with the original. Later changes to the template will not appear in your repo automatically. We will announce anything important as far as template updates.

### 2. Add Linda and TAs as collaborators, and remember to add your partner at a later date if necessary

A private repo is invisible to everyone else, including us, so you must give us access. If you are on a team, figure out who is hosting the main repo and ensure everyone has access and can work together.

1. In your repo, go to **Settings → Collaborators → Add people**.
2. Add **`Linda-Clark`** and **`Jojo52504, kimmonebartley2, and liamphealy`**.
3. Confirm the repo shows the **Private** label at the top of the page.

We will accept the invitations. Do this **this week, not at the end of the term.**

### 3. Submit your repo link 

**Reply to the EdStem post within a week of the Workshop with the link of your repo**. We will confirm we can open it. If we get a "404" page, either the collaborator invite has not been accepted or the username was mistyped, so double-check both.


### 4. Fill in your project charter

Open [`PROJECT.md`](PROJECT.md) and fill it in with your partner during or right after your kickoff meeting: goals, deliverables, timeline, communication preferences, required tools, and constraints. Treat this as the shared source of truth and update it when scope changes.

### 5. Log your kickoff meeting

Copy `meetings/_TEMPLATE.md` to `meetings/YYYY-MM-DD-kickoff.md` and fill it in.

### 6. Add a personal email to your GitHub account

Go to **GitHub → Settings → Emails** and add an email you will keep after you leave Brown, so you never lose access to your account or your repo.

---

## Folder guide

| Folder / file | What goes here |
|---|---|
| `PROJECT.md` | Project charter: partner, goals, deliverables, timeline, constraints |
| `meetings/` | One file per meeting, named `YYYY-MM-DD-topic.md` |
| `planning/` | `roadmap.md` (milestones) and `weekly-log.md` (done / blocked / next) |
| `docs/` | Decision log, user guides, handoff notes, and reference materials |
| `docs/user-guide/` | Instructions written for your partner or non-technical users |
| `data/` | Data folders  |
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

- **Decisions:** record important choices and the reasoning in `docs/decisions.md`. Future you and your partner will thank you.
- **Documentation:** write for someone who was not in the room. Assume your partner may hand this project to a non-technical colleague.
- **Deliverables:** move work from `work-in-progress/` to `deliverables/` only when your partner has seen it or it is ready for review, and update `deliverables/README.md` with its status.

---

## Submitting your final work

1. **Make sure everything is committed and pushed** to your repo's main branch.
2. **Tag the final version** so there is a fixed snapshot to review, even if you keep editing later:
   ```bash
   git tag v1.0-final
   git push origin v1.0-final
   ```
3. **Send your instructor the link** to your repo and to the tag (`https://github.com/<your-username>/<your-repo-name>/releases/tag/v1.0-final`) by **`<final due date>`**. Send it the way you sent your week 1 link.

## End of term checklist

- [ ] `PROJECT.md` is up to date and reflects what was actually delivered
- [ ] Final deliverables are in `deliverables/` and indexed in its README
- [ ] `docs/user-guide/` is complete and has been tested by someone who did not write it
- [ ] `docs/handoff.md` says where final versions live (repo, shared drive, Kodiak, partner's system, etc.) and who owns them
- [ ] No sensitive data or credentials are in the repo or its history
- [ ] Code runs from a clean clone, with setup instructions in `src/README.md` or below
- [ ] Repo is still **Private** and your instructor and TA can open it
- [ ] Final version has been submitted
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


## Getting help

- Stuck on Git or GitHub? Ask us, or open an issue using the **task** template in `.github/ISSUE_TEMPLATE/`.
- Unsure whether something is safe to commit? **Ask first.**
- Need to change the scope of your project? Discuss it with your partner, then record the change in `PROJECT.md` and `docs/decisions.md`.
