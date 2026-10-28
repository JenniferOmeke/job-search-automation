# Workflow 2: Daily application tracker

**Schedule:** every day at 14:41 (Europe/Berlin), so the tracker is current by 15:00
**Connections:** Gmail, Notion
**Output:** new and updated rows in the Notion Working Student Tracker, Gmail drafts for follow-ups, one push notification

This is the instruction set the agent runs each afternoon, with personal details and database IDs removed.

---

## Notion targets

- **Working Student Tracker:** every working-student, student-assistant and internship application
- **Working Student Digest:** used to link contacts and mark rows as Applied

The agent fetches the database schema first for exact property names, and never creates duplicates: company + role is the match key, and one application confirmed by both a job board and the employer is one row.

## Steps

### 1. Search Gmail (last 2 days; catches up further if a run was missed)
In English and German:
- Confirmations: "thank you for applying", "application received", "Ihre/deine Bewerbung", "Eingangsbestätigung", "Kopie deiner Bewerbung"
- ATS senders: Workday, Personio, Workable, JOIN, onlyfy, softgarden, SmartRecruiters, Greenhouse, Lever, Ashby, Teamtailor, Recruitee, d.vinci, SuccessFactors, Indeed Apply, XING, StepStone, LinkedIn
- Sent mail with CV attachments or "Bewerbung" / "Application" in the subject

Ignores job alerts, reminders, newsletters and data-deletion notices.

### 2. Log new applications
New row in the tracker with: role, company, area, status ("Applied", or "Acknowledged" if a confirmation arrived), date applied, days since applied, last update, evidence (quoted email line), job link, link to the Gmail thread, CV used and channel.
If the role came from the digest, the contact details are copied over and that digest row is set to "Applied".

### 3. Update statuses, only with evidence
Each change quotes the line that caused it and sets "Last update":
- In Review
- Assessment / Task
- Interview (date, time, format and interviewers recorded)
- Offer
- Rejected ("unfortunately", "leider", "other candidates", "nicht berücksichtigen")
- Withdrawn

### 4. Follow-up logic for every open application
- Recalculate days since applied
- **10–14 days, no reply** → set a specific next action (who to message: the LinkedIn contact or the email in the thread) and a date
- **21+ days, no reply** → status "No Response"

### 5. Interviews
Scheduled interviews go to the top of the summary, with next action "Prepare: research the team, 3 STAR stories matching the ad".

### 6. Follow-up emails
Written **only as Gmail drafts**, in the language of the application, and only when a reply address exists.

### 7. Scam check
Flags likely recruitment scams in Notes: contract without interview, requests for ID or bank details, off-platform registration.

## Finish

One push notification with 3 lines:
1. New applications today
2. Status changes, especially interviews and offers
3. The most urgent follow-up and who to contact

**Never** sends anything, applies labels or applies to jobs.
