# MESA-AI - Restaurant AI Receptionist SaaS

## Problem
Restaurants receive reservations, menu questions, order-related messages and customer requests across multiple channels. Staff can lose time switching between conversations and operational tools.

## Solution
MESA-AI is a multi-tenant SaaS platform that centralizes AI-assisted restaurant communication and operational workflows.

## What I worked on
- Multi-tenant restaurant and branch architecture.
- Reservation and table workflows.
- Digital menu and product management.
- CRM and conversation flows.
- WhatsApp and voice-oriented automation design.
- Role-based access and branch isolation.
- Backend workflows with Supabase/PostgreSQL.
- Validation, testing and deployment workflows.

## Stack
Next.js, TypeScript, React, Supabase, PostgreSQL, Zod, Vitest, Vercel, AI agent workflows and WhatsApp integrations.

## Engineering decisions
A key design principle is to keep business-critical rules outside the language model whenever possible. AI interprets intent and language; deterministic code validates state, permissions, availability and workflow transitions.

## Status
Commercial/private codebase. Architecture and sanitized demos can be discussed during interviews.
