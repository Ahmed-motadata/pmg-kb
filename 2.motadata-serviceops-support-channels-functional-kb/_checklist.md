# Support Channels — coverage checklist (working file)

Environment: http://172.16.15.185 (PMG ServiceOps), login yash. Captured 2026-07-20.
Scope: Admin → Platform Configuration → Support Channels (sidebar group).

## Emails (/admin/support-channels/emails)
- [x] Outgoing Email Servers (?tab=outgoing) — docs/10
- [x] Add Outgoing Email Servers form (SMTP/MAPI, Basic/OAuth, Microsoft/Other, filters, validation) — docs/11
- [x] Configure Outgoing Email Rules dialog (8 module tabs, rule block, condition builder) — docs/12
- [x] Incoming Email Servers (?tab=incoming) incl. Unreachable badge, queue/sync pills, MAILCONREF error banner — docs/20
- [x] Add Incoming Email Server form (IMAP/MAPI/POP3, Real Time Scanning, Keywords filter) — docs/21
- [x] Configure Incoming Email Rules dialog (conditions + actions) — docs/22
- [x] Email Preference (?tab=emailpreference) — all toggles/radios — docs/30
- [x] View Setup Guide links (open docs.motadata.com pages in new tab)

## Support Portal
- [x] Full page, all 9 sections, every toggle + Requester Ticket Visibility — docs/40

## Chat
- [x] Full page — docs/50

## Virtual Agent (/admin/support-channels/ai-bot)
- [x] Chat Flow list (15 flows) — docs/60
- [x] Settings / Manage Variable / Create+Edit Chat Flow dialogs — docs/61
- [x] Slack (?tab=slack_app_config) — docs/70
- [x] Teams — docs/71
- [x] Google Chat — docs/72
- [x] Telegram — docs/73
- [x] Facebook Messenger (list + Messenger Settings + Add Messenger Page) — docs/74
- [x] WhatsApp — docs/75
- [x] Viber — docs/76
- [x] Line — docs/77

## Write-up
- [x] README.md index
- [x] docs/ one file per page (20 files)
- [x] Field tables per form
- [x] Review pass vs live app (outgoing list re-checked; matches)
- [x] Cleanup confirmed — no ZZ-KBPROBE- records were created (no admin config was
      saved at any point); the one shared thing touched by accident (the "Hello" chat
      flow's Enabled toggle) was switched back On and verified.

## Stated gaps (also in CLAUDE.md)
- Microsoft-provider sign-in variants (need a real Microsoft account).
- Chat-flow conversation designer behind a flow's name.
- Exact option lists of some search pickers (rules condition/action fields, Technician
  Group, Category, Font Family) — described as what they search instead.

## Out of scope (different sidebar groups, same URL prefix)
LDAP Configurations, SSO Configuration, SCIM Provisioning, Custom SSO, Chat Plugin
(/admin/integration).
