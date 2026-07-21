# Incoming Email Servers

**Path:** Admin → Support Channels → Emails → Incoming Email Servers
(`/admin/support-channels/emails?tab=incoming`)

The mailboxes ServiceOps reads to create tickets from email. The page description
reads: "Configure inbound mail servers and email-to-ticket rules."

## Page layout

Header buttons: **Configure Incoming Email Rules** and **Add Incoming Email Server**
(dark). Below them, one card per mailbox, then the standard pager ("Showing 1-2 of 2
items" style).

## Each server card

The card header shows the server's name plus live status:

- a red **• Unreachable** badge when the mailbox cannot be reached;
- an **Inbound Queue : N** pill (mails waiting to be processed);
- a **Last Sync : …** pill with a clock icon (e.g. "Last Sync : Not Synced Yet");
- **Test Connection**, a pencil (edit) and a red trash (delete).

Card fields:

| Field | Meaning |
|---|---|
| Email | The mailbox address |
| Protocol | e.g. imap |
| Technician Group | Group assigned to tickets from this mailbox, or "---" |
| Username | Mailbox login |
| Server | Mail host (e.g. imap.gmail.com) |
| Port | e.g. 993 |
| Security Type | None, TLS or SSL |
| Email Auth Type | Basic Auth or OAuth |
| Enabled | Yes / No |
| Primary | Yes / No |
| Outgoing Email Servers | Yes / No — whether this entry also acts as an outgoing server |
| Real Time Scanning | Yes / No |
| Category | Category applied to tickets from this mailbox, or "---" |
| Proxy Server | Proxy used, or "---" |

## Error state

When a mailbox cannot connect, a red banner appears under its card with the exact
error, for example:

> MAILCONREF: Unable to connect to the mail server. Please verify the port number and
> firewall settings.

followed by a **View error details** link.
