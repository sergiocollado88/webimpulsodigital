# LegalOS / Bufetly - AI-assisted Legal Operations Platform

## Problem
Law firms manage clients, matters, hearings, documents, billing, communications and court-portal checks across disconnected tools and manual routines. Missing a new assignment or hearing can create serious operational risk.

## Solution
A legal operations SaaS/CRM designed for law firms, combining practice management, AI-assisted workflows and automated monitoring.

## What I worked on
- Client, matter and document management.
- Calendar and hearing workflows with Panama timezone handling.
- Billing, accounts receivable, expenses and financial reporting.
- Role-based access, Row Level Security and an operator/admin back office.
- AI-assisted email drafting with guardrails against invented legal advice or facts.
- WhatsApp and email notification workflows.
- Automated court-portal monitoring architecture.
- Deduplication logic to prevent repeated hearing/case alerts.
- Review queue that converts verified portal findings into real case records.
- Credential vault design using AES-256-GCM encryption and server-side keys.
- Safe handling for CAPTCHA/MFA and human intervention.
- Mobile responsive redesign and production debugging.

## Stack
Next.js, TypeScript, React, Supabase/PostgreSQL, RLS/RPCs, OpenAI/Anthropic SDKs, Zod, email/IMAP integrations, WhatsApp integrations, cron jobs and server-side encryption.

## Engineering decisions
### Deterministic automation
Critical workflow rules such as permissions, deduplication, case creation and notification state are handled by deterministic code and database constraints rather than delegated to the language model.

### Security
Sensitive portal credentials are encrypted server-side and never returned to the browser. Access checks are enforced in the database/server layer, not only in the UI.

### Human-in-the-loop
When a portal requires CAPTCHA, MFA or manual review, the automation stops and requests human attention instead of attempting to bypass controls.

### Privacy
Real client/case fixtures are kept out of the public repository. This case study is intentionally sanitized.

## Current status
The product is near production readiness. Some live court-portal and external messaging integrations still require real authorized accounts/credentials for final end-to-end validation.

The commercial codebase remains private. Architecture and sanitized workflows can be discussed in interviews.
