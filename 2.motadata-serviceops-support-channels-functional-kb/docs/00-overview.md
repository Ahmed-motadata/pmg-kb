# Support Channels — Overview

Support Channels is an admin section of Motadata ServiceOps (Admin → Platform
Configuration → Support Channels). It holds every way requesters and technicians talk to
the service desk: email in and out, the self-service Support Portal, live Chat, and the
Virtual Agent chatbot with its per-channel messenger connections.

This guide describes the PMG ServiceOps environment at `http://172.16.15.185` as of
20 July 2026. All labels and options are copied from the live product.

## Where it sits

Open **Admin** (the technician portal's admin area) and look in the left sidebar under
**Platform Configuration**. The **Support Channels** group contains:

```
Support Channels
├── Emails
│   ├── Outgoing Email Servers      /admin/support-channels/emails?tab=outgoing
│   ├── Incoming Email Servers      /admin/support-channels/emails?tab=incoming
│   └── Email Preference            /admin/support-channels/emails?tab=emailpreference
├── Support Portal                  /admin/support-channels/support-portal
├── Chat                            /admin/support-channels/chat
└── Virtual Agent
    ├── Chat Flow                   /admin/support-channels/ai-bot?tab=chat_flow
    ├── Slack App Config            /admin/support-channels/ai-bot?tab=slack_app_config
    ├── Teams App Config            /admin/support-channels/ai-bot?tab=teams_app_config
    ├── Google Chat App Config      /admin/support-channels/ai-bot?tab=google_chat_app_config
    ├── Telegram App Config         /admin/support-channels/ai-bot?tab=telegram_app_config
    ├── Facebook Messenger App Config  /admin/support-channels/ai-bot?tab=messenger_app_config
    ├── WhatsApp Config             /admin/support-channels/ai-bot?tab=whatsapp_config
    ├── Viber App Config            /admin/support-channels/ai-bot?tab=viber_config
    └── Line App Config             /admin/support-channels/ai-bot?tab=line_app_config
```

## How the pieces relate

- **Outgoing Email Servers** send the platform's mail (notifications, replies). One
  server can be marked **Primary**. Per-module **Outgoing Email Rules** can route
  specific records through specific servers.
- **Incoming Email Servers** are the mailboxes ServiceOps polls (or scans in real time)
  to turn email into tickets. Each mailbox can point at a Technician Group and Category
  for the requests it creates, and **Incoming Email Rules** apply conditions and actions
  to arriving mail.
- **Email Preference** holds the global email-to-ticket behavior switches (guest
  senders, CC/BCC handling, what happens when someone replies to a closed request).
- **Support Portal** switches control what requesters can see and do in the self-service
  portal.
- **Chat** turns on live chat between requesters and technicians and sets its
  greeting/missed messages, engineers, and branding.
- **Virtual Agent** is the chatbot. **Chat Flow** defines the conversations it can hold;
  the eight **App Config** pages connect the same bot to Slack, Microsoft Teams, Google
  Chat, Telegram, Facebook Messenger, WhatsApp, Viber, and LINE.

## Patterns shared across these pages

- Every page has a title, a one-line description, and a **View Setup Guide** link that
  opens the matching page of the product documentation (docs.motadata.com) in a new tab.
- Settings pages end with **Update** and **Cancel** buttons; nothing is saved until
  Update is pressed.
- List pages (email servers, chat flows) have a footer pager: first/previous/next
  arrows, the page number, an items-per-page dropdown (default 25) labelled "Items Per
  Page", and a count line like "Showing 1-2 of 2 items".
- Required fields are marked with a red asterisk; submitting or leaving them empty shows
  an inline red message of the form "<Field> field is required".
- Toggles are small switches (green = on). Choice controls open a menu; pickers that
  search live data open a small panel with a Search box (showing "No Data Found" when
  the tenant has none).

## Files in this guide

See the README index one level up. One file covers one page (or one form / dialog set),
in the order of the sidebar.
