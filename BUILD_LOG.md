# 🛠️ Build Log — Facebook Flier Bot

Time tracked task-by-task in a live tracker. Times are estimated from session timestamps.

| Date | Time | Running total |
|---|---|---|
| Oct 22, 2026 | 36m | 0h 36m |
| Oct 26, 2026 | 1h 35m | 2h 11m |
| Oct 27, 2026 | 52m | 3h 03m |
| Oct 29, 2026 | 24m | 3h 27m |
| Nov 2, 2026 | 2h 29m | 5h 56m |
| Nov 5, 2026 | 2h 06m | 8h 02m |
| Nov 6, 2026 | 1h 23m | 9h 25m |
| Nov 9, 2026 | 26m | **9h 51m** |
| Nov 9, 2026 (part 2) | 53m | **10h 44m** |
| Nov 9, 2026 (part 3) | 45m | **11h 29m** |
| Nov 13, 2026 | 1h 06m | **12h 35m** |
---

## Oct 22, 2026 — Planning and client guide (36m)
- Checked Make.com free plan limits (1,000 credits/month, 2 active scenarios) and planned a $0 build
- Designed a 6-page client guide (kawaii Halloween / Día de los Muertos theme) with a how-it-works overview, an info checklist, 12 monthly flier ideas, a sample flier, and a GitHub sharing permission page
- Client approved the build and all sharing options

## Oct 26, 2026 — Google setup and first Make modules (1h 35m)
- Reviewed the client's answers and photos
- **Decision:** run the bot on my own free Make account for now, and move it to the client's account if she decides to pay later
- Built the Google Drive folders and the **Flier Queue** Sheet (Month, Theme, Flier Link, Caption, Post Date, Status, Posted On, Notes) with a Status dropdown
- Make: **Search Rows** (Status = Approved) → **Download a File** → **Update a Row** (Status = Posted, date stamped)
- **Fix:** Drive file ID was piece 5 of the split link, not 6
- Designed the review step: added an **In Review** status instead of a new column

## Oct 27, 2026 — Facebook access blocker (52m)
- Made a Facebook account so the client could add me as a Page admin
- **Blocker:** her Page is in a Meta business portfolio, and the invite failed twice ("User Cannot be Added to Business")
- The new account was flagged and permanently banned
- **Decision:** backup plan. The client logs in herself during the Make connection
- **Lessons:** default to the client connecting their own accounts; ask early whether the Page is in a business portfolio; never make a new, empty Facebook account for client work

## Oct 29, 2026 — Plan changes (24m)
- **Plan change:** Instagram removed; Facebook only
- Planned the connection session: the client must type her own login, in person or over Zoom with remote control
- Added **In Review** to the Status dropdown

## Nov 2, 2026 — Review path, AI experiment, Facebook module (2h 29m)
- Search filter: Approved OR Pending; added a **Router** with filtered paths
- **Pending path:** Gmail review email (month, theme, post date, flier link, caption) → Status = In Review. Tested ✅
- **Experiment:** auto-generated fliers with the OpenAI image API (gpt-image-2.5-flare). Compared model pricing (~$0.04–$0.17 per flier)
- Two test rounds (~$0.20) didn't match the approved flier style → **dropped**; ChatGPT stays the flier designer
- Removed the generate path; added Facebook Pages **Upload a Photo** to the Approved path
- Caught the default 15-minute schedule (~2,900 credits/month) → switched to manual runs
- Planned future timing: batch-made fliers, client approves one per month

## Nov 5, 2026 — Go live! (2h 06m)
- Connection session over Zoom with remote control; the client typed her own Facebook login
- **Gotcha:** the browser tried to connect my account first, so I logged out of Facebook before retrying
- The client logging in through her personal profile is normal: Pages are managed through personal Facebook accounts
- Configured Upload a Photo: her Page, the flier from the Drive download, and the caption from the Sheet
- End-to-end test passed; added the client to the review email
- 🎉 **First real flier ("Fall in Love," Nov 2026) posted live to her Facebook Page**
- 
## Nov 6, 2026 — GitHub case study (1h 23m) · Running total: 9h 25m
- Created this repo and wrote the README case study: problem, Mermaid flow diagram, status flow, tools and costs, challenges and lessons
- Added screenshots: the Make scenario, the review email, and the live Facebook post
- Wrote this build log from the time tracker
- 
## Nov 9, 2026 — Docs, blueprint, privacy cleanup (26m) · Running total: 9h 51m
- Added `docs/sheet-layout.md` (Google Sheet columns, status dropdown, tips)
- Added a public version of the client guide: last name removed, contact info blurred
- Exported the Make scenario and sanitized it (connection IDs, Sheet/Page IDs, emails, and client details removed) with import instructions

## Nov 9, 2026 — Monthly automation + December flier (53m) · Running total: 10h 44m
- Removed the leftover "Generate" filter rule from the live scenario
- Made the December "Gift of Gorgeous" flier with ChatGPT: kept Rylee the same, changed everything else (scene, colors, layout)
- Caught an unconfirmed "gift cards" line before it went on a flier and replaced it with a booking-urgency line
- **Automated monthly timing:** the scenario runs on the 23rd and the 1st
  - Pending path emails the flier for review when its Post Date is within 8 days
  - Approved path posts the flier when its Post Date has arrived
- Raised the search limit to 20 rows so batched fliers are all visible
- Safety test passed: the December flier was found but correctly not emailed early

- 
## Nov 9, 2026 — Batched fliers + automation ON (45m) · Running total: 11h 29m
- Made January ("New Year, New You!"), February ("Love Your Hair"), and March ("Lucky Locks!") fliers, each with a new scene and colors while keeping Rylee consistent
- Skipped a champagne idea for January since the client is under 21; used a "snipping the 2026 streamer" scene instead
- Loaded all fliers into the Sheet as Pending with Post Dates on the 1st
- 🚀 Turned the scenario ON. First automatic review email: Nov 24. First automatic post: Dec 1

- 
## Nov 13, 2026 — Spring and summer fliers (1h 06m) · Running total: 12h 35m
- Made April ("Frizz-Free Season"), May ("Treat Mom!"), and June ("Summer Glow Up") fliers; all queued as Pending with Post Dates on the 1st
- Added "mostly platinum blonde on top" to prompts so the character's hair stopped drifting pinker
- Fixed a misspelling ("Custom Color") on the June flier and swapped an outfit that looked too similar to May's
- Moved the monthly review email from the 24th to the 23rd and widened the date rule to 10 days to cover 31-day months
- 7 fliers now queued (December 2026 through June 2027)
