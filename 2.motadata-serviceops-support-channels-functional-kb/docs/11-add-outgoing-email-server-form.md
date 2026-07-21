# Add Outgoing Email Servers — form

**Path:** `/admin/support-channels/outgoing-email-config-create` (opened by the **Add
Outgoing Email Servers** button; the pencil on a server card opens the same form
pre-filled at `/admin/support-channels/outgoing-email-config-edit/<id>`).

Full-page form. Header: a back chevron (returns to the list), the title, and **Save** /
**Cancel** buttons. Leaving a required field empty shows "<Field> field is required" in
red under the field.

## Fields

The form changes with **Protocol** and **Email Provider**. The fullest variant
(Protocol = SMTP, Provider = Other) is:

| Field | Required | Type | Default | Choices / behavior |
|---|---|---|---|---|
| Name | Yes | Text | — | Display name of this server entry |
| Email | Yes | Text | — | Address mail is sent from |
| Protocol | Yes | Choice | — ("Select") | SMTP, MAPI |
| Sender Name | Yes | Text | — | Shown only for SMTP |
| Email Provider | Yes | Tile choice | — | Two tiles: **Sign in with Microsoft**, **Other** |
| Server | Yes | Text | — | Shown when Provider is Other |
| Port | Yes | Number (with +/- steppers) | 25 | SMTP only; hidden for MAPI |
| Security Type | Yes | Choice | — | None, TLS, SSL (SMTP only; hidden for MAPI) |
| Authentication Needed | — | Toggle | Off | When On, the auth fields below appear |
| Email Auth Type | — | Segmented choice | Basic Auth | Basic Auth, OAuth |
| Username | Yes | Text | — | With authentication on |
| Password | Yes | Password (eye icon reveals) | — | Basic Auth only |
| Client ID | Yes | Text | — | OAuth only |
| Client Secret | Yes | Text | — | OAuth only |
| Authorization Url | Yes | Text | — | OAuth only; placeholder `https://oauth2.example.com/auth` |
| Token URL | Yes | Text | — | OAuth only; placeholder `https://oauth2.example.com/token` |
| Scope | Yes | Text | — | OAuth only |
| Redirect URL | Read-only | Text with copy button | `http://yash.motadata.com/oauth/callback` | OAuth only; copy this into the identity provider |
| Reply-To Email | Yes | Text | — | |
| Proxy Server | No | Search picker | — | Searches the proxy servers configured in the platform; in this environment the list is empty ("No Data Found") |
| Enabled | — | Toggle | On | |
| Primary | — | Toggle | Off | Marks this server as the platform default |

Protocol variants:

- **SMTP** shows Sender Name, Server, Port and Security Type.
- **MAPI** drops Sender Name, Port and Security Type; only Server remains alongside the
  authentication block.

Choosing **Sign in with Microsoft** as the provider connects a Microsoft account
through Microsoft's own sign-in. Completing it needs a real Microsoft account, which
was not available, so the signed-in variant is not documented here.

## Filters section

Below the main fields sits a **Filters** block that limits which mail this server
handles:

- **Filter Type** — radio: **Allow** / **Ignore** (default Ignore).
- **Emails** — a "+" button adds an inline text entry with a green check (confirm) and
  red cross (cancel). Confirming while empty shows "Email field is required".
- **Domains** — same pattern; placeholder "Domain"; empty confirm shows "Domain field
  is required".
