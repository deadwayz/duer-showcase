# Duer

**Know what is due. Know what comes next.**

Duer is a personal and operational workspace for responsibilities with a deadline. It brings today’s work, recurring commitments, renewals, and optional financial context into a coherent planning experience.

![Duer — tasks and recurring work](assets/cover.svg)

[View the preview](#preview) · [Engineering notes](#engineering-notes) · [Project scope](#project-scope)

## Why it exists

A calendar shows dates, but recurring responsibilities also need ownership, completion, history, and a clear next occurrence. Duer connects those details while keeping the immediate question simple: **what needs to be done, and when?**

## Preview

![Recorded Duer interface preview showing due items, planning, and operational summaries](duer-demo.gif)

This recording shows an earlier interface revision. The current application prioritizes Today, This Week, and This Month; the recording is retained as a visual reference, not a promise that every screen is unchanged. The working application and source remain private.

## What the application does

- Prioritize overdue and upcoming items without losing later commitments.
- Add, edit, complete, reopen, and recreate responsibilities.
- Schedule recurring work, with supported completion undo and history.
- Browse calendar, timeline, all-item, and completed-work views.
- Organize workspaces and categories.
- Add renewal, budget, currency, and spending context when relevant.
- Sign in through Supabase and manage account and appearance preferences.

## Engineering notes

| Decision | Why it matters |
| --- | --- |
| Device-local calendar dates | Date-only responsibilities stay aligned with the user's day |
| Anchored recurrence | Repeated work can retain its intended schedule across uneven month lengths |
| Retry-safe completion operations | Repeating an uncertain request need not create a second recurrence |
| Schema capability detection | Existing records and older deployments can coexist with additive database changes |
| Shared domain utilities | Calendar, history, and planning views use consistent calculations |

**Application stack:** React · TypeScript · Vite · Tailwind CSS · React Router · Supabase/Postgres · Cloudflare static hosting

The current query bar hands text into item search, and natural-language entry uses parsing logic. This showcase does not claim a generative AI assistant, external system-health monitoring, or autonomous decision-making.

## Project scope

Duer is an evolving private application. Recurrence and ownership behavior depend on the configured database schema. The public repository contains a portfolio overview and an earlier recording; it does not contain application source, a login endpoint, or setup credentials.

## More projects

[HYLE — IT asset management](https://github.com/deadwayz/hyle-showcase) · [Recall — reusable knowledge](https://github.com/deadwayz/recall-showcase) · [Creator's GitHub profile](https://github.com/deadwayz)

## Usage and permissions

See [NOTICE.md](NOTICE.md). Showcase content and application code are separate materials; neither is given a new open-source license by this repository.
