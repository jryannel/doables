# Doables – defect list from avatar walkthroughs (2026-09-26)

Source: three walkthroughs of https://doables.gelbkappe.de, two runs each (team lead and household organizer: FLOW-001; task contributor: FLOW-002). Defects are product observations anyone would see; the avatars' opinions and change requests are in `hypotheses/`, not here.

"Seen in" lists the walkthroughs (TL = team lead, HO = household organizer, TC = task contributor); "stable" means it showed up in both runs of that walkthrough. Screenshot paths are relative to `results/walkthroughs/`.

Priority is a suggestion: **P1** breaks a promise or a core step, **P2** confuses users, **P3** polish.

---

## P1

### 1. Finished tasks don't show who finished them, although the welcome page promises it
- **Where:** list view, Done filter; welcome page text
- **Steps:** Get started with a name → create a list → add a task → mark it done → open the Done filter.
- **Actual:** the completed task shows no name and no time.
- **Expected:** the welcome page says "People you share lists with will see this name next to the tasks you add and finish" – the finisher's name (ideally with time) is shown on done tasks.
- **Seen in:** TL (stable), HO (unstable – maybe only with a single member), TC (stable)
- **Screenshots:** `2026-09-26-team-lead-flow-001-plan-week/run-1/12-done-filter.png`, `2026-09-26-task-contributor-join-shared-list/run-2/15-done-filter.png`

### 2. Assign menu offers only "you" and "Anyone", with no hint how to add others
- **Where:** task row → "Assign this task" ("Whose job is this?")
- **Steps:** create a new list alone → add a task → open the assign menu.
- **Actual:** only your own name and "Anyone"; nothing explains that others appear after they join, and there's no link to Share.
- **Expected:** at least an empty-state hint ("Invite people to assign tasks to them") with a link to the Share dialog.
- **Seen in:** TL (stable), HO (stable), TC
- **Screenshots:** `2026-09-26-household-organizer-plan-the-week/run-1/07-assign-menu.png`, `2026-09-26-team-lead-flow-001-plan-week/run-2/07-assign-only-me.png`

### 3. No way to join someone else's list from inside the app
- **Where:** first start / empty dashboard / "New list"
- **Steps:** get started as a new user without having opened an invite link.
- **Actual:** the only option is "Create your first list"; there is no "Join a list" or "Paste an invite link" field. Joining works only by opening the full `/join/…` URL.
- **Expected:** a way to paste an invite link or code, or at least an empty-state hint "Got an invite? Open the link you received."
- **Seen in:** TC (stable)
- **Screenshots:** `2026-09-26-task-contributor-join-shared-list/run-1/07-new-list-no-join-option.png`, `…/run-1/03-empty-dashboard.png`

## P2

### 4. Profile dialog shows a developer command-line line to every user
- **Where:** profile dialog (sign-in key / token section)
- **Actual:** shows text like `DOABLES_TOKEN=… doables lists`.
- **Expected:** hide CLI instructions from regular users (e.g. behind "For developers").
- **Seen in:** HO (stable), TL, TC
- **Screenshots:** `2026-09-26-household-organizer-plan-the-week/run-1/14-sign-in-key.png`, `2026-09-26-task-contributor-join-shared-list/run-1/04-profile-token.png`

### 5. The same thing is called "sign-in key", "sign-in token", and "token"
- **Where:** banner ("Save your sign-in key"), profile dialog ("sign-in token"), other screens ("token")
- **Expected:** one term everywhere.
- **Seen in:** TL (stable), HO (stable), TC (stable)
- **Screenshots:** `2026-09-26-team-lead-flow-001-plan-week/run-1/03-signin-key-modal.png`

### 6. "Show it" on the banner opens the dialog with the token still masked
- **Steps:** click "Show it" in the "Save your sign-in key" banner.
- **Actual:** the dialog opens but the token is hidden; a second click is needed.
- **Expected:** "Show it" shows it.
- **Seen in:** TL (unstable), TC (unstable)
- **Screenshots:** `2026-09-26-task-contributor-join-shared-list/run-2/16-show-sign-in-key.png`

### 7. Today and My tasks have no comment button
- **Where:** Today view, My tasks view
- **Actual:** comments are only possible in the list view.
- **Expected:** the same task actions (comment) in all task views.
- **Seen in:** TC (stable)
- **Screenshots:** `2026-09-26-task-contributor-join-shared-list/run-2/12-today-view.png`

### 8. Ticking a task in Today removes it instantly, with no undo
- **Steps:** Today → mark a task as done.
- **Actual:** the task disappears immediately; an accidental tick can't be undone from there.
- **Expected:** a short "Undo" toast, or the task stays visible as done until the view is left.
- **Seen in:** TL (unstable)
- **Screenshots:** `2026-09-26-team-lead-flow-001-plan-week/run-2/10-today-after-done.png`

### 9. Mobile empty state points to a "+" that is hidden behind the menu
- **Where:** empty dashboard on a phone-sized screen
- **Actual:** the text says to press "+" next to "Lists", but on mobile that's inside the closed hamburger menu.
- **Expected:** a visible "New list" button in the mobile empty state.
- **Seen in:** HO (unstable)
- **Screenshots:** `2026-09-26-household-organizer-plan-the-week/run-2/03-home-mobile.png`, `…/run-2/04-menu-open.png`

## P3

### 10. Progress percentage is truncated instead of rounded
- **Steps:** a list with 6 tasks, 1 done.
- **Actual:** "16%". **Expected:** "17%".
- **Seen in:** TL (stable), HO (stable)
- **Screenshots:** `2026-09-26-team-lead-flow-001-plan-week/run-1/13-list-done-filter.png`

### 11. Submitting a task with an empty title gives no feedback
- **Steps:** press "Add task" with an empty title.
- **Actual:** nothing happens. **Expected:** a short validation message.
- **Seen in:** HO (unstable)
- **Screenshots:** `2026-09-26-household-organizer-plan-the-week/run-1/05-empty-title-submit.png`

### 12. The same view is called "My tasks" on desktop and "Mine" on mobile
- **Expected:** one name.
- **Seen in:** TC (unstable)
- **Screenshots:** `2026-09-26-task-contributor-join-shared-list/run-2/18-phone-today.png`

### 13. Browser console warning on every page: "Password field is not contained in a form"
- **Where:** all pages (the hidden sign-in key/token field)
- **Expected:** no console warnings; wrap the field in a form or use a non-password input with masking.
- **Seen in:** TL (stable), TC (unstable)

---

## Not tested
- Joining a list through an invite link from a second person, and signing in on a second device – each run had only one browser identity.

## Test data left on the live site
DEMO lists created by the walkthroughs (names ending in "(DEMO)"), including "Week 40 team plan (DEMO)" with an active invite link, "WG Woche 39 (DEMO)" (/lists/3 and /lists/6), "Week tasks (DEMO)" (/lists/5 and /lists/8), plus "Team week 40 (DEMO)" and the test users "Claude (test)" and "Mara (demo organizer)" from the setup.
