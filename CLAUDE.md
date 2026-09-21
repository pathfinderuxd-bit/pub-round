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

Shared through a Google Sheet in Rich's Drive ("Pub Round data"), behind an Apps
Script web app deployed as *Execute as: Me, Access: Anyone*. No logins. The URL
is `REMOTE` in site/index.html.

- The script stores the whole state as JSON down column A, in 45,000-character
  chunks (a cell holds 50,000), each prefixed `~` so Sheets never reads one as a
  formula. GET returns it; POST replaces it.
- Each phone also keeps a copy in localStorage: the app opens from that
  instantly, then pulls. Newest `updatedAt` wins. It pulls on open and whenever
  the app returns to the front.
- POST is sent as text/plain on purpose — Apps Script cannot answer a CORS
  preflight, so an application/json POST fails.
- Editing the script does nothing until **Deploy → Manage deployments → edit →
  Version: New version**. The /exec URL keeps serving the old code otherwise.
- Anyone with the /exec URL can write. The owner accepted that; the script only
  accepts something with a `history` array.
