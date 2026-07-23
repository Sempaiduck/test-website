# Project Context

## What this is
Andrew (GitHub: Sempaiduck) is starting a small business building and selling websites to local companies — either a one-time build fee, a monthly hosting/maintenance retainer, or a hybrid of both. This is early-stage / practice work, learning the full pipeline before pitching real clients.

## Tech stack & workflow (already working end-to-end)
- **Sites are static HTML/CSS/JS** for now — no backend, no database. Fine for most small business sites (menus, hours, contact info, photos). Backend/database only needed later for bookings, logins, or e-commerce — save that for clients who specifically need it, and price those jobs higher.
- **Version control:** Git + GitHub. Windows machine, using Git Bash (MINGW64).
  - Git is configured: `user.name = "Sempaiduck"`, `user.email = "andrewandanthonyvang@gmail.com"`
  - `CLAUDE_CODE_GIT_BASH_PATH` should be set to `C:\Program Files\Git\bin\bash.exe` (fixes the "Git is required for local sessions" error in Claude Code desktop on Windows)
- **Hosting/deploy:** Vercel, connected to GitHub via OAuth. Every `git push` to `main` auto-redeploys the live site — no manual redeploy needed.
- **Test repo:** `github.com/Sempaiduck/test-website`, live at `test-website-delta-three.vercel.app`. Contains a one-page demo site (see below). This proves the full pipeline works.

## Standard git workflow for updates
```
cd path/to/project
git add .
git commit -m "describe the change"
git push
```
(First time only, per new project: `git init`, `git branch -M main`, `git remote add origin <repo-url>`, `git push -u origin main`.)

## Design tooling
Installed the `ui-ux-pro-max` skill (github.com/nextlevelbuilder/ui-ux-pro-max-skill) for design intelligence — auto-activates on UI/UX requests in Claude Code. Use it when building new sites: mention the business type/industry and preferred stack (defaults to HTML+Tailwind) to get tailored style/color/typography recommendations.

## Demo site built so far
A one-page landing page for a fictional coffee shop ("Waypoint Coffee") — dark espresso-brown palette, Fraunces (serif display) + Space Grotesk (body), with a coffee-ring "stamp" badge as the signature visual element reused across section labels. Sections: hero, about, menu (chalkboard style), hours/location, footer CTA. This is the current `index.html` in the test-website repo — a reference point for the visual quality bar to aim for on future sites (distinctive, not templated-looking).

## Business model notes (undecided/in progress)
- Hosting under Andrew's own Vercel/GitHub account is the likely default (simpler multi-client management, supports recurring billing), vs. deploying under the client's own accounts (client owns everything outright).
- Pricing not yet finalized — considering one-time build fee + optional monthly retainer for hosting/updates/support.
- Not yet started: real client outreach, contracts, connecting a custom domain (only tested on free `.vercel.app` subdomain so far).

## How Andrew works / preferences
- Newer to Git/terminal workflows — walk through commands one at a time rather than large batches, and explain what each step does.
- Prefers being told the reasoning behind an error before the fix (e.g. "this failed because X, so try Y").
