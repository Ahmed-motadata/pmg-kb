# Outgoing Email Servers

**Path:** Admin → Support Channels → Emails → Outgoing Email Servers
(`/admin/support-channels/emails?tab=outgoing`)

Configures the SMTP (or Microsoft) servers ServiceOps uses to send outbound email. The
page description reads: "Configure SMTP servers used to send outbound email."

## Page layout

```
Outgoing Email Servers
Configure SMTP servers used to send outbound email.  View Setup Guide ↗

                    [ Configure Outgoing Email Rules ] [ Add Outgoing Email Servers ]
┌───────────────────────────────────────────────────────────────────────────────┐
│ <server name>                                  [Test Connection] ✎ 🗑          │
│ Email …        Protocol …        Reply-To Email …                             │
│ Sender Name …  Email Provider …  Server …                                     │
│ Port …         Security Type …   Username …                                   │
│ Email Auth Type … Enabled …      Primary …                                    │
│ Proxy Server …                                                                │
└───────────────────────────────────────────────────────────────────────────────┘
⏮ ◀ 1 ▶  [25 ▾] Items Per Page                          Showing 1-1 of 1 items
```

- **View Setup Guide** opens the product documentation for outgoing email servers in a
  new tab.
- **Configure Outgoing Email Rules** opens the rules dialog (see the rules file).
- **Add Outgoing Email Servers** opens the full-page add form (see the form file).

## Each server card

Each configured server appears as a card showing the server's name and these read-only
fields:

| Field | Meaning |
|---|---|
| Email | The address mail is sent from |
| Protocol | SMTP or MAPI |
| Reply-To Email | Address replies are directed to |
| Sender Name | Display name on outgoing mail |
| Email Provider | Microsoft or Other |
| Server | Mail server host (e.g. smtp.gmail.com) |
| Port | Mail server port (e.g. 587) |
| Security Type | None, TLS or SSL |
| Username | Login used to authenticate |
| Email Auth Type | Basic Auth or OAuth |
| Enabled | Yes / No |
| Primary | Yes / No — the platform's default outgoing server |
| Proxy Server | The proxy used, or "---" when none |

Card actions:

- **Test Connection** — tries the connection with the saved settings.
- **Pencil icon** — opens the edit form at
  `/admin/support-channels/outgoing-email-config-edit/<id>`; the edit form has the same
  fields as the add form.
- **Red trash icon** — deletes the server.

## Paging

Footer pager with first/previous/next arrows, page number, an items-per-page dropdown
(default 25) labelled "Items Per Page", and a count line such as "Showing 1-1 of 1
items".
