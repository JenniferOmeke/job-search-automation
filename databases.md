# Notion databases

Three linked databases. The digest is filled by Workflow 1, the tracker by Workflow 2. A digest row is set to "Applied" when the tracker logs that application.

## Working Student Digest

| Property | Type | Notes |
|---|---|---|
| Job title | Title | Exact title from the posting |
| Company | Text | |
| Area | Select | Project / PMO, Programme / NGO, Operations, Customer Operations, Office / Admin, Grants / Fundraising, Research, Data (entry-level) |
| Fit | Select | ★★★ Strong · ★★ Good · ★ Stretch |
| Decision | Select | New · Apply · Applied · Skip |
| Date found | Date | |
| Posted at | Date-time | Exact first-publication time (Berlin) |
| Posted | Text | Weekday + time, "approx." if calculated |
| Location | Select | Berlin, Brandenburg, Remote (Germany) |
| German | Select | Not required · Plus (nice to have) |
| Hours / week | Text | Starts with role type, e.g. "Working student · 20 h" |
| Pay | Text | When stated |
| Why you fit | Text | 1–2 sentences linking requirements to the profile |
| Job link | URL | Live posting on employer site / ATS |
| Source | Select | LinkedIn, Indeed, Glassdoor, Arbeitnow, Bundesagentur für Arbeit, StepStone, Company site, English job board, NGO / research board, Other |
| Contact name / role | Text | |
| Contact type | Select | Hiring manager · Recruiter · HR · Team member |
| Contact LinkedIn | URL | Only verified profiles |
| Message angle | Text | |
| Connection message | Text | ≤ 200 characters |
| CV to use | Select | Tailored CV version per area |
| Deadline | Date | If stated |

## Working Student Tracker

| Property | Type | Notes |
|---|---|---|
| Role | Title | |
| Company | Text | |
| Area | Select | Same areas as the digest, plus Other |
| Status | Select | Applied · Acknowledged · In Review · Assessment / Task · Interview · Offer · Rejected · No Response · Withdrawn |
| Date applied | Date | |
| Days since applied | Number | Recalculated daily |
| Last update | Date | |
| Evidence | Text | Quoted line from the email behind the current status |
| Job link | URL | |
| Gmail link | URL | Link to the email thread |
| CV used | Text | Attachment name or "Uploaded via portal" |
| Channel | Select | Company portal, Email, LinkedIn, Indeed, StepStone, Other job board |
| Contact name / LinkedIn | Text / URL | Copied from the digest when available |
| Interview | Text | Date, time, format, interviewers |
| Next action date | Date | Follow-ups at 10–14 days |
| Notes | Text | Scam flags and other notes |

## Employer Watchlist

| Property | Type | Notes |
|---|---|---|
| Company | Title | |
| Sector | Select | Tech / Startup, Fintech / Finance, NGO / Foundation, Think tank / Research, International organisation, Corporate / Multinational, Climate / Energy, Mobility / Travel, Other |
| Cities | Multi-select | Berlin, Brandenburg, other German cities |
| Careers URL | URL | Only URLs actually opened |
| ATS | Select | Personio, Greenhouse, Lever, Ashby, Workday, SmartRecruiters, Teamtailor, Recruitee, Workable, Own site |
| Hires for | Multi-select | Working student, Internship |
| Last checked | Date | Oldest checked first each night |
| Status | Select | Checked · Not Checked · No Job AD |
