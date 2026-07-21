# Working notes — Incoming Email Servers (captured live 2026-07-20)

## List page /admin/support-channels/emails?tab=incoming
- Title "Incoming Email Servers"; subtitle "Configure inbound mail servers and email-to-ticket rules."
- "View Setup Guide" link (docs.motadata.com incoming email server page)
- Buttons: "Configure Incoming Email Rules", "Add Incoming Email Server" (dark)
- Server cards. Header row per card: name + status badge ("• Unreachable" red when down) + right side: "Inbound Queue : N" pill, "Last Sync : Not Synced Yet" (clock icon) pill, Test Connection button, pencil edit, red trash.
- Card fields: Email, Protocol (e.g. imap), Technician Group, Username, Server, Port, Security Type, Email Auth Type, Enabled, Primary, Outgoing Email Servers (Yes/No), Real Time Scanning, Category, Proxy Server ("---" when unset)
- Error banner under a failing card: "MAILCONREF: Unable to connect to the mail server. Please verify the port number and firewall settings." + "View error details >" link (red banner)
- Pager identical to outgoing. "Showing 1-2 of 2 items"
- Existing: "bjh" (abc@b.com, imap 8.8.8.8:993 TLS, Basic Auth, Enabled Yes, Primary Yes, unreachable), "test" (testalpha2409@gmail.com, imap imap.gmail.com:993 SSL, Basic Auth, Enabled No)

## Add form /admin/support-channels/incoming-email-config-create
Header: back chevron (→ incoming list), "Add Incoming Email Server", Save, Cancel.
Validation: "<Field> field is required" inline red.

Fields:
| Field | Req | Type | Default | Choices/notes |
| Name | yes | text | — | |
| Email | yes | text | — | |
| Protocol | yes | dropdown | none | IMAP, MAPI, POP3 |
| Technician Group | no | search-picker | — | pick a technician group (assigns tickets from this mailbox) |
| Category | no | search-picker | — | pick a category |
| Proxy Server | no | search-picker | — | configured proxy servers; "No Data Found" here |
| Email Provider | yes | tiles | — | "Sign in with Microsoft" / "Other" |
| Server | yes | text | — | with Other |
| Port | yes | number | 0; auto 993 when IMAP selected | |
| Security Type | yes | dropdown | none | None, TLS, SSL |
| Email Auth Type | yes | segmented | Basic Auth | Basic Auth / OAuth (no "Authentication Needed" toggle here — auth always required) |
| Username | yes | text | — | |
| Password | yes | password+eye | — | Basic Auth |
| Client ID/Client Secret/Authorization Url/Token URL/Scope | yes | text | — | OAuth; Redirect URL read-only + copy (http://yash.motadata.com/oauth/callback) |
Toggles: Enabled (default On), Primary (Off), Outgoing Email Servers (Off), Real Time Scanning (Off; appears when Protocol=IMAP).
Filters: Filter Type Allow/Ignore (default Ignore); Emails +; Domains +; Keywords + (Keywords extra vs outgoing). Inline add with ✓/✗.

## Configure Incoming Email Rules — modal (to capture)
