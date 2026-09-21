# Working in this repo

## How the owner wants this done

- **Be concise.** Short answers. Findings, then the next action.
- **Walk through anything operational one step at a time.** One instruction,
  wait, next.
- **Only ask a question when the answer changes what happens next.**
- **Never push, and never commit without being asked.** Show what changed and
  wait. Version and tag every commit.
- The repo is public — GitHub Pages on a free plan only serves public repos.
  The owner has chosen to publish the family's names, photos and rota history
  as they are. Anything beyond that still needs asking first.

## Saving

The app was written as a Claude artifact, where a tick is published for every
viewer. On Pages there is no `window.claude`, so it runs in standalone mode:
every visitor can edit, and each device saves to its own `localStorage`. A tick
on one phone is not seen on another. Shared saving would need a backend.

## The shape of it

`site/` is the whole published site. The workflow copies it as-is, adds a
`robots.txt` that disallows everything, and deploys. There is no build step;
keep it that way unless one is genuinely needed.
