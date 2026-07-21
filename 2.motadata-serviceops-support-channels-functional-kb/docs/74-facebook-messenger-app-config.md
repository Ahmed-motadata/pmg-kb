# Virtual Agent — Facebook Messenger App Config

**Path:** Admin → Support Channels → Virtual Agent → Facebook Messenger App Config
(`/admin/support-channels/ai-bot?tab=messenger_app_config`)

Connects the Virtual Agent to Facebook Messenger. The page description reads: "Connect
the bot to Facebook Messenger for chat-based support."

Unlike the other channel pages this one is a **list of Messenger pages**, because a
Facebook presence can span several pages:

- **Add Messenger Page** (dark button) — opens the add dialog.
- A gear icon — opens **Messenger Settings**, a dialog holding a single **Verify
  Token** field with **Save** / **Cancel**.
- A table with columns **Name · Enabled · Actions** ("No Data Found" here — none are
  configured).

## Add Messenger Page — dialog

| Field | Type | Notes |
|---|---|---|
| Enabled | Toggle | When On, the fields below appear |
| Name | Text | The Facebook page's display name |
| Client ID | Text | |
| Page Id | Text | The Facebook page id |
| Allow Guest User | Toggle | |

Buttons: **Add** / **Cancel**.
