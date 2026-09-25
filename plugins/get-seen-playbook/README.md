# The Get Seen Playbook (Cowork plugin)

This plugin runs the parent-side work of college recruiting. It sets up a family's project,
keeps their pipeline tracker current, and drafts coach outreach in the Playbook voice. It
complements recruiters. It does not replace them.

## What it does

| Skill | What the family says | What happens |
| --- | --- | --- |
| Set up my recruiting workspace | "Set up my recruiting workspace" | Collects the athlete details, builds the Pipeline folder, places the tracker, saves the project instructions as CLAUDE.md |
| Update my pipeline | "Here is a coach reply" / "I sent this" | Updates the tracker, notes any dated next step, flags what is overdue and what has gone quiet |
| Draft outreach | "Draft an email to [school]" | Writes the coach email and saves it as a Gmail draft to review and send |

## First-time setup for a family (about 15 minutes)

1. Install the Claude desktop app and sign into a Claude plan.
2. Accept this plugin when it appears in the chat.
3. Point Cowork at a folder for the athlete and put the four Playbook files in it (the Guide,
   Email Template Library, Prompt Library and Pipeline Tracker).
4. Type "set up my recruiting workspace" and answer the questions.
5. Connect Gmail before the first draft. The email skill stops and asks for it if it is not
   connected.

After that, the two skills the family uses most are "Update my pipeline" and "Draft
outreach." The tracker stays current on its own instead of getting forgotten.

## Privacy

The athlete's information and the family's inbox stay on the family's own machine and
account. The family connects their own email. Nothing is shared back to anyone.

## Notes for this version (0.6.13)

- **The Targeting Brief wins over a template.** When an email template and the Brief disagree (for example, the template leads with height and the Brief says not to raise it), Claude follows the Brief and says in one line what it changed from the template and why. The same rule is in the starter block setup writes into CLAUDE.md.
- **Claude asks before drafting after a change.** If the family asks for a change, even while approving, Claude makes it and asks whether they want to see the whole email again before it creates the Gmail draft.
- **Clearer writing rules in the starter block.** The voice section now opens with the goal: clear, natural, grounded writing that sounds like a real athlete and family, not a sales pitch and not a polished AI draft. New rules: mix short and fuller sentences, say each thing once, let a stat make the point instead of an adjective, watch for writing that is too polished, and keep a school hook specific and true instead of generic praise. "It isn't X, it's Y" joins the banned phrases.

## Notes for 0.6.12

From the 9/24 retest:

- **Draft outreach shows the whole email first.** The family sees the complete email, word for word, and the Gmail draft is created only after they approve that exact email. The short bullet preview is gone. Section headings (the stats label, Film:, Team:, Jersey:, Position: and the Day schedule line) stay bold in the draft.
- **Stats come from the stats file.** Draft outreach reads current stats from the file the Athlete Dossier names and confirms they are current before using them.
- **Social media, not Instagram.** Signatures carry each social media handle with its platform. E03 is now Social Media Follow.
- **Setup asks women's or men's volleyball** and writes it into the first line of CLAUDE.md. The high school is asked before its position, with "does not play high school volleyball" as a choice. Time zone offers the four US zones, and the family can type another or say they are not sure.
- **The starter block matches P0-01 word for word**, including the new rule that Lock Your Voice (P2-05) is offered only after at least two batches of emails, never right after P1-01 or P2-01.

## Notes for this version (0.6.11)

- Wording: "chat" instead of "conversation" wherever it means a chat with Claude, matching the Playbook files (Alva's call, 9/23). "Conversation" stays where it means talking with a coach.

## Notes for this version (0.6.10)

- The one-line profile confirmation added in 0.6.9 is removed from draft-outreach and update-pipeline (Alva's call, 9/23). Both skills still read CLAUDE.md first and stop if they cannot find it. The Prompt Library made the same change.

## Notes for this version (0.6.9)

From the 9/22 account test and the Stage 2 plugin check:

- **Updates on Cowork save to CLAUDE.md.** The starter block's update rule now says to update CLAUDE.md in the folder, ask first, save the whole file and check it. The family is never asked to paste their instructions. It matches P0-01, which gives the paste wording back on the Project-Based path.
- **Proof it read the profile.** draft-outreach confirms the athlete's name, grad year and recruited position in one line after reading CLAUDE.md; update-pipeline confirms the name and time zone.
- **No made-up follow-up dates.** A school that has not replied gets no automatic "follow up by" date. The tracker review now lists the schools that have gone longest without contact, oldest first, and asks the family what to do. Dated next steps (film requested, an event, a date the family chose) are still logged and flagged when due.
- **Tiers match the tracker.** Any coach reply, compliance and form replies included, is Warm by default; Cold is contacted with no response yet.
- **Daily snapshot.** The tracker skill saves a dated copy into Pipeline/Archive before its first change each day, as the starter block says, and whenever the family asks.
- **No email as text.** With no email connected, draft-outreach stops and asks for Gmail, as the prompts do. It also shows a short bullet preview before writing the full email.
- **Names and rules match the Playbook files.** E01, E02, E03, E06 and E07 carry the Library's names; the June 15 rule is "before junior year" and applies to D1 only (D2, D3, NAIA and JUCO use the call close); "Instagram," "tier" and "Email Template Library" throughout; camp wording is gender-neutral.
- **First run gets a new chat.** Setup is its own chat; the setup skill now tells the family to start a new chat for P1-01, then run P2-01 in that same chat.
- README: first-time setup steps match the Setup Guide.

## Notes for this version (0.6.8)

From the 9/22 account test: in Cowork, sessions started from the sidebar (and some started inside the project) did not see the instructions pasted into the project's Instructions field. The email skill then drafted with every athlete detail left in brackets.

- **Project instructions now live in a file named CLAUDE.md** in the top level of the family's folder, so they go wherever the folder goes. The setup skill saves it there, shows the family what it says, and tells them in one sentence what the file is. It never tells a Cowork family to paste into the Instructions field.
- **draft-outreach and update-pipeline read CLAUDE.md first** and stop if they cannot find it, instead of drafting with placeholders or guessing details from folder names.
- **The starter block now matches P0-01 exactly**: the two role sentences and the four comma fixes are in, and the first working rule tells Claude to read CLAUDE.md.
- This reverses the 0.6.1 note below about family-facing wording. Families still hear "your project instructions"; the file behind them is CLAUDE.md.

## Notes for this version (0.6.7)

- The three skills now carry the 9/21 edits that were made after 0.6.6 but never shipped.
  0.6.6 on the channel had the older text, so anyone installing got a setup block and a
  tracker skill that no longer matched the Playbook files.
- The setup skill writes the same starter block as getseenplaybook.com/starter-instructions:
  volleyball only (no sport question), gender-neutral wording, the club team and high school
  lines, and the new sections, including MY TRACKER AND DATES (save each change in place, and
  a dated copy in Pipeline/Archive before the first change each day).
- The tracker skill writes to the tracker's real columns: Tier, All Contact Dates, Response?,
  Response Date(s) and Response Summary / Notes. The tracker has no Next Action column, so the
  next step goes on a "Next:" line in the notes, and the overdue check reads those lines and the
  Follow-Up Date on Calls & Visits. The tracker and setup skills say tier, not status, except
  for the Status column on Calls & Visits, and Cancelled is spelled Canceled to match the tracker.
- Draft outreach: E09 is for sharing the schedule during a tournament with coaches the family
  has already emailed, whether or not they replied.
- P0-01 has changed since (the role lines and the Stage 3 edits). The starter block gets copied
  again from the final P0-01 once that review is settled, in the next release.

## Notes for this version (0.6.6)

- New codes, same templates and prompts. The email templates are now E01 through E14 (they
  were T01 through T14). The tournament cross-check is now P4-01 (was TP-01), and the two
  tracker updates are P5-01 and P5-02 (were TP-02 and TP-03). TP meant two different things,
  so every prompt now carries the number of the phase it belongs to. The skills use the new
  codes to match the updated Playbook files. Nothing about how any of them work changed.
- The tracker skill checks two things before it logs anything. A call or visit on the Calls
  and Visits sheet carries a Status (Planned, Completed, Canceled), and a past date alone does
  not mean it happened. And an empty search of one mailbox is reported as exactly that, not as
  proof that nothing was sent, because parents and athletes often send from different accounts.
- One em dash removed from the setup skill.

## Notes for this version (0.6.5)

- The setup skill no longer promises a Targeting Brief file or an Athlete Dossier file in the
  folder it builds. There are no such files. Both are sections of the family's project
  instructions, written by P1-01 and P2-01 and reconciled before either is saved. The old
  scaffold taught families to expect two files that never arrive, and it taught the early-commit
  error the Playbook is built to prevent. Transcript stays in the scaffold.
- This is a content-only release. It carries the fix that landed after 0.6.4 shipped, so anyone
  already on 0.6.4 gets it.

## Notes for this version (0.6.4)

- Time zone handling now has a mechanism behind it, not just a rule. Setup asks the family for
  their time zone and stores it as a standard zone name in their project instructions, and the
  tracker skill resolves today's date against that zone before it writes anything, instead of
  trusting its own clock (which runs on UTC and rolls to tomorrow while it is still evening in
  the US). Tracker updates also report the date they logged against.

## Notes for this version (0.6.3)

- Model guidance is now evergreen: setup says to use the most capable model available (the highest-level option in the picker) instead of naming a specific model, so it stays correct as the model lineup changes. No behavior change.

## Notes for this version (0.6.2)

- draft-outreach now references the Email Template Library by its current name (the file was renamed from Email Template Packet on 7/1/26). No behavior change.

## Notes for this version (0.6.1)

Renamed to the Get Seen Playbook (plugin slug `get-seen-playbook`), and folded in the fixes from the live Windows setup test:

- **Use the most capable model for setup** (the highest-level option available): the Brief, Dossier, and pipeline audit are reasoning-heavy.
- **Do not publish the Targeting Brief alone.** Build it as a draft, reconcile against the Dossier (weighting net measurables like approach touch, not height alone), review with the family, then save the combined profile only once it reads right.
- **Branch on prior coach contact** after setup: if the family already has outreach, connect Gmail and run a full pipeline audit before building a new list.
- **Shell first for batch outreach**, and **hook edits after drafting default to paste-in**, not a new draft.
- **Family-facing wording says project Instructions**, not CLAUDE.md (Cowork stores instructions in-app, not as a file).
- Outreach templates now cover **E01 through E14**.

## Notes for this version (0.6.0)

This version brings the starter project instructions up to the full set of operating rules
Alva runs in her own recruiting workspace, so a family's workspace behaves the same on day one.

New rules now written into the starter project Instructions by the setup skill:

- **Confirm the folder is connected** before doing anything, and stop rather than work blind.
- **Keep a running to-do list** and update it every session (done / in progress / next).
- **Preview an email** as bullets and get the okay before drafting it.
- **Ask before creating another draft** when one already exists; never auto-replace.
- **Nudge on stale drafts** that have sat unsent more than 24 hours.
- **Reply in the same thread** on prior-contact emails, with a new subject line.
- **Address the head coach plus the recruiting coordinator**, verified on the athletics site.
- **Do not log a send until confirmed** sent (or seen in the Sent folder).
- **Resolve today's date in the family's time zone** before writing any date, rather than
  trusting the assistant's own clock, which runs on UTC and rolls over to tomorrow while it is
  still evening in the US. The family's zone is captured at setup and stored in their project
  instructions.
- **Screen schools on both academic and athletic fit**, never one alone.
- **Keep school lists alphabetical**.

Athlete-specific content (target divisions, geographic or institution exclusions, academic
path, stats, film, contact details) is deliberately NOT in the starter set. Each family builds
that through P1-01 and P2-01.

## Notes for this version (0.5.0)

This version makes every numbered prompt runnable by code in a fresh workspace.

- **The setup skill now points the workspace at the Prompt Library.** The starter project
  instructions list the Prompt Library as a project file and tell Claude to open it and run
  the matching prompt whenever the family names a code (or describes a task that maps to one),
  and to confirm before running when the match is unclear. Before this, the starter file named
  the Guide, Email Templates, and Tracker but not the Prompt Library, so "run P3-03" could come
  back empty. Now any P, M, or E01 through E14 prompt runs by code.
- This also makes the new **P3-05 (Research and Vet Schools)** prompt reachable
  by code: it researches and sorts a list or batch into Yes / Maybe / Pass and stops, with no
  outreach drafted, so a family can vet before they commit.
- Skills logic is otherwise unchanged from 0.4.0.

### Earlier: version 0.4.0

This version wires the last two skills to the real product, so DIY buyers get the genuine
Playbook, not placeholder logic.

- **draft-outreach now uses the real Email Templates.** It selects the correct template (E01
  through E09) for the situation and stage, pulls that template's wording from the family's
  own Email Template packet in their project folder, and fills the brackets from the athlete's
  project instructions. It locks the greeting (by time of day) and the close (before or after
  June 15 of junior year), verifies coach emails, and saves the result as a Gmail draft for
  the family to review and send. It never auto-sends.
- **update-pipeline now follows P5-02.** A pasted coach reply is classified the Playbook way
  (genuine interest, compliance template, camp invite, or something else), the school moves to
  the real status set (Hot, Warm, Cold, Dead), and the tracker updates in place: status, last
  contact date, and notes. Batch outreach the family sent follows P5-01 (logged as Cold).
  Coach replies are handed off to draft-outreach template E07 in a dedicated thread rather
  than answered inside the update. The "surface what is overdue" safety net is preserved.
- The setup skill is unchanged: it builds the real folder structure, moves the family's real
  Pipeline Tracker into place, writes the starter project instructions, and points the family
  to the first-run prompts (P1-01, then P2-01).
- `~~email` is the connector placeholder. Most families use Gmail.

### Earlier: version 0.3.0

- v0.3.0 setup tweaks from a real run: grad year accepts any year (including 2030 and beyond),
  club team and high school captured as separate fields, the confusing "essentials" summary
  line removed, and after P1-01 and P2-01 the combined Brief and Dossier is saved as the
  project Instructions (asking before replacing the project Instructions).
- The setup skill matches the Playbook's actual setup guide: it builds the real folder
  structure (Pipeline/Archive, Targeting Brief, Athlete Dossier, Transcript), moves the
  family's real Pipeline Tracker into place, writes the starter project instructions, and
  points the family to the first-run prompts (P1-01, then P2-01).
