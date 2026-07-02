# The Get Seen Playbook (Cowork plugin)

This plugin runs the parent-side work of college recruiting. It sets up a family's project,
keeps their pipeline tracker current, and drafts coach outreach in the Playbook voice. It
complements recruiters. It does not replace them.

## What it does

| Skill | What the family says | What happens |
| --- | --- | --- |
| Set up my recruiting project | "Get me started" | Collects the athlete profile, builds the pipeline tracker, writes the project file |
| Update my pipeline | "Here is a coach reply" / "I sent this" | Updates the tracker, schedules the follow-up, flags what is overdue |
| Draft outreach | "Draft an email to [school]" | Writes the coach email and saves it as a Gmail draft to review and send |

## First-time setup for a family (about 15 minutes)

1. Install the Claude desktop app and sign into a Claude plan.
2. Accept this plugin when it appears in the chat.
3. Point Cowork at a folder for the athlete (an empty folder is fine).
4. Run "Set up my recruiting project" and answer the questions.
5. Connect Gmail the first time you draft outreach (optional but recommended).

After that, the two skills the family uses most are "Update my pipeline" and "Draft
outreach." The tracker stays current on its own instead of getting forgotten.

## Privacy

The athlete's information and the family's inbox stay on the family's own machine and
account. The family connects their own email. Nothing is shared back to anyone.

## Notes for this version (0.6.2)

- draft-outreach now references the Email Template Library by its current name (the file was renamed from Email Template Packet on 7/1/26). No behavior change.

## Notes for this version (0.6.1)

Renamed to the Get Seen Playbook (plugin slug `get-seen-playbook`), and folded in the fixes from the live Windows setup test:

- **Use the most capable model for setup** (Opus or higher): the Brief, Dossier, and pipeline audit are reasoning-heavy.
- **Do not publish the Targeting Brief alone.** Build it as a draft, reconcile against the Dossier (weighting net measurables like approach touch, not height alone), review with the family, then save the combined profile only once it reads right.
- **Branch on prior coach contact** after setup: if the family already has outreach, connect Gmail and run a full pipeline audit before building a new list.
- **Shell first for batch outreach**, and **hook edits after drafting default to paste-in**, not a new draft.
- **Family-facing wording says project Instructions**, not CLAUDE.md (Cowork stores instructions in-app, not as a file).
- Outreach templates now cover **T01 through T13**.

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
- **Count dates in local time zone**, not UTC, so late sends log on the right day.
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
  back empty. Now any P, TP, M, or T01 through T13 prompt runs by code.
- This also makes the new **P3-05 (Research and Vet Schools, research only)** prompt reachable
  by code: it researches and sorts a list or batch into Yes / Maybe / Pass and stops, with no
  outreach drafted, so a family can vet before they commit.
- Skills logic is otherwise unchanged from 0.4.0.

### Earlier: version 0.4.0

This version wires the last two skills to the real product, so DIY buyers get the genuine
Playbook, not placeholder logic.

- **draft-outreach now uses the real Email Templates.** It selects the correct template (T01
  through T09) for the situation and stage, pulls that template's wording from the family's
  own Email Template packet in their project folder, and fills the brackets from the athlete's
  project instructions. It locks the greeting (by time of day) and the close (before or after
  June 15 of junior year), verifies coach emails, and saves the result as a Gmail draft for
  the family to review and send. It never auto-sends.
- **update-pipeline now follows TP-03.** A pasted coach reply is classified the Playbook way
  (genuine interest, compliance template, camp invite, or something else), the school moves to
  the real status set (Hot, Warm, Cold, Dead), and the tracker updates in place: status, last
  contact date, and notes. Batch outreach the family sent follows TP-02 (logged as Cold).
  Genuine warm leads are handed off to draft-outreach template T07 in a dedicated thread rather
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
