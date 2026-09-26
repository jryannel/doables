# Persona: Task contributor

Version: 1 | As of: 2026-09-26 | Last decision: – 
Maturity: 0 % E2+ | Critical assumptions tested: 0 of 10
Buying function: User | Segment: All segments – invited team members, freelancers, club volunteers, household members; groups of 2–20, DACH first

## Context
- Measured by (KPIs): at work, getting assigned tasks done on time [E0: industry assumption]; at home or in a club, not being nagged and being seen as doing a fair share [E0: industry assumption]
- Current tools: the group chat is the default channel; WhatsApp is used by 81 % of internet users in Germany [E1: https://www.bitkom.org/Presse/Presseinformation/Eine-Milliarde-Kurznachrichten-pro-Tag]; in trades, 91 % of businesses use messengers internally [E1: https://www.bitkom.org/Presse/Presseinformation/Handwerk-wird-digitaler]; otherwise whatever tool the organizer or team lead picked [E0: industry assumption]
- Decision power: no formal say over the tool, but an effective veto by not using it [E0: industry assumption]
- Time budget and technical affinity: wants zero learning time and spends seconds, not minutes, per visit [E0: industry assumption]; technical affinity varies widely, from agency staff to trades workers where 76 % of businesses see a need for more digital competence [E1: https://www.bitkom.org/sites/main/files/2026-01/bitkom-studienbericht-handwerk.pdf]
- Typical workday: gets tasks through chat messages, calls, or a quick word from the organizer; does them in between other work; reports back by chat or not at all [E0: industry assumption]

## Jobs to be done
- Find out what is mine and what is due today | Frequency: daily [E0: industry assumption]
- Mark a task done so the organizer knows without a call or message | Frequency: daily [E1: https://mein-handwerker-app.de/aufgabenverwaltung/]
- Add something I noticed (we're out of milk, material missing, a new to-do) | Frequency: weekly [E0: industry assumption]
- Add a note or question to a task | Frequency: weekly [E0: industry assumption]
- Join a list from a link someone sent in chat | Frequency: rare (once per list) [E1: https://support.microsoft.com/en-us/todo/share-a-task-list]
- Get back into my lists on a new phone or computer | Frequency: rare [E0: industry assumption]

## Typical industry flows
Receiving and doing a task today [E0: industry assumption]:
1. Gets a message in the team, family, or club chat, among many unrelated messages. [E1: https://flowhubr.com/blog/project-management/why-using-whatsapp-to-manage-internal-tasks-fails-for-smes/]
2. Has to work out whether the task is meant for them, because responsibility is implied rather than assigned. [E1: https://flowhubr.com/blog/project-management/why-using-whatsapp-to-manage-internal-tasks-fails-for-smes/]
3. Remembers it or not; later scrolls back to find the details. [E0: industry assumption]
4. Does the task and replies "done" in chat, or says nothing. [E0: industry assumption]
5. Gets reminded by the organizer if nothing was reported. [E1: https://liastoeffler.de/blog/3-gr%C3%BCnde-warum-putzen-in-der-wg-nicht-funktioniert]

Joining a shared tool someone else chose [E0: industry assumption]:
1. Receives an invitation link or email. [E1: https://support.microsoft.com/en-us/todo/share-a-task-list]
2. Has to install an app and/or create or sign in with a matching account; in Microsoft To Do the invitee must use an Exchange Online-backed account. [E1: https://learn.microsoft.com/en-us/answers/questions/5525689/microsoft-to-do-list-cannot-be-shared-to-other-mic]
3. Joining fails often enough that people post about it ("can't join list", "List isn't available"). [E1: https://learn.microsoft.com/en-us/answers/questions/5688092/to-do-app-cant-join-list]
4. After joining, gets notifications for assigned tasks, e.g. Apple Reminders notifies the assignee. [E1: https://support.apple.com/en-us/105124]
5. If the tool feels like extra work, drifts back to chat. [E0: industry assumption]

Trades worker on site [E0: industry assumption]:
1. Receives the day's jobs by WhatsApp or a call from the office or team lead. [E1: https://mein-handwerker-app.de/einsatzplanung-handwerk-tipps/]
2. Works on site with the phone in the pocket, often with dirty hands or gloves. [E0: industry assumption]
3. Reports completion or problems by call or voice message. [E0: industry assumption]

## Pain points (sorted by severity)
- Tasks buried in chat threads; unclear whether a task is theirs [E1: https://flowhubr.com/blog/project-management/why-using-whatsapp-to-manage-internal-tasks-fails-for-smes/]
- Being nagged or checked on, which feels like being policed [E1: https://liastoeffler.de/blog/3-gr%C3%BCnde-warum-putzen-in-der-wg-nicht-funktioniert]
- Having to create an account and remember a password for a tool someone else picked [E0: industry assumption]
- Invitations that fail or open under the wrong account [E1: https://learn.microsoft.com/en-us/answers/questions/5975091/unable-to-access-a-microsoft-to-do-list-invitation]
- Yet another app with its own notifications on top of chat [E0: industry assumption]
- Feeling that the split of work is unfair when effort and presence differ [E1: https://liastoeffler.de/blog/3-gr%C3%BCnde-warum-putzen-in-der-wg-nicht-funktioniert]

## Core value – do not touch
(from phase 3)

## Current workflow with our tool
(from phase 3)
| Workflow step | In tool | Instead | Evidence |
|---|---|---|---|

## Relationships to other roles
- Team lead: receives work from the lead; completion status is what the lead needs back [E0: industry assumption]
- Household organizer: peer relationship; accepts tasks voluntarily and may push back on unfair splits [E0: industry assumption]
- Field worker (candidate): may be a segment variant of the contributor in trades rather than a separate role [E0: industry assumption]
- Business owner (candidate): at work, may see the contributor's completed tasks, which can feel like monitoring [E0: industry assumption]

## Contradictions (open)
(none yet)

## Critical assumptions
The statements most product decisions depend on. Status changes only through a decision.
- Contributors will only join if it takes no account, email, password, or app install; each extra step loses a noticeable share of invitees [E0: industry assumption] | Critical because: the identity model, invite-by-link flow, and the success criterion "invited people complete tasks without asking how the app works" | Status: open
- Contributors open the list mainly to see "what's mine and what's due today" and rarely browse the rest [E0: industry assumption] | Critical because: default view, "my tasks" filter, and navigation design | Status: open
- Contributors mark tasks done in the list instead of replying in chat; otherwise the list goes stale [E0: industry assumption] | Critical because: weekly active lists, the lead's/organizer's status view, and check-off UX | Status: open
- Without a push notification or a chat nudge, contributors don't come back to the list [E0: industry assumption] | Critical because: notification channels in a product without email (web push, chat sharing, reminders) | Status: open
- Contributors are fine with their name being shown next to what they added and finished [E0: industry assumption] | Critical because: the visible-name identity model and any activity/statistics features that could feel like surveillance at work | Status: open
- Contributors keep their sign-in key or stay signed in; losing access when switching devices is rare or easy to fix [E0: industry assumption] | Critical because: the sign-in key design and whether recovery or re-invite flows are needed | Status: open
- Contributors add tasks themselves, not only complete assigned ones [E0: industry assumption] | Critical because: permissions (who can add, assign, delete) and quick-add on mobile | Status: open
- Contributors belong to several lists from different contexts (work, home, club) and use one identity for all of them [E0: industry assumption] | Critical because: list switching, cross-list "my tasks" view, and separation of work and private life | Status: open
- An English UI is understood without help by DACH contributors, including trades workers and older club members [E0: industry assumption] | Critical because: localization priority and first-use success | Status: open
- Trades workers use the list only on the phone and need it to work with weak connectivity on site [E0: industry assumption] | Critical because: offline support and whether field worker needs its own profile | Status: open

## Refuted
(none)
