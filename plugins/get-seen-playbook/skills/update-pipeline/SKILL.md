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
itself. This skill follows the Playbook's tracker-update prompts: P5-02 for a coach response,
P5-01 for batch outreach the family sent.

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
and use that date for every write that follows: contact dates, response dates, follow-up dates,
snapshot filenames, and any "sent today" count. If the project instructions do not name a time zone,
ask the family for it once, use it for this session, and tell them to add it to their
instructions so it holds next time.

Dates that come from outside get converted before they are logged, not after. A send timestamp
from an email tool may be stored in UTC, so an email sent late in the evening can show under
the next calendar day. Convert it to the family's local date first, so the tracker and the
daily counts agree.

## Step 0b: A plan is not a record

The Calls & Visits sheet holds two things that look identical once written down: calls and
visits that actually happened, and ones that are only scheduled. Nothing in the row shape tells
them apart, so anything reading that sheet later will assume every row happened.

Column A of that sheet is **Status**, a dropdown with three values: Planned, Completed,
Canceled. Every row gets one, and it is the first thing you write, not the last.

Set it to Planned when you log something that has not happened yet, and leave the fields that
can only be filled in afterward empty: Duration (min), Key Topics Covered, Level of Interest,
Follow-Up Date. Move it to Completed when the family confirms it happened, and fill the rest in then. Set
it to Canceled if it fell through, and say why in Parent Notes. Do not delete a canceled row. The
prep in it stays useful for the rescheduled date, and Type still records what it was going to be.

Before you treat any past-dated entry as something that occurred, read its Status. A date in the
past is not evidence that it happened. If Status is blank or still Planned, you do not know, so
ask the family rather than fill it in yourself. Ask the family rather than
assume, and never build a follow-up action on top of an unconfirmed event. Chasing a family for
a thank-you note about a visit they never took is worse than saying nothing at all.

## Step 0c: A finding from one mailbox stays a finding about one mailbox

The email tool the family connects usually reaches ONE account. Parents often send from their
own address and athletes from theirs, and neither mailbox can see the other. A search that comes
back empty tells you what is not in the mailbox you can see. It does not tell you that nothing
was sent.

So write down what you actually checked and scope the conclusion to it. "Nothing found in the
athlete's sent mail since 9/1" is honest. "Nothing has been sent" is not, unless every account
in play is connected.

Never raise a flag, an overdue item, or a priority ranking on evidence that covers only part of
the picture. If the gap matters, ask the direct question: did you send this from your own
account? One question settles it. Writing a caveat next to a conclusion does not cancel the
conclusion, and the conclusion is the part the family reads and acts on.

## Step 1: Read the input

The family will paste or describe one of these:

- A coach's reply email (paste the text or upload a screenshot)
- A note that they sent outreach to one or more schools
- A tier change ("Coach said they are coming to watch at the tournament")

Identify which school and coach it concerns by reading the response against the current
tracker. If the school is not yet in the tracker, add a new row. Do not invent coach names or
emails. If something is unknown, leave it blank.

## Step 2: If it is a coach response, run the P5-02 logic

This is the heart of the skill. Review the coach's email against the current tracker and work
out, in this order:

1. **Which school and coach** the email is from.
2. **What kind of response it is**: genuine interest, a compliance template (an automated or
   form reply), a camp or ID clinic invite, or something else. Say which, and why.
3. **What tier the school should move to**, using the Playbook's four tiers, and why:
   - **Hot**: genuine, active interest. A coach engaging directly, wants to talk, wants film
     because they are interested, or a real back-and-forth.
   - **Warm**: real but early or conditional. Following along, will keep an eye out, will
     evaluate at an event, or interested but not yet active.
   - **Cold**: contacted, no meaningful engagement yet, or a generic compliance reply.
   - **Dead**: a clean pass. Not recruiting this position or year, or fully committed
     elsewhere. Leave the row as a record.
4. **Exactly what to update** in the tracker, using its real column names: Tier, Response?
   (YES), Response Date(s) (add today's date), and Response Summary / Notes (quote the useful
   part of the coach's message).

## Step 3: If it is outreach the family sent, run the P5-01 logic

For each school the family emailed, add or update the row on the All Outreach tab: add today's
date to All Contact Dates, fill Coach Name(s), Coach Email(s) and Tournament(s) Referenced if
they are known, and set Tier to **Cold** (contacted, no reply yet) for a new school. This is the
batch-outreach log.

## Step 4: Update the row and note the next step

Use the tracker's own column names. Do not add columns the family did not ask for.

On the **All Outreach** tab, update the matching row: Tier, Response?, Response Date(s), and
Response Summary / Notes. Then move the row to the tab that matches its new tier (Hot, Warm,
Cold or Dead) so the tier tabs and the Tier column agree.

The tracker has no Next Action column. Write the next step as the last line of Response Summary /
Notes, starting with "Next:" and a date, for example:

- Hot reply asking for film: "Next: send film link by [date 1 to 2 days out]"
- Warm, watching at an event: "Next: send tournament schedule before [event]"
- Cold, just contacted: "Next: follow up by [date 7 to 10 days out]"
- Dead: no next step; leave the row as a record

When a call or visit is involved, log it on the **Calls & Visits** tab instead, and put the next
step in Action Items / Follow-Up with a Follow-Up Date.

## Step 5: Coach-reply hand-off (do not draft the reply here)

If a coach replied, do not draft a reply inside this update. Tell the
family to run draft-outreach with template E07 in a dedicated conversation for that coach.
Every coach who replies gets their own thread. E07 is a relationship conversation, not a batch
operation.

## Step 6: Surface what is overdue (the safety net)

After updating, scan the whole tracker and report anything due today or already past, grouped
as "Overdue" and "Due this week." Look at the dates in "Next:" lines in Response Summary / Notes
and at Follow-Up Date on the Calls & Visits tab. This is the safety net that keeps the
pipeline from going quiet. Keep it short and specific.

Every item you surface here has to clear Step 0b and Step 0c first. Do not list a follow-up that
hangs off an unconfirmed call or visit, and do not list something as not sent when you could only
see one of the family's accounts.

## Step 7: Confirm

Tell the family in one or two lines what changed (school, new tier, next step) and what is
now due next. If they asked for a snapshot, confirm the dated copy was saved to
`Pipeline/Archive`.

Include the date you logged against, written out (for example "logged 2026-08-30"). It is a
one-second check for the family and it catches a wrong-day entry on the spot, while it is
still cheap to fix.

## Voice

Real and direct, not corporate. No em dash characters. Stay on the parent-side work. Do not
give recruiting advice that steps into a recruiter's role.
