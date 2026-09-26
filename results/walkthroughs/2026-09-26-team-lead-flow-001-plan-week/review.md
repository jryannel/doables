> ⚠ Avatar output, not customer evidence – team-lead: 0 % E2+, critical assumptions tested 0 of 10. Mostly assumptions – treat as a guess.

# Walkthrough: team-lead – FLOW-001 Plan the coming week together

Date: 2026-09-26 | Environment: https://doables.gelbkappe.de/ (live site) | Profile version: 1 | Account: display name "Tina (DEMO team lead)" (no password; new user per session)
Runs: 2 | Demo data used: none (flow needs no uploads) | Previous walkthrough: none

Change requests become hypotheses at most. "Stable" = found in all runs.

## Review
### Fits my workflow
- Starting takes under 10 seconds with no email or password. That fits the "minutes, not hours" setup budget and avoids the account barriers of other tools [E0: industry assumption] [E1: https://support.microsoft.com/en-us/todo/create-and-share-lists] | stable
- Sharing by invite link with a Copy button fits handing out work in the team chat [E1: https://www.bitkom.org/Presse/Presseinformation/Handwerk-wird-digitaler] | stable
- "Today" (Overdue / Today / Next 7 days, across all lists) covers the daily "what is due today" check [E0: industry assumption] | stable
- Task entry is fast and flat (title, optional note, optional date, Enter submits, sorted by due date), with no projects or subtasks, which avoids the Asana learning-curve problem [E1: https://www.g2.com/products/asana/reviews?qs=pros-and-cons] | stable
- No member limit or paywall was seen [E1: https://support.atlassian.com/trello/docs/workspace-user-limit/] | unstable

### Change requests
- Let me assign tasks to people who haven't joined yet (a name placeholder they claim when they join), or at least put "share/invite to assign people" inside the "Whose job is this?" menu | because: I plan the week first and share it second. Right now I have to share, wait for everyone to join, and come back to assign [E1: https://www.jobverde.de/karriereinfo/teamleitung-der-job-als-teamleiterin] [E1: https://techcommunity.microsoft.com/discussions/to-do/to-do-task-assignment-feature-is-inconvenient--unable-to-set-reminders-for-tasks/4028520] | priority: high | stable
- Show "done by X, at time" on completed tasks | because: I have to stop chasing status in chat and I report weekly to the owner [E0: industry assumption] | priority: high | stable
- Group or filter Today and the list by person ("who is behind"). Run 2 also wants the assignee's name on every row | because: the daily "who is behind" job, and "responsibility is implied rather than assigned" [E0: industry assumption] [E1: https://flowhubr.com/blog/project-management/why-using-whatsapp-to-manage-internal-tasks-fails-for-smes/] | priority: medium–high | stable
- Show open tasks without a date in Today (e.g. a "No date" group) | because: undated tasks vanish from the daily check, and about 20 % of the plan is flexible work [E0: industry assumption] [E1: https://www.teamleader.eu/de/blog/ressourcenplanung-vorlage] | priority: low–medium | stable
- Make the sign-in key banner less alarming, use one term (key vs. token), and hide the CLI hint | because: teams have mixed digital skills, and contributors can veto the tool by not using it [E1: https://www.bitkom.org/sites/main/files/2026-01/bitkom-studienbericht-handwerk.pdf] [E0: industry assumption] | priority: medium | stable
- Paste several lines at once, one task per line | because: I dump the week's collected work in one go on Monday [E0: industry assumption] | priority: medium | unstable
- Undo after ticking a task in Today | because: I tick things quickly between other work [E0: industry assumption] | priority: low | unstable

### Where I would leave the tool
- Step 5, assigning: if I can't give tasks to named colleagues during Monday planning, I'd post the list in WhatsApp with @names as before [E0: industry assumption] | stable
- Mid-week: if Today can't show who is behind, I'd go back to asking "Is X done?" in chat [E0: industry assumption] | unstable
- Later, if team members lose access (new phone, cleared browser) and I have to sort it out (not tested) [E0: industry assumption] | unstable

### Core value touched
- None. The profile has no "Core value" section yet (phase 3). Both runs said the no-account start and the invite link are what the critical assumptions depend on, and they must not get worse.

### No basis (ask real customers)
- Whether team members actually open the link on their phones and join (both runs)
- Whether "Anyone" as an assignee is useful or confusing (both runs)
- How recovery on another device feels in practice (run 2), and whether the owner accepts per-person tokens (run 1)

## Issues found (product defects, for the team)
| # | Step | What happened | Expected | Screenshot | Stable |
|---|---|---|---|---|---|
| 1 | Onboarding | The banner says "sign-in key", but the dialog it opens says "sign-in token" | One consistent term | run-1/03-signin-key-modal.png, run-2/03-signin-key-modal.png | stable |
| 2 | Progress | 1 of 6 done shows "16%" (16.67 is cut off, not rounded) | 17% | run-1/14-overview.png, run-2/12-overview.png | stable |
| 3 | Done task | The welcome text promises your name "next to the tasks you add and finish", but done tasks show no completer and no time | Completer name (and time) on done tasks | run-1/13-list-done-filter.png, run-2/11-list-done-filter.png | stable |
| 4 | Assign | The assign menu offers only "you" and "Anyone", with no hint that others appear only after joining by link | Empty-state hint or invite shortcut in the menu | run-1/07-assign-menu.png, run-2/07-assign-only-me.png | stable |
| 5 | All pages | Console notice "Password field is not contained in a form" (probably the hidden token field). Harmless | No console notice | – | stable |
| 6 | Onboarding | "Show it" opens the dialog with the token still masked, so a second click is needed | Show the key directly | run-2/03-signin-key-modal.png | unstable |
| 7 | Today | Ticking a task removes it instantly, with no undo | Short undo toast | run-2/10-today-after-done.png | unstable |

Side notes: run-1/12-done-filter.png is misnamed (it shows the Today view). Live-site artifacts left behind: list "Week 40 team plan (DEMO)" (/lists/4) with an active invite link, and list "Team week KW 39 (DEMO)", each with 6 DEMO tasks. In run 2, the task "Fix contact form bug (DEMO)" has no description because of a tester tooling limit, not a product issue.

## Compared with the previous walkthrough
- **Resolved:** – (no previous walkthrough)
- **Still open:** –
- **New:** everything above

## Run details
### Run 1
#### Steps taken
| # | What I wanted to do (my workflow) | What I did in the product | Result | Screenshot |
|---|---|---|---|---|
| 1 | Get started fast on Monday morning, with no account setup | Entered "Tina (DEMO team lead)" and clicked "Get started" | Worked. Under 10 seconds, no email and no password | 01-welcome.png, 02-dashboard-empty.png |
| 2 | Understand the "save your sign-in key" warning | Clicked "Show it" in the yellow banner, which opened the profile dialog | Confusing. The banner says "sign-in key", the dialog says "sign-in token", and the dialog shows a CLI line (`DOABLES_TOKEN=<token> doables lists`). The banner stays on every page until "I've saved it" is clicked | 03-signin-key-modal.png |
| 3 | Create a list for this week | "+" next to "Lists", typed "Week 40 team plan (DEMO)", pressed Enter | Worked. The empty dashboard showed where to click | 04-list-created-empty.png |
| 4 | Enter 5–8 tasks, some with a due date and a short description | Used the title, description and date fields, then Enter or "Add task", six times | Worked. Enter submits and the form clears. Tasks sort by due date with "Yesterday", "Today" and "Sep 29" labels. Still one task at a time, with no pasting a whole list | 05-due-date-picker.png, 06-six-tasks-added.png |
| 5 | Give each task to one person | Clicked "Assign this task" | Partly failed. "Whose job is this?" offers only me or "Anyone", with no hint that the list has to be shared first. I assigned the offer task to myself | 07-assign-menu.png |
| 6 | Share the list into the team chat | "Share" opened an invite link with a Copy button, "Anyone with this link can join…", and a people list | Worked and fits the chat workflow. Joining as a colleague was not tested (one browser identity) | 08-share-dialog.png, 09-share-link-copied.png |
| 7 | Check what is due today and what is open | Opened "Today" | Worked well: Overdue, Today and Next 7 days across lists. Undated tasks are missing, and there's no filter by person | 10-today-view.png |
| 8 | Tick off one task | Ticked "Send revised offer…" in Today | Worked. It disappeared from Today and the counters updated | 11-task-marked-done.png, 12-done-filter.png (misnamed) |
| 9 | Check that the done task is recorded | Done filter in the list, then Overview | Worked, but there's no "who finished it or when". Overview: "5 open · 1 done 16%" | 13-list-done-filter.png, 14-overview.png |
| 10 | Edge case: another device | Only saw "Already use Doables on another device?" on the welcome page | Not tested. The only way back is the token | 01-welcome.png |

#### Review
**Fits my workflow**
- Starting takes seconds with no email or password. That removes the account problem that keeps freelancers out of other tools [E1: https://support.microsoft.com/en-us/todo/create-and-share-lists] and fits my limited patience for setup [E0: industry assumption].
- Sharing works by link, which I can paste into the team chat [E1: https://www.bitkom.org/Presse/Presseinformation/Handwerk-wird-digitaler].
- "Today" with Overdue / Today / Next 7 days is my daily check [E0: industry assumption], and so is "5 open · 1 done" on Overview.
- Simple entry with no projects or subtasks avoids the Asana learning-curve problem [E1: https://www.g2.com/products/asana/reviews?qs=pros-and-cons].
- No member limit or paywall seen.

**Change requests**
- Assign to people who haven't joined yet, or at least hint "share the list first" in the menu | because: weekly planning, and the same wait-for-join problem as in To Do [E1: jobverde] [E1: techcommunity] | priority: high
- "Done by X, on date/time" | because: stop chasing status, weekly owner report [E0] | priority: high
- Filter or group by person in Today and in the list | because: "who is behind" and rebalancing [E0] | priority: medium
- Paste several lines at once | because: Monday dump of collected work [E0] | priority: medium
- Undated tasks in Today | because: they're invisible in the daily check otherwise [E0] | priority: low
- One word for key/token, drop the CLI line, and a less alarming banner | because: mixed digital skills in trades [E1: bitkom study] | priority: medium

**Where I would leave the tool**
- Step 5: without assigning named people on Monday, I'd post the list in WhatsApp as before and only come back once the team has joined.
- Possibly later, when team members lose access and I have to fix it (not tested).

**Core value touched:** the profile section is empty (phase 3). The no-account start and the invite link are the strongest points and should not get worse.

**No basis:** whether the team joins from their phones; whether "Anyone" is useful; whether the owner accepts per-person tokens.

#### Issues found
1. "sign-in key" vs. "sign-in token" (03-signin-key-modal.png)
2. "16%" for 1 of 6, cut off instead of rounded (13, 14)
3. No completer or time on done tasks, despite the welcome text's promise (13)
4. The assign menu has no hint that others appear after joining (07)
5. Console notice "Password field is not contained in a form" on every page (harmless)

Notes: no errors or failed saves; the flow took about 2 minutes. Created: "Week 40 team plan (DEMO)" (/lists/4) with six tasks and an active invite link.

### Run 2
#### Steps taken
| # | What I wanted to do (my workflow) | What I did in the product | Result | Screenshot |
|---|---|---|---|---|
| 1 | Start fast on Monday morning | Typed "Tina (DEMO team lead)" and clicked "Get started" | Worked. Under 10 seconds, no email and no password | 01-welcome.png |
| 2 | Get oriented | Empty dashboard with a yellow banner "Save your sign-in key… these lists are gone". "Show it" opened a profile dialog with a masked "sign-in token" and a CLI line | Confusing. Key vs. token, a scary warning before doing anything, and a CLI hint that means nothing to my team | 02-dashboard-empty.png, 03-signin-key-modal.png |
| 3 | Create this week's list | "+" next to "Lists", typed "Team week KW 39 (DEMO)", pressed Enter | Worked. The list opened right away | 04-list-created-empty.png |
| 4 | Write the week's list with dates and notes | Added 6 tasks with the always-visible form. Enter submits | Worked, fast and sorted by due date | 05-task-form-filled.png, 06-six-tasks-added.png |
| 5 | Give each task to one person | "Assign this task" offered only "Tina (you)" and "Anyone" | Failed for the team case. No colleagues until they join, and no hint or invite in the menu. 5 of 6 tasks stayed unassigned | 07-assign-only-me.png |
| 6 | Post the list into the team chat | "Share" showed an invite link with Copy, "Anyone with this link can join, add tasks and tick them off", People (1): me, Owner | Worked, exactly what I'd paste into WhatsApp. The invitee side was not tested | 08-share-dialog.png |
| 7 | Check what's due today and what's behind | "Today": Overdue (1), Today (1), Next 7 days (3), across lists | Mostly worked. No "who" column or filter, and the undated task is missing | 09-today-view.png |
| 8 | Mark one task done | Ticked "Send offer…" in Today | Worked. It disappeared and the counters updated. No undo seen | 10-today-after-done.png |
| 9 | See what got finished | List "Done" filter, Overview "5 open · 1 done 16%" | Worked, but there's no "done by / when", and 16% for 1 of 6 | 11-list-done-filter.png, 12-overview.png |
| 10 | Come back on another device | Only saw "Already use Doables on another device?" | Not tested | 01-welcome.png |

#### Review
**Fits my workflow**
- In and on the first list in well under two minutes [E0: industry assumption]. Avoids the account problems of other tools [E1: support.microsoft.com To Do sharing].
- The invite link is easy to paste into chat [E0] and 91 % of trades use messengers [E1: bitkom].
- Quick flat task entry fits Monday list writing [E0].
- The Today view is close to the daily "what is due today" job [E0].

**Change requests**
- Assign someone who hasn't joined yet (a placeholder claimed on join), or "Invite people to assign them" in the assign menu | because: plan first, share second, and the To Do wait-for-join problem [E1: techcommunity] | priority: high
- Assignee name or avatar on each row in the list and in Today, plus a "by person" filter or grouping | because: "who is behind", responsibility implied rather than assigned [E1: flowhubr] | priority: high
- "Done by X, time" on completed tasks, as the welcome text promises | because: chasing status, weekly owner report [E0] | priority: high
- Undated open tasks in Today ("No date"), or an "open" count | because: "what is still open", 20 % flexible work [E1: teamleader.eu] | priority: medium
- A less alarming key banner, one term, and no CLI hint | because: 76 % of trades need more digital skills [E1: bitkom study], and contributors can veto the tool [E0] | priority: medium
- Undo after ticking in Today | because: I tick quickly between other work [E0] | priority: low

**Where I would leave the tool**
- Step 5: if I can't give "Finalize mockups" to Jonas on Monday before he opens the link, I'd go back to posting the list in chat with @names.
- Mid-week: if Today can't show who is behind, I'd be back to asking "Is X done?" in chat.

**Core value touched:** not defined yet. "Joining takes seconds with no account" works. "One named person per task" is blocked until people join.

**No basis:** whether members open the link on their phones and join; whether "Anyone" is useful; how recovery on another device feels.

#### Issues found
1. The banner says "sign-in key", the dialog says "sign-in token" (02, 03)
2. "Show it" opens the dialog with the token still masked, so a second click is needed (03)
3. The welcome text promises names next to added/finished tasks, but none are shown (only "Yours" on the self-assigned one) (11)
4. "16%" for 1 of 6, cut off instead of rounded (11, 12)
5. Ticking in Today removes the task instantly, with no undo (10)

Only one harmless console message ("Password field is not contained in a form"); no errors. The "Fix contact form bug (DEMO)" task has no description because of a tester tooling limit (semicolon), not the product.
