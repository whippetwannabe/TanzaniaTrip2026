# Claude Code Instructions — Tanzania Trip Hub

## Project
Maintain the Tanzania Trip 2026 static site at https://whippetwannabe.github.io/TanzaniaTrip2026/  
GitHub repo: whippetwannabe/TanzaniaTrip2026  
File to maintain: `index.html`

---

## Workflow

**Source of truth: `TRIP_CONTEXT.md` in this folder.**  
When Matt gives you updates, first check if `TRIP_CONTEXT.md` is already current. Then:

1. Read `TRIP_CONTEXT.md` fully before touching `index.html`
2. Apply all changes from the "Known Issues" section and any new updates Matt describes
3. Edit `index.html` to match
4. After editing, clear the fixed items from the "Known Issues" section in `TRIP_CONTEXT.md` and update the "Last updated" date at the top
5. Commit and push: `git add index.html TRIP_CONTEXT.md && git commit -m "Update: <brief description>" && git push`
6. GitHub Pages redeploys in ~1 minute

---

## index.html Structure

Single-file app · all CSS and JS inline · no external dependencies  
**7 tabs:** Itinerary · Hotels · To-Do · Gear · Weight · Budget · Health  
**5 phase selectors** (filter view by trip phase)  
Fully interactive — checkboxes, phase filters, responsive layout

---

## Key Rules

- **Never break the single-file structure.** All CSS and JS stays inline in `index.html`.
- **Match TRIP_CONTEXT.md exactly.** If the context file says something is purchased/completed, the hub must reflect that.
- **Preserve interactivity.** Don't remove or simplify JavaScript functionality when making content edits.
- **Update both files.** After fixing issues in `index.html`, remove them from the "Known Issues" section in `TRIP_CONTEXT.md`.
- **Commit message format:** `"Update: <what changed>"` e.g. `"Update: gear tab purchases, budget totals, May 24 items"`

---

## Cowork ↔ Claude Code Split

| Tool | Responsibility |
|---|---|
| Cowork | Matt tells it what's changed → it updates `TRIP_CONTEXT.md` · keeps memory across sessions |
| Claude Code | Reads `TRIP_CONTEXT.md` → updates `index.html` → pushes to GitHub |

When working in Claude Code, always pull latest before editing:  
`git pull origin main`
