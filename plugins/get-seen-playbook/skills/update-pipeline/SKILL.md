---
name: update-pipeline
description: >
  Keep the recruiting pipeline tracker current. Use when a user pastes a coach's reply,
  logs an email they sent, says update my tracker, log this response, mark this school, I
  heard back from a coach, or asks what is overdue or what is next. This is the skill that
  stops follow-ups from slipping.
---

# Update Pipeline

Take whatever the family gives you (a coach reply, a note that they sent outreach, a verbal
update) and update the family's Pipeline Tracker in place so the pipeline is always current.
The whole point of this skill: families miss follow-ups, and this makes the tracker update
itself. This skill follows the Playbook's tracker-update prompts: TP-03 for a coach response,
TP-02 for batch outreach the family sent.

Work on the family's one working tracker (the `[Athlete]_Recruiting_Pipeline` file in their
`Pipeline` folder). Update it in place. Never create "v2" or "final" copies. When the family
asks for a snapshot, save a dated copy into `Pipeline/Archive`.

**Dates use the family's local time zone, not UTC.** Every time you write a date into the
tracker (last contact, next action, or "today"), compute "today" in the family's local
time zone. Some tools, Gmail included, bucket sent messages by UTC, so an email sent late
in the evening local time can roll into the next calendar day. If a date comes from a
UTC-based source, convert it to local time before logging, so the tracker dates and any
"sent today" counts reconcile.

## Step 1: Read the input

The family will paste or describe one of these:

- A coach's reply email (paste the text or upload a screenshot)
- A note that they sent outreach to one or more schools
- A status change ("Coach said they are coming to watch at the tournament")

Identify which school and coach it concerns by reading the response against the current
tracker. If the school is not yet in the tracker, add a new row. Do not invent coach names or
emails. If something is unknown, leave it blank.

## Step 2: If it is a coach response, run the TP-03 logic

This is the heart of the skill. Review the coach's email against the current tracker and work
out, in this order:

1. **Which school and coach** the email is from.
2. **What kind of response it is**: genuine interest, a compliance template (an automated or
   form reply), a camp or ID clinic invite, or something else. Say which, and why.
3. **What status the school should move to**, using the Playbook's four statuses, and why:
   - **Hot**: genuine, active interest. A coach engaging directly, wants to talk, wants film
     because they are interested, or a real back-and-forth.
   - **Warm**: real but early or conditional. Following along, will keep an eye out, will
     evaluate at an event, or interested but not yet active.
   - **Cold**: contacted, no meaningful engagement yet, or a generic compliance reply.
   - **Dead**: a clean pass. Not recruiting this position or year, or fully committed
     elsewhere. Leave the row as a record.
4. **Exactly what to update** in the tracker: status, last contact date (today), and the
   notes field (quote the useful part of the coach's message).

## Step 3: If it is outreach the family sent, run the TP-02 logic

For each school the family emailed, add or update the row with today's date and status
**Cold** (contacted, no reply yet). This is the batch-outreach log.

## Step 4: Update the row and set the next action

Apply the changes to the matching row: Status, Last Contact (today's date), Notes, and a
sensible Next Action with a Next Action Date. Examples:

- Hot reply asking for film: Next Action "Send film link," due in 1 to 2 days
- Warm, watching at an event: Next Action "Send tournament schedule before the next event"
- Cold, just contacted: Next Action "Follow up," due in 7 to 10 days
- Dead: Next Action blank, leave the row as a record

## Step 5: Warm-lead hand-off (do not draft the reply here)

If the response is a genuine warm lead, do not draft a reply inside this update. Tell the
family to run draft-outreach with template T07 in a dedicated conversation for that coach.
Every warm-lead coach gets their own thread. T07 is a relationship conversation, not a batch
operation.

## Step 6: Surface what is overdue (the safety net)

After updating, scan the whole tracker and report anything where Next Action Date is today or
in the past, grouped as "Overdue" and "Due this week." This is the safety net that keeps the
pipeline from going quiet. Keep it short and specific.

## Step 7: Confirm

Tell the family in one or two lines what changed (school, new status, next action) and what is
now due next. If they asked for a snapshot, confirm the dated copy was saved to
`Pipeline/Archive`.

## Voice

Real and direct, not corporate. No em dash characters. Stay on the parent-side work. Do not
give recruiting advice that steps into a recruiter's role.
