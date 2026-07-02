---
name: draft-outreach
description: >
  Draft a coach outreach email and save it as a Gmail draft. Use when a user says draft an
  email to a coach, write outreach to a school, reach out to a program, or names a school
  they want to contact. Picks the right Email Template (T01 through T13), pulls the wording
  from the family's Email Template Library, fills the brackets from the athlete's project
  instructions, and creates a draft in the connected email tool.
---

# Draft Outreach

Write a coach outreach email for a target school using the family's real Email Templates, and
save it as a draft in the family's connected email tool (`~~email`, typically Gmail) so the
family can review and send it themselves. Never send on the family's behalf. Draft only.

This skill runs the Playbook's outreach framework. It does not invent an email structure. It
selects the correct template, pulls that template's wording from the family's own Email
Template Library, and fills the brackets from the athlete's profile.

## Step 1: Confirm the Email Templates are in the workspace

The outreach templates live in the family's Email Template Library in their project folder
(the "Email Templates" file the setup skill placed there). If it is not in the folder, tell
the family to add it before drafting. Do not recreate the templates from memory. They are the
purchased product, and the family's copy is the source of truth for exact wording.

## Step 2: Pick the right template

Ask what is happening with this school, then choose the template that matches the situation
and stage. The thirteen templates and when each one is used:

- **T01 Initial Outreach, Between Tournaments**: first contact, no Instagram follow, no live
  tournament. The school has been researched and you are reaching out between events.
- **T02 Initial Outreach, School Attending Tournament**: first contact when the school is
  verified (via University Athlete) to be attending an upcoming tournament. Includes the
  tournament schedule block (jersey number, court, match times). Send 3 to 5 days out.
- **T03 IG Follow, Initial Outreach**: a coach followed on Instagram, or the athlete followed
  and the coach followed back. Send within 48 hours. Opener changes to thank them for the
  follow or the follow-back, then it follows T01.
- **T04 Referral Introduction**: a coach, recruiter, or advisor referred the athlete to this
  program. Lead with the referral and keep the pitch lighter.
- **T05 Pre-Tournament Pipeline Re-Engagement**: a previously contacted school, an upcoming tournament, and
  updated stats. Builds the case ("I have proven to be"). Includes the full schedule block.
- **T06 Updated Stats and Film, Re-Engagement**: months since last contact, new tournaments
  done, no response. Reply to the original thread, never a new email. New film only.
- **T07 Coach Responded, Now What (Warm Lead Nurture)**: a coach replied with genuine
  interest. This one is a relationship reply, not batch outreach. Give it its own dedicated
  conversation for that coach. The close changes depending on whether it is before or after
  June 15 of junior year.
- **T08 Post-Call / Post-Visit Thank You**: a coach call or campus visit has happened. Send
  within 24 hours. Reference something specific that was said or shown.
- **T09 Tournament Schedule Share**: a coach is already in the picture (responded, said they
  would watch, follows on IG, or you have emailed before) and a tournament is coming up. A
  short, friendly, athlete-driven touch with just the schedule and signature. No pitch, no
  stats, no film. If the coach has never heard from you, use T02 instead.
- **T10 Post-Tournament Recap**: a tournament just wrapped and you want to update coaches who
  watched or expressed interest. Recap how it went, note results, and point to new film if any.
- **T11 Pre-Camp Contact**: the athlete plans to attend a college's camp or ID clinic. Reach
  out before the camp to say she is coming and what to look for.
- **T12 Camp / ID Clinic Follow-Up**: the athlete just attended a college camp or ID clinic.
  Follow up within 24 to 48 hours, referencing something specific from the camp.
- **T13 Gracious Rejection Reply**: a coach replied with a clear no (not recruiting the
  position, roster full, or further along with others). Reply graciously to keep the door open
  for the future. A relationship reply, not batch outreach.

If the situation is unclear, ask one question to place it, then pick. Do not guess.

## Step 3: Gather what the template needs

Pull the athlete profile from the family's project Instructions: name, grad
year, positions, club team, high school, selling points, and the signature details (athlete
email, phone, Instagram handle). Do not use placeholders for anything that is already in the
project instructions. Ask only for what is missing or specific to this email:

- Target school, head coach name, and the coach email if drafting straight to Gmail (also
  flag the recruiting coordinator or assistant email if found, for the family to verify)
- The reason for reaching out now, which usually confirms the template choice
- For T02, T05, T09: the tournament name, dates, jersey number, court, and match times
- For T06: the original thread to reply to, and the new film link
- Anything school-specific the family wants to mention

Verify coach email addresses on the school's athletics site before including them, and tell
the family to confirm them too.

## Step 4: Lock the greeting and the close

Two choices set the tone across the email, straight from the master-prompt logic:

1. **Time of day the email will be sent**: morning uses "Hi" or "Good morning"; afternoon or
   evening uses "Hi." Ask and lock it.
2. **Before or after June 15 of junior year**: before, use the standard close; after, the
   close asks for the coach's availability for a call this week or next. Ask and lock it.

## Step 5: Write the email from the template

Use the chosen template's wording from the family's Email Template Library as the base. Fill every bracket
from the project instructions and the details gathered in Step 3. Keep it short, specific,
and athlete-driven: a coach should know in fifteen seconds who the athlete is, why this
school, and what to do next. Remove any structural labels the template carries (the blue
OPENER, CLOSE, and similar notes are instructions for the writer, not email content).

Voice rules: real and direct, never corporate or over-polished. Inclusive of parent and
athlete. Leverage the athlete's real work, not aspirational fluff. Do not use the em dash
character. Do not overstate. Do not write anything that positions the family as replacing a
recruiter.

## Step 6: Save it as a draft

Before saving, confirm the email connector (`~~email`, typically Gmail) is connected. Create
the draft with the coach email as the recipient if provided, the subject from the template,
and the body you wrote. Confirm to the family that the draft is in their inbox, ready to
review and send. Never auto-send.

If the family later wants to change a hook or any wording after the draft exists, do not
automatically create a new draft. Give them the revised text and ask whether they want a new
draft or would rather paste the edit into the draft they are already reviewing. Default to
paste-in. Only create a new draft if they explicitly ask, and tell them which earlier draft to
delete.

If no email connector is connected, output the full email as text for the family to copy, and
tell them they can connect Gmail so future drafts save automatically.

## Step 7: Offer to log it

After drafting, offer to log the outreach in the pipeline tracker via update-pipeline so the
follow-up is scheduled. For T07, remember it is a warm-lead reply: keep that coach in their
own thread and update their status accordingly.
