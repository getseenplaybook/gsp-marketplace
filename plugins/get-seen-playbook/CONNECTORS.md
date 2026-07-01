# Connectors

## How tool references work

This plugin uses `~~email` as a placeholder for whatever email tool the family connects.
The plugin is tool-agnostic. It describes the workflow (save a draft) rather than naming one
specific product, so the same plugin works whether a family uses Gmail or Outlook.

## Connectors for this plugin

| Category | Placeholder | Options | Used by |
| --- | --- | --- | --- |
| Email | `~~email` | Gmail, Outlook | draft-outreach (to save coach emails as drafts) |

## What the family has to do

Each family connects their own email the first time they draft outreach. The plugin cannot
do this for them, and that is on purpose: the family's inbox and their athlete's information
stay on the family's own machine and account. Nothing is shared back.

If no email tool is connected, draft-outreach still works. It outputs the email as text to
copy and paste, and prompts the family to connect Gmail so future drafts save automatically.
