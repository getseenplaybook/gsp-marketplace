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

## Step 0: Set today's date before you write anything

Do this first, before reading the family's input. Every date in this tracker is a local date
for the family, and the clock you are running on is not their clock. It runs on UTC, which is
ahead of every US time zone, so from early evening onward the date you see in session context
is already tomorrow. A coach reply logged at 9pm Tuesday lands on Wednesday, and a follow-up
set for seven days out quietly comes due in six.

So never take "today" from the date shown in session context, and never take it from a file
timestamp. Resolve it against the family's time zone, which is recorded in their project
instructions:

```
TZ=America/New_York date "+%Y-%m-%d %H:%M %Z"
```

Substitute the family's time zone for the one above. Run it once at the start of the session
and use that date for every write that follows: last contact, next action dates, snapshot
filenames, and any "sent today" count. If the project instructions do not name a time zone,
ask the family for it once, use it for this session, and tell them to add it to their
instructions so it holds next time.

Dates that come from outside get converted before they are logged, not after. A send timestamp
from an email tool may be stored in UTC, so an email sent late in the evening can show under
the next calendar day. Convert it to the family's local date first, so the tracker and the
daily counts agree.

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

Include the date you logged against, written out (for example "logged 2026-08-30"). It is a
one-second check for the family and it catches a wrong-day entry on the spot, while it is
still cheap to fix.

## Voice

Real and direct, not corporate. No em dash characters. Stay on the parent-side work. Do not
give recruiting advice that steps into a recruiter's role.
