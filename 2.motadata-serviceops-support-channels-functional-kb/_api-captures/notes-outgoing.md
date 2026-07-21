# Working notes — Outgoing Email Servers (captured live 2026-07-20)

## List page /admin/support-channels/emails?tab=outgoing
- Title "Outgoing Email Servers", subtitle "Configure SMTP servers used to send outbound email."
- "View Setup Guide" link → https://docs.motadata.com/serviceops-docs/admin-section/support-channels/emails/outgoing-email-server (new window)
- Buttons top-right: "Configure Outgoing Email Rules" (secondary), "Add Outgoing Email Servers" (primary/dark)
- Server card: name (e.g. "test"), Test Connection button, pencil edit icon (→ /admin/support-channels/outgoing-email-config-edit/{id}), red trash delete icon
- Card fields (3-col grid): Email, Protocol, Reply-To Email / Sender Name, Email Provider, Server / Port, Security Type, Username / Email Auth Type, Enabled, Primary / Proxy Server ("---" when unset)
- Footer pager: first/prev/next-page arrows, page number, items-per-page dropdown (25 shown) "Items Per Page", right side "Showing 1-1 of 1 items"

## Add form /admin/support-channels/outgoing-email-config-create
Header: back chevron (→ outgoing list), title "Add Outgoing Email Servers", Save (dark), Cancel.
Inline validation style: "<Field> field is required" in red under field.

Fields (SMTP + Other, the fullest variant):
| Field | Req | Type | Default | Choices/notes |
| Name | yes | text | — | |
| Email | yes | text | — | |
| Protocol | yes | dropdown | none ("Select") | SMTP, MAPI |
| Sender Name | yes (SMTP only) | text | — | hidden when Protocol=MAPI |
| Email Provider | yes | tile choice | Other preselected visually | "Sign in with Microsoft" tile, "Other" tile |
| Server | yes | text | — | shown for Other |
| Port | yes | number spinner | 25 | SMTP only; hidden for MAPI |
| Security Type | yes | dropdown | none | None, TLS, SSL (SMTP only; hidden for MAPI) |
| Authentication Needed | — | toggle | Off | reveals below when On |
| Email Auth Type | — | segmented | Basic Auth | Basic Auth / OAuth |
| Username | yes | text | — | when auth on |
| Password | yes | password + eye reveal | — | Basic Auth only |
| Client ID | yes | text | — | OAuth only |
| Client Secret | yes | text | — | OAuth only |
| Authorization Url | yes | text | — | placeholder https://oauth2.example.com/auth |
| Token URL | yes | text | — | placeholder https://oauth2.example.com/token |
| Scope | yes | text | — | OAuth only |
| Redirect URL | read-only | text + copy icon | http://yash.motadata.com/oauth/callback | OAuth only |
| Reply-To Email | yes | text | — | |
| Proxy Server | no | searchable dropdown | empty | picks from configured proxy servers; "No Data Found" here (none configured); search box inside |
| Enabled | — | toggle | On | |
| Primary | — | toggle | Off | |

Filters section:
- Filter Type: radio Allow / Ignore (default Ignore)
- Emails: "+" button → inline text input with green ✓ confirm and red ✗ cancel; empty confirm → "Email field is required"
- Domains: "+" → input placeholder "Domain"; empty confirm → "Domain field is required"

MAPI protocol variant: keeps Email, Provider, Server, auth block, Reply-To, Proxy, toggles, Filters; drops Sender Name, Port, Security Type.
"Sign in with Microsoft": provider tile; completing it needs a real Microsoft account sign-in (not available) — couldn't verify because no Microsoft account.
Existing server "test": Email testalpha2409@gmail.com, Protocol SMTP, Provider Other, smtp.gmail.com:587 TLS, Basic Auth, Enabled No, Primary No, Proxy ---.
