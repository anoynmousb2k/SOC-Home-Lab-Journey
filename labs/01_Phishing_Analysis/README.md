# 01 — Phishing Analysis

Status: **In Progress**

Phishing is often the first ticket a SOC analyst sees. In this module I am learning how to read a message the way an analyst would: headers first, then authentication, then the body, URLs, and attachments.

I am following TCM Security's SOC 101 phishing lessons and turning each one into a write-up in this repo.

## Lessons

| Lesson | Folder | Status |
| --- | --- | --- |
| 01 Header & Sender Analysis | [`01_Header_&_Sender_Analysis/`](01_Header_&_Sender_Analysis/README.md) | Done |
| 02 Email Content Analysis | — | Upcoming |
| 03 URL Analysis | — | Upcoming |
| 04 Attachment Analysis | — | Upcoming |

## What this module covers

- Reading `.eml` files and email headers
- SPF, DKIM, and DMARC (and why a "pass" is not the whole story)
- Display-name spoofing and `From` vs `Reply-To` mismatches
- Hidden tracking pixels and what they leak when a message is opened

## Artifacts

Lesson files live next to each write-up. Screenshots for the whole repo stay in [`images/`](../../images/).
