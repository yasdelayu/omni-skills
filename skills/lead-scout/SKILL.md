---
name: lead-scout
description: Builds a qualified B2B prospect list from public web sources — finds companies matching an ICP, verifies contact details on their own sites, enriches each lead with a personalization hook, and drafts (never sends) outreach. Use when asked to "find leads", "build a prospect list", "find companies that...", "найди лидов", "собери базу клиентов".
---

# Lead Scout

## Overview

Turns an ICP description into a table of verified prospects with personalized outreach drafts. Replaces the scrape → enrich → personalize pipeline with agent research over public pages. Drafts only — sending is always the user's action.

## When to Use

- "Find me 20 dental clinics in Berlin with outdated websites" — any niche + geo + qualifier search
- NOT for: scraping platforms behind login or against their ToS, buying contact lists, or mass-sending email

## Process

1. **Pin down the ICP.** Niche, geography, size signal, and the qualifier that makes them a fit (e.g. "no online booking", "hiring for marketing", "uses Shopify"). If the request lacks a qualifier, ask for one — "all restaurants in Moscow" is a directory, not a lead list.
2. **Find candidates** via web search and public directories (maps listings, industry associations, review sites, job boards). Collect ~2× the requested count — qualification will cut half.
3. **Qualify each candidate against the ICP** by visiting their site. Drop non-fits; record *why* the fits fit.
4. **Extract contacts from the company's own pages** (contact page, imprint/legal page, team page). Record the exact page URL where each contact was found. Never guess or pattern-generate emails (`info@` seen on the site is fine; `firstname.lastname@` invented is not). No contact found → mark "no public contact", keep the lead.
5. **Enrich with one personalization hook per lead**: a recent news item, review theme, site detail, or job posting — something specific enough that the outreach couldn't be sent to their competitor unchanged.
6. **Deliver two artifacts:**
   - `leads.csv` — name, url, geo, fit reason, contact, contact source URL, hook
   - `outreach-drafts.md` — one short draft per lead (≤120 words: hook → one-sentence value → soft CTA), in the user's language and voice
7. **Do not send anything.** No emails, no form submissions, no DMs.

## Verification

- [ ] Every contact has a source URL pointing to the company's own page
- [ ] No invented email addresses
- [ ] Every draft contains its lead's specific hook — swap-test two drafts to confirm they aren't interchangeable
- [ ] Fit reason recorded for every lead; requested count met or the shortfall explained
