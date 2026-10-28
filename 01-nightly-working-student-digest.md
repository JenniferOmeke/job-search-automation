# Workflow 1: Nightly working-student digest

**Schedule:** every day at 22:40 (Europe/Berlin)
**Connections:** Notion, Gmail (read-only), Indeed, Google Drive, Google Calendar, web search
**Output:** new rows in the Notion Working Student Digest, watchlist updates, one push notification

This is the instruction set the agent runs each night, with personal details and database IDs removed.

---

## Goal

Fill the Notion digest with the top 15–20 working-student roles that were **first posted in the last 24 hours**, English-only and realistic for the candidate. Each row has a direct job link, the exact posting time, the right contact on LinkedIn and a ready-to-send message.

"Last 24 hours" = since 22:40 the previous day.

## Candidate profile

The agent receives a short, factual candidate profile (current studies, roles with dates and metrics, tools, languages). It may only use facts from this profile and must never invent others.

*(Kept private in this public version.)*

## Role types

Working student (Werkstudent), internships (including 6–24-month internships), student assistant and part-time corporate roles for students.

## Location

Berlin focus. Brandenburg (Potsdam, Wildau, Schönefeld/BER) is fine. Remote-in-Germany only if open to Berlin-based students.

## Areas, in priority order

Project / PMO, programme / development economics, policy, sustainability, teaching assistant, research assistant / NGO, operations, customer operations (office-based), office / admin, grants / fundraising, research, entry-level data (max ~1 in 5 rows).

## Hard rules (apply to every row)

1. **Fresh = first posted within 24 hours.** Exclude anything marked "Reposted", "Erneut veröffentlicht" or "refreshed", anything already seen, and any role whose company + title was already public earlier on another board. If the posting date/time can't be verified, skip it.
   Date signals used: LinkedIn "x hours ago" (not "Reposted"), Indeed "Just posted", Glassdoor 24h filter, Arbeitnow `created_at`, pegel.berlin `postedAt`, Lever `createdAt`, Ashby `publishedAt`, Greenhouse `first_published`, Personio feed `createdAt`, SmartRecruiters `releasedDate`, Recruitee `published_at`, Workday "Posted Today".
2. **Posted at:** record the exact first-publication time. If the source only says "x hours ago", calculate it and mark it "approx."
3. **English only.** Open each posting and verify. Skip any role requiring German at any level. "German is a plus" is allowed.
4. **Student-level roles only.** Skip anything senior or asking for experience beyond a student role. When in doubt, leave it out.
5. **Professional roles only:** offices of companies, startups, NGOs, foundations, research institutes, international organisations. No mini-jobs (€538 / geringfügig), hospitality, retail, warehouse, delivery, call-centre shift work or commission-only sales.
6. **Legitimate only:** real employers and reputable boards. Skip pay-to-apply, MLM, vague "data entry" ads, anonymous ads, or anything asking for ID/bank details.
7. **Direct links:** the live posting on the employer's career page or ATS, opened to confirm it is live; otherwise the board's direct posting URL (never a search-results page).
8. **Never fabricate** job links, times, names, LinkedIn URLs or facts.
9. **Deduplicate** against the digest and the tracker (query them first).
10. **Volume:** up to 15–20 roles, ranked by fit. The 24-hour rule comes first: if fewer qualify, add fewer and say so.

## Where to search (every night)

### 1. Job sites
- LinkedIn Jobs via web search (e.g. "Werkstudent" Berlin English), plus LinkedIn job-alert emails from the last 24 h (read-only), then open the employer's own posting
- Indeed (newest first, Berlin)
- Glassdoor (24 h filter), Arbeitnow API, Bundesagentur für Arbeit (English ads only), StepStone & XING, pegel.berlin API (`german=not_needed`, `postedWithin=1d`)
- English job boards (englishjobs.de, berlinstartupjobs.com, jobs.thelocal.de and similar)
- Student boards (studentjob.de, jobteaser.com)
- NGO / international boards (Impactpool, Devex, ReliefWeb, UN Careers)

Blocked sites are skipped. No proxies, caches or mirrors.

### 2. Employer career pages → Notion "Employer Watchlist"
- Check at least 40 watchlist employers per night, oldest "Last checked" first.
- Prefer the ATS's public job feed/API because it shows publication dates (Greenhouse, Lever, Ashby, Personio, SmartRecruiters, Recruitee, Workday).
- For each employer checked: fill or correct the careers URL and ATS (only a URL actually opened), set "Last checked", count roles added, and note if they mostly require German or rarely hire students.
- **Grow the list:** add 5–10 new English-working employers in Germany each night, with verified careers URLs and no duplicates.

## Contact for every row: get the right person

Priority:
1. Hiring manager (the person the role reports to, or the team lead in that office)
2. Recruiter / early-careers recruiter for that role or office
3. HR / People
4. Someone in the same team

Method: names in the posting/ATS first, then targeted web searches. Use only a LinkedIn profile URL that appears in results, and only when the snippet shows the person **currently** works there in a matching function. If nobody is verifiable, write "No verified contact".

- **Message angle:** 1–2 lines on what to say to this person and which proof point fits.
- **Connection message:** ready to send, max 200 characters: greet by first name, name the role, one concrete proof point, a light ask. No emojis; never claims an application was sent unless it was.

## Fields written per row

Job title, company, area, fit (★★★ Strong / ★★ Good / ★ Stretch), decision = "New", date found, posted at (date-time), posted (weekday + time), location, German (Not required / Plus), why you fit, job link, source, contact name / role / type / LinkedIn, message angle, connection message, CV to use (tailored version per area), deadline, hours per week (starting with the role type, e.g. "Working student · 20 h" or "Internship · 6 months") and pay when stated.

## Finish

One push notification:
- n new roles in the last 24 h (top 3: title – company – posted time)
- Watchlist: x employers checked, y added
- One line if any source failed

**Never** applies to jobs, sends emails or LinkedIn messages, or modifies Gmail.
