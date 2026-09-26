> ⚠ Avatar output, not customer evidence – task-contributor: 0 % E2+, critical assumptions tested 0 of 10. Mostly assumptions – treat as a guess.

# Walkthrough: task-contributor – FLOW-002 Join a shared list and get my tasks done

Date: 2026-09-26 | Environment: https://doables.gelbkappe.de/ (live site) | Profile version: 1 | Account: display name "Kai (DEMO contributor)" (no password)
Runs: 2 | Demo data used: none | Previous walkthrough: none

Change requests become hypotheses at most. "Stable" = found in all runs.

**Limit of both runs:** no invite link was available, so neither run could join a list as a guest. Steps 3–6 of the flow were tested on a list each run created itself, so "Kai" was the list owner, not an invited member. Neither run tested signing in on a second device.

Demo data left on the live site: "Week tasks (DEMO)" /lists/5 (run 1) and /lists/8 (run 2), each with DEMO tasks and one DEMO comment, owned by "Kai (DEMO contributor)".

## Review
### Fits my workflow
- Getting started asks only for a name: no account, email, password, or install, and it takes seconds. This supports the critical assumption "only join if it takes no account…" and removes the pain point about accounts and passwords [E0: industry assumption] | stable
- "My tasks" and "Today" across all lists, plus the "Yours" badge, answer "what's mine, what's due today" in one tap and fix "unclear whether a task is theirs" [E1: flowhubr] | stable
- Ticking a task off takes one click and progress updates right away, so nobody needs a "done" message [E1: mein-handwerker-app.de] | stable
- Comments sit on the task, so questions stay next to it instead of getting lost in chat [E0: industry assumption] | stable
- The phone layout has a bottom bar (Overview / Today / Mine / You) within thumb reach [E0: industry assumption] | stable
- The welcome text says openly that your name is shown to people you share lists with [E0] | unstable (run 1)

### Change requests
- Give people without a link a way to join: add "Got an invite link? Paste it here" on the welcome page and in the empty state, and change the empty state from "Create your first list" to a hint like "Waiting for a list? Ask for the invite link" | because: the "Join a list from a link someone sent in chat" job; a dead end here means going back to chat [E1: MS To Do share/join failures; E0: drifts back to chat] | priority: high | stable
- Make getting onto the phone one step, with a QR code or a "send to my phone / to myself in WhatsApp" link, instead of copying a token by hand | because: the "Get back into my lists on a new phone" job; technical skill varies, including trades workers [E1: bitkom Handwerk]; critical assumption about keeping the sign-in key | priority: high | stable
- Show "Done by Kai · time" on finished tasks | because: others should see without a message that I did my part (the fair-share KPI) [E1: mein-handwerker-app.de; E1: liastoeffler] | priority: medium (run 1) / high (run 2) | stable
- Let people comment directly from Today and My tasks | because: seconds per visit, no need to open the full list [E0] | priority: medium | stable
- Use one term for the sign-in secret ("key" vs "token") and hide the CLI line from non-technical users | because: skill range and first-use success [E1: bitkom Handwerk; E0: English UI assumption] | priority: high (run 1) / medium (run 2) | stable
- Shorten the permanent "Save your sign-in key" warning, or make it dismissible or shown once | because: seconds per visit; it feels like homework for a tool I didn't choose [E0] | priority: medium (run 1) / low (run 2) | stable
- Offer a German UI | because: DACH users, trades workers, older club members [E1: bitkom Handwerk; E0: English UI assumption] | priority: medium | unstable (run 1)
- Test joining by invite link inside the in-app browsers of chat apps on phones | because: joins fail often in other tools [E1: MS To Do "can't join list"] | priority: high | unstable (run 1)

### Where I would leave the tool
- Arriving without an invite link (flow step 2): the app only offers "Create your first list" → ask in chat "where's the link?", or keep replying "done" in chat and let the list go stale [E0: drifts back to chat] | stable
- Switching to a new phone: the only way back in is a token copied by hand (or a new invite, which would make me a different person in the list) → stick with the first device, or quietly stop using it [E0] | stable

### Core value touched
- None can be checked: the profile's core value section is still empty (it gets filled in phase 3). Both runs flagged token-only recovery as the weak point if "join with no account" becomes the core value.

### No basis (ask real customers)
- Whether showing names next to finished tasks and a "Progress %" feels like being watched at work (stable)
- Whether contributors come back without push notifications or a chat nudge; the app offered no notifications (stable)
- Behavior offline or with a weak signal on site; not tested (stable)
- Whether contributors really use the list instead of replying "done" in chat (unstable, run 1)

## Issues found (product defects, for the team)
| # | Step | What happened | Expected | Screenshot | Stable |
|---|---|---|---|---|---|
| 1 | 2 | No way in the UI to join someone else's list without the full /join/ URL: no paste field or code entry, and empty states only suggest creating a list | A visible join/paste option, or at least a hint to ask for the invite link | run-1/03-empty-dashboard.png, run-2/03-first-home.png, run-2/04-my-tasks-empty.png, run-2/07-new-list-dialog.png | stable |
| 2 | 6 | A finished task shows no finisher name or time, although welcome/profile promise your name appears "next to the tasks you add and finish" (only the owner's view was checked) | A "Done by [name] · time" label | run-1/13-task-done.png, run-2/14-task-done.png | stable |
| 3 | 7 | The same secret has several names: "sign-in key" (banner), "sign-in token" (profile), "token (from your Profile)" (welcome) | One term everywhere | run-1/04-profile-token.png, run-2/06-profile-token.png | stable |
| 4 | 5 | Today and My tasks rows have Edit/Delete but no Comment button; list rows do | The same row actions in every view | run-1/11-today.png, run-2/12-today-view.png | stable |
| 5 | 7 | "Show it" on the sign-in key banner opens Profile with the token still masked | Reveal the key (or a QR code) | run-2/16-show-sign-in-key.png | unstable |
| 6 | 3 | The same view is called "My tasks" on desktop and "Mine" on phone | Consistent label | run-2/18-phone-today.png | unstable |
| 7 | 1 | Console: "Password field is not contained in a form" (hidden token field) | Put the field inside a form | – | unstable |

## Compared with the previous walkthrough
- **Resolved:** – (no previous walkthrough)
- **Still open:** –
- **New:** all findings

## Run details
### Run 1

#### Steps taken
| # | What I wanted to do (my workflow) | What I did in the product | Result | Screenshot |
|---|---|---|---|---|
| 1 | Open the app from the chat message and get started fast | Opened the base URL, got sent to /welcome, typed "Kai (DEMO contributor)" and clicked "Get started" | Worked. No password, no email, no app to install, and it took seconds. | 01-welcome.png |
| 2 | Understand the "other device" option before starting | Opened "Already use Doables on another device?", which shows a field to paste a token | Confusing. I don't have a token yet, and the text doesn't say where to get one besides "(from your Profile)". | 02-other-device-token.png |
| 3 | Get to my colleague's shared list | Looked at the empty dashboard. It only says "Create your first list… then invite others". There is no "join a list" option and no field to paste a link. | Failed. Nothing tells a new person that someone else has to send them a link. As Kai I would go back to the chat and ask "which link?", or just give up. | 03-empty-dashboard.png |
| 4 | Check whether "+ New list" lets me join | Clicked "+", which only asks for a list name | Failed. There is no join option here either. | 07-new-list-no-join-option.png |
| 5 | Save my sign-in details as the banner tells me | Clicked "Show it" in the banner. It opened a Profile dialog titled "sign-in token", with a CLI line in it | Confusing. The banner says "sign-in key" and the dialog says "token". The CLI line means nothing to me. The yellow warning stays on every page. | 04-profile-token.png |
| 6 | (Stand-in) Test the rest of the flow on a list | I couldn't join a real list, so I created "Week tasks (DEMO)" and a task "Buy milk for the kitchen (DEMO)" due today. I also looked at the Share dialog to learn how an invite works: "Invite link – Anyone with this link can join" | Adding the task worked. **Note:** this is not what a contributor would do. Steps 7–11 were tested as the list owner, not as someone who joined. | 08-share-dialog.png, 09-task-assigned-to-me.png |
| 7 | Find what's mine | Assigned the task to myself ("Whose job is this?" → me), then opened "My tasks" | Worked. The task shows the list name, "Yours" and "Today". | 10-my-tasks.png |
| 8 | See what's due today | Opened "Today" | Worked. The sidebar shows a count badge. There is no comment button in this view, so I had to go into the list to comment. | 11-today.png |
| 9 | Ask a question on the task | In the list, clicked the comment icon and posted "(DEMO) Oat milk or regular?…" | Worked. It shows "You · just now" and a "1 comment" count. | 12-comment-posted.png |
| 10 | Tick it off so nobody has to chase me | Ticked the checkbox | Worked. Progress went to 100% and the checkbox now reads "Mark as not done". No "done by Kai" or time is shown on the task itself. | 13-task-done.png |
| 11 | Come back later on my phone | Resized the window to phone size and reopened /welcome | On the same browser: worked. I stayed signed in, and the phone layout has a bottom bar (Overview / Today / Mine / You). On a new phone: my only way in is to copy the token and paste it there. I didn't test this with a second device. | 14-phone-list.png, 15-phone-dashboard-returning.png |

#### Review
##### Fits my workflow
- Getting started means typing a name and nothing else: no account, email, password or app install. That removes my pain point "Having to create an account and remember a password for a tool someone else picked" [E0: industry assumption] and fits the critical assumption about joining with no account.
- "My tasks" and "Today" are right there in the side menu and in the phone's bottom bar. They answer "what is mine and what is due today" [E0: industry assumption], so I don't have to scroll back through chat [E1: flowhubr].
- A task shows "Yours" clearly. That fixes "unclear whether a task is theirs" [E1: flowhubr].
- Ticking a task off is one tap and the progress updates. That covers "Mark a task done so the organizer knows without a call or message" [E1: mein-handwerker-app.de].
- Commenting right on the task covers my weekly job "Add a note or question to a task" [E0: industry assumption].
- The welcome text says openly that my name is shown next to what I add and finish. I like that it's up front, but see "No basis" below.

##### Change requests
- On the empty dashboard, say how to join: "Got a link from someone? Open it – or paste it here" | because: the "Join a list from a link someone sent in chat" job; I landed on the base URL without a link and the only option was "Create your first list", which is a dead end for a contributor [E1: support.microsoft.com share-a-task-list; E1: learn.microsoft.com "can't join list"] | priority: high
- Add a "paste an invite link" field, and check the phone flow where the link opens in the chat app's built-in browser, not the normal one | because: joining fails often enough in other tools that people post about it, and a failed join means I go back to chat [E1: learn.microsoft.com to-do-app-cant-join-list; E0] | priority: high
- Use one word for the sign-in secret ("key" or "token", not both), hide the CLI line from non-technical people, and offer a simple way to move it to my phone (QR code, or "send to myself in WhatsApp") | because: "Get back into my lists on a new phone" job; technical skill varies a lot, including trades workers [E1: bitkom Handwerk study]; critical assumption about keeping the sign-in key | priority: high
- Make the yellow "Save your sign-in key" warning shorter or able to snooze. Right now it sits on top of every page | because: I spend seconds per visit and want zero learning time [E0: industry assumption] | priority: medium
- Show "done by Kai · 17:04" on a finished task | because: the point of ticking is that others see it without me messaging them; I could only check the owner's view [E1: mein-handwerker-app.de] | priority: medium
- Add comment and tick-off directly in "Today" and "My tasks" | because: I work in short bursts and don't want to open the list just to ask a question [E0: industry assumption] | priority: medium
- Offer a German interface | because: DACH users, trades workers and older club members [E1: bitkom Handwerk study]; critical assumption about the English UI (open) | priority: medium

##### Where I would leave the tool
- **Step 3/4, landing without an invite link.** The app only offers "Create your first list". As Kai I would write "where's the list?" in the chat. If nobody answers quickly, I'd keep doing my tasks through chat [E0: industry assumption, "drifts back to chat"].
- **New phone.** If I didn't copy the token on the first day, I can't get back in except with a new invite, and then I'd be a different person in the list. That's the kind of moment where I'd quietly stop using it [E0].

##### Core value touched
- The profile has no core value defined yet ("from phase 3"), so I can't flag anything. If "join with no account" becomes the core value, then the token-only way to recover access (step 11) is the weak point that could undo it.

##### No basis (ask real customers)
- Whether contributors would really follow a link and use the list instead of just replying "done" in chat. I have no basis for that; you should ask real customers.
- Whether it feels like being watched at work when my name shows up next to finished tasks and the list shows a "Progress %". I have no basis for that; you should ask real customers.
- Whether web push or reminders would bring me back without a nudge in chat. The app offered no notifications at all in this test. I have no basis for that; you should ask real customers.
- How it behaves offline or with a weak signal on a building site. I didn't test this.

#### Issues found (product defects)
| # | Step | What happened | Expected | Screenshot |
|---|---|---|---|---|
| 1 | 3 | A new user without a link sees only "Create your first list", with no hint on how to join someone else's list | An empty state that explains joining by link, or a place to paste the link | 03-empty-dashboard.png |
| 2 | 5 | The banner says "sign-in key" and the dialog says "sign-in token"/"token" for the same thing | One term used everywhere | 04-profile-token.png |
| 3 | 8 | "Today" has edit and delete buttons for a task, but no comment button (the list view has one) | The same task actions in every view, or at least comment | 11-today.png |
| 4 | 10 | A finished task shows no one's name and no time, even though the welcome page promises your name appears "next to the tasks you … finish" (only checked in the owner's own view) | "Done by [name]" shown on finished tasks | 13-task-done.png |
| 5 | 1 | Console message "Password field is not contained in a form" on the dashboard (the hidden token field) | Minor, no effect on users. Put the field inside a form | – |

**Limit of this run:** I got no invite link and could only use one browser session. So I never joined a list as a guest. Steps 6–10 were done as the owner of my own "(DEMO)" list, and signing in on a second device with the token was not tested.

Demo data left on the live site: the list "Week tasks (DEMO)" (/lists/5), with the task "Buy milk for the kitchen (DEMO)" and one "(DEMO)" comment. It belongs to "Kai (DEMO contributor)".

### Run 2

#### Steps taken
| # | What I wanted to do (my workflow) | What I did in the product | Result | Screenshot |
|---|---|---|---|---|
| 1 | Open Doables for the first time and get started | Opened the URL and was sent to /welcome. Entered "Kai (DEMO contributor)" and clicked "Get started". No email, password or install. | worked (about 5 seconds) | 01-welcome.png, 03-first-home.png |
| 2 | See whether "on another device" lets me in | Opened "Already use Doables on another device?". It only offers "Paste your token (from your Profile)". | confusing: it's for my own second device, not for joining a colleague's list | 02-other-device-token.png |
| 3 | Get to the shared list without an invite link | Checked the Overview empty state ("Create your first list… then invite others"), My tasks ("Open a shared list…"), Today, Profile, and the "+" next to Lists (only a name field). There's no "join a list" option and no field for a code or link anywhere. | failed: I'd leave here and write in chat "send me the link" | 03-first-home.png, 04-my-tasks-empty.png, 05-today-empty.png, 06-profile-token.png, 07-new-list-dialog.png |
| 3b | (Tester workaround, not what my role would do) Build a stand-in for the shared list | Created "Week tasks (DEMO)" with two DEMO tasks, one due today, and assigned one to myself via "Whose job is this?". Looked at Share: an invite link plus "Anyone with this link can join". | worked | 08-share-dialog.png, 09-list-assigned.png |
| 4 | Find the tasks that are mine | The list shows a "Yours" badge. The sidebar "My tasks" (called "Mine" on phone) lists only my task, with the list name. | worked | 10-my-tasks.png, 11-my-tasks-view.png |
| 5 | Look at what's due today | "Today" in the sidebar has a counter and shows my task with the list name, "Yours" and "Today". | worked | 12-today-view.png |
| 6 | Add a question to my task | Today has no comment button, so I had to open the list. There I clicked the comment icon, typed the question and posted it. It appears as "You · just now". | worked, but only from the list view | 13-comment-posted.png |
| 7 | Mark the task done | Ticked the checkbox in the list. Counts changed to 1 open / 1 done / 50 %. The task moved to the bottom, and Today now shows "Nothing due". | worked, but it doesn't show who finished it | 14-task-done.png, 15-done-filter.png |
| 8 | Find out how I get back in on my phone | Clicked "Show it" on the "Save your sign-in key" banner. It opens the Profile, where the token is still masked (an extra eye-click to see it). The only option is Copy: no QR code, no "open on phone" link. Checked the phone layout at 390px: it has a bottom bar (Overview / Today / Mine / You). | confusing: I'd have to copy a long secret from laptop to phone myself | 16-show-sign-in-key.png, 17-phone-list.png, 18-phone-today.png |

#### Review
##### Fits my workflow
- Getting started asks only for a name: no account, email, password or app. That's exactly what I'd put up with for a tool someone else picked. [E0: industry assumption – critical assumption "only join if it takes no account…"]
- "My tasks" and "Today" across all lists, plus the "Yours" badge, answer my daily question ("what's mine, what's due today") in one tap. That fixes "is this task meant for me?" [E1: flowhubr – tasks buried in chat, unclear whether a task is theirs]
- One click ticks a task off and the progress count updates right away, so the organizer doesn't need a "done" message from me. [E1: mein-handwerker-app – mark done without call or message]
- Commenting inline on the task keeps my question next to the task instead of lost in chat. [E0: industry assumption – weekly job "add a note or question"]
- On a phone, the bottom bar puts Today and Mine within thumb reach. [E0: industry assumption – seconds per visit]

##### Change requests
- Give people without a link a way to join. Add "Got an invite link or code? Paste it here" on the welcome page and in the empty state, and change the empty state from "Create your first list" to "Waiting for a list? Ask for the invite link". | because: in the trigger nobody sent me a proper invitation, only a chat message. A dead end here means I go back to chat. [E1: MS To Do join failures; E0: "if the tool feels like extra work, drifts back to chat"] | priority: high
- Make getting onto my phone one step: a QR code or a "send this login to my phone" link in the key banner, instead of copying a masked token. | because: getting back in on a new phone is a job of mine, and trades workers use the phone only. [E0: industry assumption; E1: bitkom – 76 % of trades businesses need more digital skills] | priority: high
- Show "Done by Kai · 17:05" on finished tasks. | because: the organizer has to see that I did my share without me messaging; that's my KPI of "being seen as doing a fair share". [E0: industry assumption; E1: liastoeffler – fairness] | priority: high
- Allow comments (and the done checkbox, which already works) directly in Today and My tasks. | because: I spend seconds per visit and shouldn't have to open the full list to ask a question. [E0: industry assumption] | priority: medium
- Use one word everywhere: "sign-in key", "sign-in token", "token (from your Profile)" and the CLI line all appear. Hide the CLI hint from non-technical users. | because: users range from agency staff to trades workers and older club members, and an English UI plus jargon hurts first-use success. [E1: bitkom Handwerk; E0: critical assumption on English UI] | priority: medium
- Soften the permanent red-ish "Save your sign-in key… these lists are gone" banner, or show it once. | because: it's on every page, it's scary, and it feels like more homework for a tool I didn't choose. [E0: pain "yet another app"] | priority: low

##### Where I would leave the tool
- Step 3: without a link, the app only tells me to create my own list. I'd close it and write in chat "where's the link?" or just reply "done" in chat, and the list would go stale.
- Step 8: if switching to the phone means copying a hidden token, I probably wouldn't bother. I'd use it on whichever device I first opened, or drop it.

##### Core value touched
- The profile's "Core value – do not touch" section is still empty (it comes from phase 3), so I can't check against it. The closest critical assumptions are "join without account" (supported) and "contributors mark done in the list" (works, but it's not credited to me by name).

##### No basis (ask real customers)
- Whether "done by name" would feel like being monitored at work rather than recognition. I have no basis for that – you should ask real customers. [critical assumption on visible names, and the business-owner relationship]
- Whether I'd come back without a push notification. The app offered no notification during this test. I have no basis for that – you should ask real customers.
- How it behaves offline on a building site. Not tested, and I have no basis for that – you should ask real customers.

#### Issues found (product defects)
| # | Step | What happened | Expected | Screenshot |
|---|---|---|---|---|
| 1 | 3 | No UI path to join someone else's list without the full /join/ URL: no paste field, no code entry, and the empty states only point to creating a list. | A visible way to join or paste a link, or at least a hint to ask for the invite link. | 03-first-home.png, 04-my-tasks-empty.png, 07-new-list-dialog.png |
| 2 | 7 | The welcome and profile pages promise "People you share lists with will see this name next to the tasks you add and finish", but a finished task shows no finisher name or time (only the assignee avatar "K"). | A "done by / added by" label on the task. | 14-task-done.png, 15-done-filter.png |
| 3 | 8 | "Show it" on the sign-in key banner opens the Profile with the token still masked (password field), so it doesn't show it. | Clicking "Show it" reveals the key, or a QR code. | 16-show-sign-in-key.png |
| 4 | 8 | The same thing has three names: "sign-in key" (banner), "sign-in token" (profile), "token (from your Profile)" (welcome). The same view is "My tasks" on desktop and "Mine" on phone. | Consistent terms. | 02-other-device-token.png, 06-profile-token.png, 18-phone-today.png |
| 5 | 6 | Today and My tasks rows have Edit and Delete but no Comment button, while list rows do. | The same row actions in every view. | 12-today-view.png |

Note: this test left a live list, "Week tasks (DEMO)" (/lists/8), with two DEMO tasks and one DEMO comment, owned by "Kai (DEMO contributor)". The Share dialog created an invite link for it, but it wasn't copied or sent anywhere. Steps 3b to 7 used this self-made list, so the contributor mechanics were tested as the list owner, not as an invited member.
