# Claude Code Prompt — Nepal Disaster Resilience Open Source Platform Setup

Copy everything below into Claude Code:

---

I'm setting up a GitHub repository for an open source project. Here's the context and what I need you to build, end to end.

## Project Context

This is an open source initiative to close gaps in disaster-response systems for Nepal, covering four areas: weather forecasting, flood detection, landslide detection, and fire detection.

- We'll audit existing sensors, data sources, and current systems to find where coverage is weak.
- We'll build ML models and a mobile/web application to address the gaps.
- The base version will be fully open source (MIT or Apache 2.0 — recommend one). Anyone may fork it and build a commercial product on top.
- Idea submission will be centralized: contributors submit ideas via structured GitHub Issue Forms, not free-text issues.
- Submitted ideas get triaged and tracked on a GitHub Projects board with both a Table view and a Timeline view.
- The most viable/approachable idea gets selected as the initial base project.
- Mentors/owners will be assigned to oversee code review, merges, and feature testing.

## What I need you to build

1. **Repo structure**
   - Initialize a clean repo structure suitable for a multi-track open source project (`/docs`, `/data`, `/models`, `/app`, `/.github`).
   - Add a LICENSE file (recommend MIT unless you see a reason for Apache 2.0 given the commercial-fork intent — explain your choice).

2. **Issue Forms (not plain issue templates)**
   - Create `.github/ISSUE_TEMPLATE/idea-submission.yml` as a structured GitHub Issue Form with fields:
     - Hazard type (dropdown: Weather Forecasting / Flood Detection / Landslide Detection / Fire Detection / Other)
     - Problem statement (textarea, required)
     - Proposed approach (textarea, required)
     - Data/sensors needed or available (textarea)
     - Estimated impact/viability (textarea)
     - Submitter name/contact (text, optional)
   - Also create a separate lighter-weight `.github/ISSUE_TEMPLATE/bug-feature.yml` for regular bug reports/feature requests once development starts.
   - Disable blank issues in `.github/ISSUE_TEMPLATE/config.yml` so all submissions go through a form.

3. **GitHub Projects board**
   - Set up a GitHub Projects (v2) board named "Idea Pipeline."
   - Configure a status field with these stages: `Submitted → Under Review → Selected → In Development → Merged/Shipped`.
   - Add custom fields: Hazard Type, Mentor/Owner, Submission Date.
   - Configure both a Table view (default, sortable/filterable) and a Timeline view (grouped by submission → review → selection dates).
   - Set up automation so new issues from the idea-submission form are auto-added to the board in "Submitted" status.
   - Note: if the GitHub CLI/API can't fully automate Projects v2 setup, give me exact step-by-step manual instructions instead.

4. **Governance docs**
   - Create `GOVERNANCE.md` explaining: mentor/owner roles, code review process, merge criteria, feature-test requirements, and how the open-source-vs-commercial-fork policy works.
   - Create `CONTRIBUTING.md` explaining how to submit an idea, how the review pipeline works, and coding standards.
   - Create a minimal, clean `README.md` — short mission statement, link to the idea submission form, link to the live Projects board, link to GOVERNANCE.md and CONTRIBUTING.md. Do NOT make this a long-form document; keep it under 40 lines and point elsewhere for detail.

5. **GitHub Pages landing site**
   - Build a single polished landing page (`/docs/index.html` or a `gh-pages` branch, your call — tell me which and why) that:
     - States the mission (Nepal disaster resilience, open source + commercial-friendly)
     - Has a clear "Submit an Idea" button linking to the issue form
     - Embeds or links to the live Projects board
     - Looks professional and modern — not a default GitHub theme. Use clean typography, a hazard-relevant color palette (e.g., weather blues, alert oranges), and a simple responsive layout. No generic template look.
   - Set up GitHub Pages deployment (via Actions or branch, whichever is simpler) so this goes live automatically.

## Constraints & preferences

- Keep everything native to GitHub (Issue Forms, Projects, Pages, Actions) — no third-party SaaS tools.
- Ask me before making irreversible choices (e.g., license type, org vs personal repo, public vs private during setup).
- If any of this can't be automated via CLI/API (e.g., some Projects v2 configuration), tell me clearly and give manual steps instead of skipping it silently.
- When done, give me a summary of what was created, what I still need to do manually, and the URLs/paths for everything.

---
