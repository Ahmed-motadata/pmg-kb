# Virtual Agent — Chat Flow dialogs

The Chat Flow page's header buttons open three dialogs. All are saved only when their
own Save / Update / Add button is pressed; Cancel discards.

## Settings

Titled **Settings**. Controls the bot as a whole:

- **Allow Virtual Agent Support** — master toggle (On here).
- **Greeting Flow** — picker over the flow list (set to "Greeting" here).
- **Fallback Flow** — picker over the flow list (set to "Fall Back Flow" here); the
  flow used when the bot does not understand.
- A per-channel block with one **Fallback Flow** picker for each connected channel —
  **WhatsApp, Teams, Line, Slack, Facebook Messenger, Telegram, Google Chat, Viber** —
  each defaulting to "Fall Back Flow" here.
- **Save** / **Cancel**.

## Manage Variable

Titled **Manage Variable**. Reusable values flows can insert:

- A **Create** button.
- A table with columns **Key · Value · Variable Name · Actions** and the standard
  pager. This environment has one variable: Key "Agent Name", Value "Aaksha", Variable
  Name "Agent_Name".
- **Cancel** closes.

## Create Chat Flow / Edit Chat Flow

**Create Chat Flow** (header button) and the pencil on a flow row open the same dialog
(titled "Create Chat Flow" or "Edit Chat Flow"):

| Field | Type | Notes |
|---|---|---|
| Name | Text | The flow's name |
| Description | Multi-line text | When the flow applies |
| List of Examples | Repeating text rows + **Add** | Example phrases users might type that should trigger this flow (the "Hello" flow has four) |
| Apply To | Checkboxes | **Select All**, then one per channel: Virtual Agent, Teams, Slack, Telegram, Facebook Messenger, WhatsApp, Viber, Line, Google Chat |

Buttons: **Save** (or **Update** when editing) / **Cancel**.

Opening a flow's name leads into the flow's conversation design itself; that designer
was not captured in this pass — this guide covers the flow list and its dialogs.
