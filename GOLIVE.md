# Team Member Care Tracker — Go Live
_Maintained by Claude. Reflects current project state._

## Status
Local

## What It Is
A browser-based care tracking tool for TLC Houston Levee production team members — logs meetings, conversation notes, prayer needs, next steps, Life Group attendance, and follow-up actions. Used by a small team of ministry staff.

## Active Services
_Updated when IT provisions something._

| Service | Used for | Env var | Status |
|---|---|---|---|
| _(none yet — see Notes)_ | | | |

## Hosting
- Platform: Firebase (recommended) — IT advises
- URL: not yet deployed
- GitHub repo: still local — IT creates org repos

## Database
- Needs a database: **Yes** — for real-time shared access across team members
- What gets stored: team member records with meeting logs, prayer needs, next steps, life group attendance, and follow-up action items
- Access pattern:
  - [x] Only logged-in users can read and write
- Current state: using browser localStorage (single-user) with JSON export/import as a workaround

## Login / Authentication
- Needs login: **Yes** — staff-only tool
- How: Google sign-in, restricted to @thelifechurch.com accounts
- Current state: no auth yet (local only)

## Notes for IT
- Single-file app (index.html) — no build step, no dependencies
- Currently stores data in localStorage; needs Firestore for shared access
- Auth pattern: standard TLC Google sign-in (firebase-auth-gatekeeper)
- Small team of users — light read/write load
- Ready to hand off whenever hosting + auth + database can be provisioned
