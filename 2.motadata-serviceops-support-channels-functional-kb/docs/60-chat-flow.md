# Virtual Agent — Chat Flow

**Path:** Admin → Support Channels → Virtual Agent → Chat Flow
(`/admin/support-channels/ai-bot?tab=chat_flow`)

The conversations the Virtual Agent (chatbot) can hold, across every connected channel.
The page description reads: "Design conversational flows the bot follows across
channels."

## Page layout

- A **Search** box and an **All** filter over the flow list.
- Header buttons: **Settings**, **Train Model**, **Manage Variable**, **Create Chat
  Flow** (dark). The dialogs behind Settings / Manage Variable / Create are described
  in the next file.
- **Train Model** retrains the bot on the current flows and examples (not run during
  this capture).
- A table with columns **Name · Description · Enabled · Actions**.

## The flow list

Each row is one flow with an Enabled toggle (flipping it takes effect immediately and
shows the toast "Chat Flow has been updated successfully."), a pencil (edit) and — for
flows that are deletable — a red trash with the confirmation "Are you sure, you want to
delete Chat Flow?" (Cancel / Yes).

This environment ships 15 flows ("Showing 1-15 of 15 items"), all Enabled:

| Name | Description |
|---|---|
| Non Login Fall Back Flow | Agent not understand inserted text or Not having permission for NonLogin Users |
| Non Login Greeting Flow | Use for Non Login Greeting |
| Unlock Account Flow | When Ldap User wants to Unlock Account |
| Forgot Password Flow | When User Forgot his Password |
| Chat with Technician | Guest user can Chat with Technician |
| Fall Back Flow | Agent not understand inserted text |
| Help Full Flow | When user want help |
| Transfer To Technician | Use To transfer control from agent to technician |
| My Name | Use to ask user`s name |
| Bot Name | Use to ask for bot name |
| Hello | When user say hello |
| Greeting | Use for Greeting |
| Pending Approval | When request is pending for approval |
| Open Request | When user want to open request |
| Create Request | When User want to create request |

The first five rows (the login/greeting/account flows) show only the pencil — they
cannot be deleted. The remaining flows show both pencil and trash.
