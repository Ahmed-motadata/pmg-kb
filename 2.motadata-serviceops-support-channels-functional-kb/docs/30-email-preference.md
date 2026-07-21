# Email Preference

**Path:** Admin → Support Channels → Emails → Email Preference
(`/admin/support-channels/emails?tab=emailpreference`)

Global switches for how email becomes tickets and how replies are treated. The page
description reads: "Set defaults for email formatting, signatures, and behavior."
Changes take effect on **Update**; **Cancel** discards them.

## Settings

Toggles (state shown is this environment's current setting):

| Setting | State here |
|---|---|
| Enable Email to Ticket | On |
| Allow Guest User to generate request from E-mail to Ticket | On |
| Use "Reply-To" email address to create Requester ? (If yes, then use reply-to email address while creating requester, otherwise use from email address.) | On |
| For forwarded emails by Technicians, consider the original sender as Requester | On |
| Allow User to select Outgoing Email | Off |
| Allow Ticket Creation when Incoming Mail Server Address is Added in CC | On |
| Allow Ticket Creation when Incoming Mail Server Address is Added in BCC | On |

Other controls:

- **Select Recipient Type Considered as CC User for Requests** — a multi-select of
  recipient types; here it holds one tag, **CC User**.

- **On reply received from requester for closed request** — radio, one of:
  - **Add reply to request** (selected here)
  - **Reopen request and add reply to request**
  - **Create new request**

- **On reply email received from other than assigned technician on request** — radio,
  one of:
  - **Add reply mail as collaboration** (selected here)
  - **Add reply mail as reply**
