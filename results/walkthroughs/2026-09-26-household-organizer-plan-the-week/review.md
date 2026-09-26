> ⚠ Avatar output, not customer evidence – household-organizer: 0 % E2+, critical assumptions tested 0 of 10. Mostly assumptions – treat as a guess.

# Walkthrough: household-organizer – FLOW-001 Plan the coming week together

Date: 2026-09-26 | Environment: https://doables.gelbkappe.de/ (live site) | Profile version: 1 | Account: display name "Hanna (DEMO household)" (no password; each run was a new user)
Runs: 2 | Demo data used: none (flow needs no uploads) | Previous walkthrough: none

Change requests become hypotheses at most. "Stable" = found in all runs.

Test data left on the live site: list "WG Woche 39 (DEMO)" – run 1 at /lists/3, run 2 at /lists/6.

## Review
### Fits my workflow
- Zero-setup start: name only, no email/password/install, done in seconds – fits organizing in gaps on the phone and peers who can't be forced onto a tool [E0: industry assumption] | stable
- Invite link that can be pasted into the WG WhatsApp group fits how the group already coordinates [E1: https://www.flatastic-app.com/en/, current tools WhatsApp] | stable
- Fast quick-add with Enter, due dates, sorting by date [E1: https://www.flatastic-app.com/en/] | stable
- "Today" view (Overdue / Today / Next 7 days across all lists) supports "check whether things got done before it becomes a conflict" [E0: industry assumption] | stable
- Open/Done counters and progress per list [E0: industry assumption] | stable
- Mobile layout with bottom nav, description and date folded behind a button [E0: industry assumption] | unstable (only run 1 checked the mobile nav in detail; run 2 worked on mobile throughout without complaint about it)

### Change requests
- Assign menu: when only the organizer is in the list, explain "invite people to assign them" and link to Share | because: the job "split the week among people" fails at the first try; critical assumption 1 (everyone sees who does what, so no nagging) [E0: industry assumption] | priority: high | stable
- Assign tasks to a placeholder name before the person has joined, connect it when they join | because: the plan is agreed at the flat meeting / Sunday evening and written down right then (flow step 1) [E0: industry assumption] | priority: high | stable
- Show "done by [name]" on completed tasks (ideally counts per person) | because: fairness disputes [E1: liastoeffler.de]; critical assumption 6 [E0] | priority: high | stable
- Recurring tasks with rotation (Bad: Jonas → Lea → Hanna) | because: weekly chores; without them the list is retyped every Sunday and dropped after a few weeks – critical assumption 3 [E0; E1: https://www.flatastic-app.com/en/] | priority: high | stable
- Reminders / nudges to the assignee from the tool, not from the organizer | because: pain #1 "cleaning police" [E1: liastoeffler.de] | priority: high (run 2) / medium (run 1) | stable
- Easier move to another device (QR code or short link instead of a secret token), no CLI text for household users, one term (key or token) | because: group members vary in tech affinity [E0: industry assumption] | priority: medium (run 1) / low (run 2) | stable
- Show undated open tasks in "Today" or add an "Open this week" group | because: chores without an exact day are still this week's work [E0: industry assumption] | priority: medium (run 2) / low (run 1) | stable
- Native "Share via…" / WhatsApp button next to Copy | because: organizing happens on the phone, the group lives in WhatsApp [E0; E1: current tools] | priority: medium | unstable
- "New list" button directly in the mobile empty state | because: zero-setup expectation on the phone [E0: industry assumption] | priority: low | unstable

### Where I would leave the tool
- Step 4 (assigning): can't give anyone a chore → writes "Jonas: Bad" into the title/description or posts the plan in WhatsApp again; stays the one who reminds [E1: liastoeffler.de, pain "cleaning police"] | stable
- After 2–3 weeks: no recurring chores, retyping the same list every Sunday [E0: critical assumption 3] | stable
- When a flatmate clears their browser and loses their identity (few will save a token) [E0: technical affinity varies] | unstable

### Core value touched
- The profile's "Core value – do not touch" section is still empty (phase 3), so nothing can be flagged formally. Both runs point to critical assumption 1 ("everyone can see who does what so the organizer doesn't have to nag") as only partly met: assignment works only after people join, and done tasks show no name. | stable

### No basis (ask real customers)
- Whether flatmates actually open the invite link and trust a name-only identity (both runs)
- Which reminder channel (push, email, WhatsApp) groups would accept (run 2)
- Whether "anyone with the link can join" feels safe enough for clubs under GDPR (run 2)
- Whether the sign-in token model works for families with older members (run 2)
- Whether households would pay (run 1)
- Whether a visible progress bar motivates or feels like being watched (run 1)

## Issues found (product defects, for the team)
| # | Step | What happened | Expected | Screenshot | Stable |
|---|---|---|---|---|---|
| 1 | 4 | Assign menu ("Whose job is this?") offers only "you" and "Anyone"; no hint that others must join first, no link to Share | Hint/empty state pointing to Share / invite | run-1/07-assign-menu.png, run-2/09-assign-menu.png | stable |
| 2 | 8 | Banner says "sign-in **key**", profile dialog says "sign-in **token**" | One consistent term | run-1/14-sign-in-key.png, run-2/15-sign-in-key.png | stable |
| 3 | 7 | Progress shows "16%" for 1 of 6 (16.7 %) | 17 % (rounding); cosmetic | run-1/13-list-done-filter.png, run-2/14-task-done.png | stable |
| 4 | 8 | Profile dialog shows developer CLI text (`DOABLES_TOKEN=<token> doables lists`) to every user | Hidden or under "advanced" | run-1/14-sign-in-key.png, run-2/15-sign-in-key.png | stable (run 1 as defect, run 2 as change request) |
| 5 | 7 | Welcome/profile promise the name is "shown next to the tasks you add and finish", but a completed task shows no name | Name on completed/added tasks, or remove the promise | run-2/14-task-done.png | unstable (both runs saw no name; only run 2 linked it to the promise – may only appear with >1 member) |
| 6 | 2 | Mobile empty state says "Press + next to 'Lists' in the menu", but the menu is collapsed behind the hamburger; no button of its own | Direct create button, or hint to open the menu | run-2/03-home-mobile.png, run-2/04-menu-open.png | unstable |
| 7 | 3 | Submitting a task with empty title gives no visible message (inputs kept) | Inline "Enter a task title" | run-1/05-empty-title-submit.png | unstable |

Not tested in either run: another person joining through the link, and signing in on a second device (needs a second browser identity).

## Compared with the previous walkthrough
- None – this is the first walkthrough of FLOW-001 for household-organizer.

## Run details
### Run 1

## Steps taken
| # | What I wanted to do (my workflow) | What I did in the product | Result (worked / confusing / failed / left the tool) | Screenshot |
|---|---|---|---|---|
| 1 | Get started quickly on a Sunday evening, with no setup | Typed "Hanna (DEMO household)" and pressed "Get started". There was no email and no password. | Worked. It took about 5 seconds. | 01-welcome.png, 02-home-empty.png |
| 2 | Write down this week's chores the way I would at the kitchen table | Pressed "+" next to "Lists" and typed "WG Woche 39 (DEMO)", then Enter | Worked. The empty state told me where the "+" is. | 03-list-created.png |
| 3 | Add 5–8 tasks, some with a due date and a short note | Added 6 tasks: Bad putzen (today, with a note), Müll/Altglas (Mon, with a note), Einkaufen (Fri, with a shopping list as the note), Küche wischen, Pflanzen gießen, Nebenkosten (yesterday, to test overdue) | Worked. Enter adds a task fast. Tasks sort by due date. Past dates show as "Yesterday". When I left the title empty, the form refused it and kept my note and date. | 04-task-form-filled.png, 05-empty-title-submit.png, 06-six-tasks.png |
| 4 | Assign chores to my flatmates | Opened "Assign this task" on "Bad putzen" | Confusing. "Whose job is this?" only offers me and "Anyone". Nothing says flatmates must join through the link before I can pick them. I could only assign the landlord task to myself, and it then showed "Yours". | 07-assign-menu.png, 08-assigned-to-me.png |
| 5 | Share the list in our WG WhatsApp group | Share → invite link → Copy | Worked. The button showed "Copied". The text is clear: "Anyone with this link can join, add tasks and tick them off." I did not test the flatmate's side of joining, because each session is a new user and I only had one session. | 09-share-dialog.png, 10-invite-copied.png |
| 6 | See what is due today and what is still open | Opened "Today" | Worked well. It groups tasks into Overdue / Today / Next 7 days across all lists. Tasks without a date (Küche, Pflanzen) don't appear there, only in the list's "Open" filter. | 11-today-view.png |
| 7 | Tick off one task | Ticked "Bad putzen" in Today | Worked. It moved to the list's Done filter and progress became "1 of 6". The done task shows no "done by" name. | 12-marked-done-today.png, 13-list-done-filter.png |
| 8 | Edge case: I come back later on my phone or laptop | Banner → "Show it" | Confusing. To use another device I have to copy a secret token and paste it there. The dialog calls it a "sign-in token" but the banner calls it a "sign-in key", and it shows a CLI command (`DOABLES_TOKEN=<token> doables lists`). | 14-sign-in-key.png |
| 9 | Use it on my phone, which is where I really organize | Resized to 390×844, then checked the list, the edit form and Overview | Worked. There is a bottom nav (Overview / Today / Mine / You), and description and due date fold behind a button. The edit form has no repeat option. | 15-mobile-list.png, 16-edit-task-mobile.png, 17-overview-mobile.png |

## Review
### Fits my workflow
- Starting really does take zero setup: a name and one tap. That is what I need, because I organize in gaps, on my phone [E0: industry assumption]. It also means my flatmates would not need an email or an app install, which could fix "getting everyone onto the same tool" [E0: industry assumption]. I couldn't check what the invite link looks like on their side.
- An invite link I can paste into the WG WhatsApp group fits how we already talk [E1: flatastic / WhatsApp as current tool]. The share text is honest and easy to follow.
- The "Today" view (Overdue / Today / Next 7 days) is exactly my weekly job "check whether things got done before it becomes a conflict" [E0: industry assumption].
- Adding tasks is fast, and a note field for the shopping items is useful [E1: https://www.flatastic-app.com/en/].

### Change requests
- In the assign menu, when only I am in the list, add a line like "Your flatmates aren't here yet. Share the invite link so you can give them tasks", with the Share button right there. | because: the job "split the week among people" fails at the first try, and the whole point for me is "everyone sees who does what so I don't have to nag" (critical assumption 1) [E0: industry assumption] | priority: high
- Let me assign a task to a name before that person has joined (a placeholder like "Jonas"), and connect it when they join. | because: we agree the plan at the flat meeting, and I write it down right then (flow step 1). Waiting for everyone to click a link first breaks that moment. [E0: industry assumption] | priority: high
- Show "done by [name]" on completed tasks, and ideally a simple count per person. | because: fairness disputes are my #3 pain [E1: liastoeffler.de]. Without names, the list can't settle "who did what". I only saw this with myself in the list, so it may appear once others join. | priority: high
- Add repeating tasks with a rotation (weekly Bad putzen, rotating between us). | because: recurring chores are my weekly job, and without them I would have to retype the list every Sunday (critical assumption 3) [E1: https://www.flatastic-app.com/en/] | priority: high. The list is usable for one week, but I would likely drop it after a few weeks without this.
- Let the task owner get a gentle nudge from the tool, not from me. | because: my #1 pain is being the "cleaning police" [E1: liastoeffler.de]. I found no reminders in this flow. | priority: medium
- Make moving to another device easier: a QR code or a short link instead of a secret token, and no CLI text for household users. Use one term (key or token). | because: "you come back on another device" is part of the flow. My flatmates vary in how tech-savvy they are [E0: industry assumption], and a scary "keep it secret" token will lose them. | priority: medium
- Show undated tasks in "Today", or add a "This week" group. | because: chores like "Küche wischen" often have no exact day, but they are still "this week's" work [E0: industry assumption] | priority: low

### Where I would leave the tool
- At step 4, assigning. I set up the whole week and then could not give anyone a chore. A busy organizer would type "Jonas: Bad" into the task title, or go back to WhatsApp. This is the point where I would decide whether to keep going.
- After 2–3 weeks, when there are no repeating chores and I am retyping the same list every Sunday.

### Core value touched
- The profile has no defined core value yet (it comes in phase 3). The nearest thing is critical assumption 1, "everyone can see who does what so the organizer doesn't have to nag". Assignment only works after people join, and done tasks show no name, so this central promise was not shown in this solo run.

### No basis (ask real customers)
- Whether my flatmates would actually click the invite link and trust a name-only identity. I have no basis for that; you should ask real customers.
- Whether households would pay for this. I have no basis for that; you should ask real customers.
- Whether the plain "16 % progress" bar motivates people or feels like being watched. I have no basis for that; you should ask real customers.

## Issues found (product defects)
| # | Step | What happened | Expected | Screenshot |
|---|---|---|---|---|
| 1 | 7 | With 1 of 6 done, progress shows "16%" in the list and in Overview (1/6 = 16.7 %) | Rounded to 17 % | 13-list-done-filter.png, 17-overview-mobile.png |
| 2 | 8 | The banner says "Save your sign-in **key**" but the dialog says "Your sign-in **token**" | One consistent term | 14-sign-in-key.png |
| 3 | 8 | The profile dialog shows developer CLI text (`DOABLES_TOKEN=<token> doables lists`) to every user | Hidden or tucked into an "advanced" section for non-technical users | 14-sign-in-key.png |
| 4 | 4 | The assign dropdown has only "you" and "Anyone". There is no hint or link to invite people. | An empty-state hint that points to Share | 07-assign-menu.png |
| 5 | 3 | Submitting with an empty title gives no visible message. The form just does nothing (my inputs were kept). | A short inline "Enter a task title" | 05-empty-title-submit.png |

No console errors, failed requests or broken pages came up during the run.

Test data left on the live site: the list "WG Woche 39 (DEMO)" (/lists/3), owned by the user "Hanna (DEMO household)".

### Run 2

## Steps taken
| # | What I wanted to do (my workflow) | What I did in the product | Result (worked / confusing / failed / left the tool) | Screenshot |
|---|---|---|---|---|
| 1 | Open the app on my phone on Sunday evening and get started with zero setup | Opened the site, typed "Hanna (DEMO household)", tapped "Get started", switched to a 390×844 phone viewport | Worked. Name only, no email, done in seconds | 01-welcome.png, 02-home-empty.png, 03-home-mobile.png |
| 2 | Create a list for this week | The empty state says to press + next to "Lists" in the menu. On the phone that's hidden behind the hamburger. Opened it, tapped +, typed "WG Woche 39 (DEMO)", pressed Enter | Worked, but a little confusing on mobile: the empty state has no create button of its own | 04-menu-open.png, 05-list-created.png |
| 3 | Add 5–8 tasks, some with a due date and description | Added 6 tasks. 3 have dates (today, Sep 28, Sep 30) and 2 have descriptions. Title plus Enter is fast; dates and descriptions sit behind a small icon button | Worked. Tasks sort by due date and "Today" is labelled | 06-task-form-expanded.png, 07-first-task.png, 08-six-tasks.png |
| 4 | Assign "Bad putzen" to Jonas, the shopping to me | The assign menu ("Whose job is this?") only offers "Hanna (you)" and "Anyone". I couldn't assign Jonas and there's no hint to invite him first. Workaround: wrote "Jonas ist dran" in the description. Assigned the shopping to myself, which shows "Yours" | Failed for other people (they aren't in the list yet). Assigning myself worked | 09-assign-menu.png, 10-assigned-self.png |
| 5 | Share the list with my flatmates via the WG chat | Share opens an invite link with Copy, "Create a new link", and People (1): me as Owner | Worked. The link is easy to paste into WhatsApp. There's no native share / WhatsApp button, and I couldn't check the Copy feedback in the snapshot | 11-share-dialog.png, 12-share-copied.png |
| 6 | Check what's due today and what's still open | "Today" view: 1 task under Today, 2 under "Next 7 days", across all lists. For open tasks I used the list's "Open" filter | Worked, but tasks without a date (Altglas, Papiermüll, Klopapier) don't appear in Today, so I have to check two places | 13-today.png |
| 7 | Mark one task as done | Ticked "Altglas wegbringen". Counters show 5 open, 1 done, 16 %, and the task moves to the bottom | Worked. No "done by Hanna" is visible on the task | 14-task-done.png |
| 8 | Edge case: come back later on another device | Banner "Save your sign-in key" leads to Profile, with a masked token, Copy button, and CLI hint | Confusing for my group. Welcome page has "Already use Doables on another device?" | 15-sign-in-key.png |

## Review
### Fits my workflow
- Getting started with only a name and no email, install or account is exactly the low-friction entry I need. My flatmates are peers I can't force onto a tool [E0: industry assumption, Decision power]. It also fits the mixed-device problem, since iCloud lists exclude Android [E0: pain point "Getting everyone onto the same tool"].
- A share link I can paste into the WG WhatsApp group matches how we already coordinate [E1: Current tools WhatsApp/Signal].
- Quick-add with Enter, due dates, and the Today / Next 7 days view cover "keep chores visible" [E1: JTBD weekly chores, flatastic].
- Open/Done counters and progress let me "check whether things got done before it becomes a conflict" without asking around [E0: JTBD check].

### Change requests
- Let me assign tasks to people who haven't joined yet (placeholder name that the person claims on joining), or at least say "Invite people to assign them" in the assign menu, linked to Share | because: my main value is "everyone sees who does what so I don't have to nag". Right now I plan Sunday evening, but the names only work once each flatmate has clicked the link [E0: critical assumption 1; pain point "cleaning police", E1 liastoeffler] | priority: high
- Recurring tasks with a rotation (Bad: Jonas, then Lea, then Hanna) | because: a weekly list without rotation means rebuilding it every Sunday, and this is the habit that makes or breaks the tool [E0: critical assumption 3; E1: flatastic] | priority: high
- Show who completed a task ("erledigt von Jonas") | because: the welcome text promises it, and fairness disputes need it [E1: pain point "Disputes about fairness"; E0: critical assumption 6] | priority: high
- Reminders or notifications for assigned people when a task is due | because: without them I'm still the one sending the WhatsApp nag [E1: pain point "cleaning police"] | priority: high (no basis for which channel; see below)
- A native "Share via…" or WhatsApp button next to Copy | because: I do this on my phone and our group lives in WhatsApp [E0: Time budget "almost always on the phone"; E1: Current tools] | priority: medium
- In Today, show undated open tasks too, or add an "Open this week" view | because: I want to see "due today plus still open" in one place [E0: JTBD check] | priority: medium
- Put a "New list" button directly in the empty state on mobile | because: I expect zero setup on the phone [E0: Time budget] | priority: low
- Hide the CLI hint for normal users and use the same word ("key" or "token") everywhere | because: others in my group vary in tech affinity [E0: Time budget and technical affinity] | priority: low

### Where I would leave the tool
- At step 4. If I can't write "Jonas: Bad" on Sunday evening, I'll post the plan in WhatsApp again. The list becomes only a checklist and I'm still the one reminding people [E1: pain point "cleaning police"].
- After 2–3 weeks if I have to retype the same chores every week with no recurrence [E0: critical assumption 3].
- If a flatmate clears their browser and loses their identity. The warning is clear, but most of my group won't save a token [E0: technical affinity varies].

### Core value touched
- The "Core value – do not touch" section is still empty (phase 3), so nothing can be formally flagged. The nearest thing is critical assumption 1, "Everyone can see who does what, so the organizer doesn't have to nag", and it's only partly met: assignment works only after people join, and nothing shows who completed a task.

### No basis (ask real customers)
- Whether flatmates will actually open a link and enter a name, or ignore it: I have no basis for that – you should ask real customers.
- Which reminder channel (push, email, WhatsApp) groups would accept: I have no basis for that – you should ask real customers.
- Whether "anyone with the link can join" feels safe enough for clubs under GDPR: I have no basis for that – you should ask real customers.
- Whether the sign-in token model is acceptable for families with older members: I have no basis for that – you should ask real customers.

## Issues found (product defects)
| # | Step | What happened | Expected | Screenshot |
|---|---|---|---|---|
| 1 | 7 | Welcome and profile say the name is "shown next to the tasks you add and finish", but the completed task "Altglas wegbringen" shows no name | Name on completed tasks (and on added tasks), or the promise removed | 14-task-done.png |
| 2 | 2 | On mobile the empty state says "Press + next to 'Lists' in the menu", but the menu is collapsed behind the hamburger and the empty state has no button of its own | A direct create button in the empty state, or a hint to open the menu | 03-home-mobile.png, 04-menu-open.png |
| 3 | 4 | The assign menu offers only "you" and "Anyone", with no explanation of how to add other people | An explanation or link to Share / invite | 09-assign-menu.png |
| 4 | 8 | Inconsistent wording: the banner says "sign-in key", the profile says "sign-in token" | One term everywhere | 15-sign-in-key.png |
| 5 | 7 | Progress shows "16%" for 1 of 6 (16.7 %) | 17 % (rounding); cosmetic | 14-task-done.png |

Not tested: another person joining through the link, and signing in on a second device. Both need a second browser identity, and I only had one session.

Test data left on the live site: "WG Woche 39 (DEMO)" at https://doables.gelbkappe.de/lists/6.
