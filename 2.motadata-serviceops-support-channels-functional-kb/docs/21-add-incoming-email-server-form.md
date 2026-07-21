# Add Incoming Email Server — form

**Path:** `/admin/support-channels/incoming-email-config-create` (opened by the **Add
Incoming Email Server** button; the pencil on a card opens the same form pre-filled).

Full-page form with back chevron, title, **Save** / **Cancel**. Empty required fields
show "<Field> field is required" in red.

## Fields

| Field | Required | Type | Default | Choices / behavior |
|---|---|---|---|---|
| Name | Yes | Text | — | Display name of this mailbox entry |
| Email | Yes | Text | — | The mailbox address |
| Protocol | Yes | Choice | — ("Select") | IMAP, MAPI, POP3 |
| Technician Group | No | Search picker | — | Searches technician groups; tickets from this mailbox go to the picked group |
| Category | No | Search picker | — | Searches categories to stamp on created tickets |
| Proxy Server | No | Search picker | — | Configured proxy servers ("No Data Found" here) |
| Email Provider | Yes | Tile choice | — | **Sign in with Microsoft** / **Other** |
| Server | Yes | Text | — | With Provider = Other |
| Port | Yes | Number | 0; changes to 993 when Protocol = IMAP is picked | |
| Security Type | Yes | Choice | — | None, TLS, SSL |
| Email Auth Type | Yes | Segmented choice | Basic Auth | Basic Auth, OAuth. There is no "Authentication Needed" toggle here — an incoming mailbox always authenticates |
| Username | Yes | Text | — | |
| Password | Yes | Password (eye reveal) | — | Basic Auth only |
| Client ID / Client Secret / Authorization Url / Token URL / Scope | Yes | Text | — | OAuth only; Redirect URL is read-only with a copy button (`http://yash.motadata.com/oauth/callback`) |

Toggles:

| Toggle | Default | Meaning |
|---|---|---|
| Enabled | On | Whether the mailbox is polled |
| Primary | Off | The default incoming mailbox |
| Outgoing Email Servers | Off | Also register this account as an outgoing server |
| Real Time Scanning | Off | Appears when Protocol = IMAP; watches the mailbox continuously instead of on the polling schedule |

Choosing **Sign in with Microsoft** connects the mailbox through Microsoft's sign-in;
this needs a real Microsoft account, which was not available.

## Filters section

Same pattern as the outgoing form, with one extra list:

- **Filter Type** — radio **Allow** / **Ignore** (default Ignore).
- **Emails** — "+" adds an inline entry (✓ confirm / ✗ cancel); empty confirm shows
  "Email field is required".
- **Domains** — placeholder "Domain"; "Domain field is required" when empty.
- **Keywords** — a third list unique to incoming servers, for filtering mail by
  keyword.
