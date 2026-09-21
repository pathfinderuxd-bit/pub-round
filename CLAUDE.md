# Working in this repo

## How the owner wants this done

- **Be concise.** Short answers. Findings, then the next action.
- **Walk through anything operational one step at a time.** One instruction,
  wait, next.
- **Only ask a question when the answer changes what happens next.**
- **Never push, and never commit without being asked.** Show what changed and
  wait. Version and tag every commit.
- The repo is public — GitHub Pages on a free plan only serves public repos —
  so nothing private goes in it.

## The shape of it

`site/` is the whole published site. The workflow copies it as-is, adds a
`robots.txt` that disallows everything, and deploys. There is no build step;
keep it that way unless one is genuinely needed.
