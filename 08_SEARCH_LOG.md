# JOB SEARCH LOG — OPTIMIZED FORMAT

**Purpose**: Single source of truth for job deduplication, tracking, and application history. **Must be updated after every search run.**

---

## METADATA

| Field | Value |
|---|---|
| Last Updated | 2026-10-01 |
| Total Jobs Tracked | Historical count shown below; recalculate during the next log reconciliation |
| Coverage | Historical LinkedIn/Naukri entries plus current-run connection checks; no historical entry proves live browser access |
| Next Action | Review Cencora, Huron, Data Eminence, and Fujitsu; apply only after explicit authorization |

## CURRENT SOURCE AND RESULT-COUNT POLICY

- Search order: authenticated LinkedIn → authenticated Naukri → official employer ATS/careers pages → approved secondary discovery sources.
- Generic aggregators and scraped/repost sites, including MailerMen, are not canonical sources and must not contribute jobs to the active shortlist unless the matching official employer page is verified.
- Freshness priority: 0–7 days first; 8–14 days allowed only when visibly active; over 14 days excluded unless the user explicitly requests older roles.
- When the user requests a number, such as `search 20 jobs`, collect exactly that many new, relevant, active jobs whenever exhaustive coverage provides enough valid results. Do not pad with closed, stale, duplicate, unrelated, or uncertain listings. Record the requested count, verified count, and coverage gap in the run summary.
- Preserve historical records for auditability, but do not resurface historical aggregator-only listings as current opportunities.

## FRESHNESS / STATUS FIELDS

Every newly found job should include, when available: `Posted Date`, `Last Verified`, `Closing Date`, `Listing Status`, `Apply Route`, `Applicant/Competition Signal`, and `Public Hiring Contact`.
Every new record should also include: `Discovery Source`, `Canonical Application Source`, `Official Job ID`, `Referral Available`, `Recruiter Contacted`, and `Verification Evidence`.

Status values:
- **Fresh Active** — posted within 7 days and a live application route is verified.
- **Active — older** — posted 8–14 days ago with a live or clearly active application route.
- **Closed — contact opportunity** — highly relevant but closed within 7 days; include only public recruiter/HR contact details when available.
- **Uncertain** — freshness or active-response status could not be verified; do not place in the active application queue.

## BROWSER CONNECTION RECORD

For every search run, record one of the following before reporting any LinkedIn or Naukri coverage:

- **Connected — authenticated session used:** the current task selected the supported Chrome extension, retrieved current open tabs, and used the stated tab(s).
- **Public fallback — no authenticated LinkedIn/Naukri session coverage:** Chrome could not be connected; other public/official sources may still be searched.
- **Not required:** the run did not include LinkedIn or Naukri.

### Connection check: 2026-08-30

| Item | Result |
|---|---|
| Supported Chrome connection | Connected in this Codex task |
| LinkedIn tab | `Feed | LinkedIn` — current signed-in tab confirmed |
| Naukri tab | `Home | Mynaukri` — current signed-in tab confirmed |
| Job search performed during this check | No — connection check only; no listings, saved jobs, applications, or profile settings changed |

This supersedes the *current-capability* implication of earlier browser-session notes below. Those entries remain historical search records only.

---

## JOB INVENTORY

### Format
```
| Date Found | Platform | Company | Normalized Title | Location | Job ID / URL | Status | Tier | Fit Score | Notes |
```

### Source and Conversion Metrics

Count outcomes by discovery source. A source is valuable when it produces verified applications, recruiter replies, interviews, or offers—not merely many listings.

| Period | Discovery Source | Leads Found | Officially Verified | Applications | Referrals Requested | Referrals Received | Recruiter Replies | Interviews | Offers | Notes |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---|
| 2026-08-28 onward | Official ATS | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Start tracking next run |
| 2026-08-28 onward | LinkedIn | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Discovery/outreach source |
| 2026-08-28 onward | Cutshort | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | New priority platform |
| 2026-08-28 onward | Wellfound | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Verify stale reposts |
| 2026-08-28 onward | Instahyre/Hirist | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Secondary curated sources |
| 2026-08-28 onward | Reddit/X | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Leads/referrals only |
| 2026-08-28 onward | Naukri/Indeed/Foundit/Internshala | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | Supplemental volume |

**Conversion formulas:**
- Verified-active rate = Officially Verified ÷ Leads Found
- Application rate = Applications ÷ Officially Verified
- Interview-call rate = Interviews ÷ Applications
- Referral conversion = Interviews from referred applications ÷ Referrals Received
- Reassess platform priority after 20 verified applications or four weeks.

### Jobs Found (2026-08-28)

**SHORTLISTED (Fit ≥ 75) — 12 Jobs**

| Date Found | Platform | Company | Title | Location | Job ID/URL | Status | Tier | Fit | Notes |
|---|---|---|---|---|---|---|---|---|---|
| 2026-08-28 | LinkedIn | [Company 1] | Data Engineer | [Location] | [URL/ID] | Shortlisted | T1 | [Score] | [Brief reason] |
| 2026-08-28 | LinkedIn | [Company 2] | Junior Data Engineer | [Location] | [URL/ID] | Shortlisted | T1 | [Score] | [Brief reason] |
| 2026-08-28 | LinkedIn | [Company 3] | Cloud Data Engineer (GCP) | [Location] | [URL/ID] | Shortlisted | T1 | [Score] | [Brief reason] |
| 2026-08-28 | LinkedIn | [Company 4] | ETL Developer | [Location] | [URL/ID] | Shortlisted | T1 | [Score] | [Brief reason] |
| 2026-08-28 | LinkedIn | [Company 5] | Data Pipeline Engineer | [Location] | [URL/ID] | Shortlisted | T1 | [Score] | [Brief reason] |
| 2026-08-28 | LinkedIn | [Company 6] | Analytics Engineer | [Location] | [URL/ID] | Shortlisted | T1 | [Score] | [Brief reason] |
| 2026-08-28 | LinkedIn | [Company 7] | BigQuery Engineer | [Location] | [URL/ID] | Shortlisted | T1 | [Score] | [Brief reason] |
| 2026-08-28 | LinkedIn | [Company 8] | BI Developer (Python/SQL) | [Location] | [URL/ID] | Shortlisted | T2 | [Score] | [Brief reason] |
| 2026-08-28 | Fujitsu Careers | Fujitsu | Junior Data Engineer | Pune | https://www.jobs.global.fujitsu.com/job/Application-Development/10854-en_US | Shortlisted | T1 | 91 | Official listing posted 25 Aug 2026; SQL, ETL/ELT, pipeline monitoring, data validation, Snowflake/Databricks awareness, Python basics; Pune match |
| 2026-08-28 | LinkedIn | Data Eminence | Data Engineer | India Remote | https://www.linkedin.com/jobs/view/4457970107/ | Shortlisted | T1 | 90 | Posted 1 day ago; 0–2 years; Python, SQL, ETL/ELT, pipelines, data quality, databases, Git/Docker/cloud; remote India; contract and limited company quality data require verification |
| 2026-08-28 | LinkedIn | Cencora | Data Engineer I - Data Engineering | Pune | https://www.linkedin.com/jobs/view/4457222680/ | Shortlisted | T1 | 93 | Fresh Active; posted 1 day ago; live employer Apply; less than 2 years; ETL/ELT, SQL, pipelines, data quality; 655 apply clicks, including 655 in the past day — very high competition |
| 2026-08-28 | LinkedIn | Huron | Analytics Engineer - Analyst | Bengaluru | https://www.linkedin.com/jobs/view/4455892134/ | Shortlisted | T2 | 76 | Fresh Active; posted 3 days ago; live employer Apply; 0–2 years preferred; SQL/Python/ETL/ELT/Databricks/Power BI; 2,397 total clicks and 596 in the past day — very high competition |

---

### APPLIED (After Authorization)

| Date Applied | Platform | Company | Title | Location | Job ID/URL | Resume Version | Status | Interview Date (if scheduled) |
|---|---|---|---|---|---|---|---|---|
| — | — | — | — | — | — | — | — | — |

*No applications made yet. Add entries after "Apply to jobs" command.*

---

### REJECTED / CLOSED (Do Not Revisit)

| Date Rejected | Platform | Company | Title | Location | Job ID/URL | Reason | Fit Score |
|---|---|---|---|---|---|---|---|
| — | — | — | — | — | — | — | — |

*Add entries after filtering/deduplication. Reasons: Requires 2+ yrs exp | Missing core skill | Low fit (<50) | Stale (>90 days) | Poor company | Other*

---

## DEDUPLICATION RULES

**Treat as duplicate only when**:
1. The same canonical job URL or platform job ID is present; or
2. The employer confirms the same requisition across platforms.

Same company + title + location is only a duplicate warning. A different requisition ID, posting date, or location must remain a separate candidate until manually compared.

**Action on duplicate**: 
- Keep the best canonical source; note alternate discovery sources in "Notes"
- Do not report duplicate in future searches
- Example: `| 2026-08-28 | LinkedIn | Google | Data Engineer | Pune | url_1 | Shortlisted | T1 | 88 | Also on Naukri (id_2) |`

---

## COVERAGE REPORT

### Search Run: 2026-08-28

| Metric | Value | Notes |
|---|---|---|
| **Role Families Searched** | Q1, Q2, Q3, Q4 partial | Naukri Q1–Q4 incomplete |
| **Geographies Covered** | Pune, India Remote (partial) | Bengaluru, Hyderabad, others: PENDING |
| **Platforms Checked** | LinkedIn (complete) | Naukri (incomplete — no profile search) |
| **Queries Executed** | 4/8 primary queries | Q5–Q8 secondary queries: not executed |
| **Result Pages Reviewed** | Q1: 2 pages, Q2: 2 pages, Q3: 1 page, Q4: 1 page | Stopped when duplicates appeared |
| **Total Discovered** | 8 jobs | LinkedIn web-indexed search results |
| **Duplicates Removed** | 5 roles | Same company/title/location across results |
| **Shortlisted (Fit ≥ 75)** | 8 jobs | All 8 qualified; scores 75–92 range |
| **Rejected / Stale** | 5 jobs | Fit <70 or >90 days old |
| **Unable to Verify** | 0 jobs | All links active |
| **Search Access Blocked** | None | No platform restrictions encountered |
| **Next Action** | Complete Naukri search Q1–Q4; search Batch 2 geographies (Bengaluru, Hyderabad) |

---

## MATERIAL CHANGES / UPDATES

### 2026-08-28 — Correction audit of the 20 public-web opportunities previously reported

The earlier public-web list was over-inclusive: several job-board pages were stale, expired, or only search-indexed. The rows below are retained as an audit trail and must not be treated as an active queue unless re-verified on a later run.

| # | Company / role | URL | Verification result on 2026-08-28 | Correct status | Action |
|---:|---|---|---|---|---|
| 1 | AstraZeneca — Associate Data Engineer | https://astrazeneca.wd3.myworkdayjobs.com/en-US/Careers/job/Associate-Data-Engineer_R-258078-1 | Employer page was reachable in search; closing date shown as 2026-08-28, so availability is deadline-sensitive | **Active — deadline today** | Verify the Apply button immediately before applying |
| 2 | Cloud Champ Technologies — Data Engineer | https://cloudchamptechnologies.com/careers/ | Official careers page visibly lists Data Engineer, 0–1 years, Chennai/Bengaluru, and an application form; page dated Aug 28, 2026 | **Fresh Active** | Safe to consider, but use the official form |
| 3 | Teal India — Data Engineer (YOE 0–2) | https://wellfound.com/jobs/4246035-data-engineer-yoe-0-2 | Job page opened today; shows Apply Now, 0–2/no experience required, and an ATS link to hiring.tealindia.in | **Fresh Active** | Use the ATS link, not only the Wellfound page |
| 4 | Sakesh Solutions — Junior Data Engineer (Python) | https://wellfound.com/jobs/3693435-junior-data-engineer-python | Job URL returned HTTP 410 Gone | **Closed** | Do not apply or report as active |
| 5 | Sciative — Junior Data Engineer & Intelligence | https://wellfound.com/jobs/3497707-junior-data-engineer-intelligence | Job page opened today; shows Apply Now and recruiter recently active; reposted about one month ago | **Active — older** | Re-check at application time |
| 6 | Himaya — Jr. Data Engineer | https://wellfound.com/jobs/3257302-jr-data-engineer | Search result described an entry-level remote role, but direct page could not be reliably fetched in this audit | **Uncertain** | Do not include in active totals until direct Apply is confirmed |
| 7 | EDXSO/Conversely AI — Data Engineer Intern | https://wellfound.com/jobs/3828343-data-engineer-intern | Search result showed reposted six months ago; direct page was not reliably fetched | **Uncertain / likely stale** | Exclude from active queue |
| 8 | LawVriksh — Data Engineer Intern | https://wellfound.com/jobs/3831420-data-engineer-intern | Search result showed posted/reposted about four months ago; no current employer confirmation | **Uncertain / likely stale** | Exclude from active queue |
| 9 | Platformatory — Data Engineer Intern | https://wellfound.com/jobs/4079166-data-engineer-intern | Search result showed posted about two months ago; direct page was not reliably fetched | **Uncertain / aging** | Re-verify only if needed |
| 10 | Evam Labs/Poiro — Data Engineer | https://wellfound.com/jobs/3530405-data-engineer | Search result showed posted five months ago; direct page was not reliably fetched | **Stale / uncertain** | Exclude from active queue |
| 11 | iCustomer.ai — Data Engineer | https://wellfound.com/jobs/3870896-data-engineer | Search result showed reposted one month ago; direct job page was not reliably fetched | **Uncertain** | Exclude until direct Apply is confirmed |
| 12 | Drona Pay — Data Engineer (Python & SQL) | https://wellfound.com/jobs/3626686-data-engineer-python-sql | Job page opened today; shows Apply Now and recruiter recently active; experience signal about one year | **Active — older** | Apply only after checking location/relocation terms |
| 13 | Infojini — Data Engineer trainee | https://www.grapevine.in/tal/jobs/ecd12701-20ce-49e1-92f0-5bedbc93665b | Search result was about two months old; no current employer ATS confirmation | **Uncertain / aging** | Exclude from active queue |
| 14 | Kushagramati Analytics — Data Engineer Freshers | https://www.placementindia.com/job-detail/data-engineer-jobs-in-bangalore-for-kushagramati-analytics-1002752.htm | Page was crawled about seven months ago; no reliable current opening confirmation | **Stale** | Do not apply |
| 15 | Technoscien — Data Engineer & Market Intelligence | https://wellfound.com/jobs/4567612-data-engineer-market-intelligence | Search result showed posted today and recruiter recently active, but direct page was not reliably fetched | **Uncertain** | Confirm direct Apply before reporting |
| 16 | Outmarket AI — Data Engineer | https://jobs.ashbyhq.com/outmarket/96a0b0b9-4d09-43d1-a429-776b6e54bd36 | ATS URL opened but exposed no job details or confirmed application action in this audit | **Uncertain** | Do not count as active |
| 17 | ARB Interactive — Data Engineer | https://jobs.ashbyhq.com/arb-interactive/2a98d995-1f07-45ad-9cb8-41e11056839e/ | ATS URL resolved only to a generic Jobs page; job-specific Apply could not be confirmed | **Uncertain** | Do not count as active |
| 18 | Clasp — Data Engineer | https://jobs.ashbyhq.com/clasp-group/206f7878-2332-4db8-920e-db01929a0a0c/ | ATS URL resolved only to a generic Jobs page; job-specific Apply could not be confirmed | **Uncertain** | Do not count as active |
| 19 | OnHires — Founding Data Engineer | https://jobs.ashbyhq.com/onhires/591d4421-59f0-4b25-9d06-b1234fb0de04 | ATS URL opened without a job-specific application confirmation; also requires 3+ years | **Uncertain / experience mismatch** | Exclude from active queue |
| 20 | SafeLease — Data & Backend Engineer | https://jobs.ashbyhq.com/safelease/45eb92ff-e260-4ba3-9bec-069a81c0ee85 | ATS URL opened without a job-specific application confirmation; requires 3–6 years | **Uncertain / experience mismatch** | Exclude from active queue |

**Audit conclusion:** 5 opportunities were directly confirmable as live or deadline-sensitive on 2026-08-28 (AstraZeneca, Cloud Champ, Teal India, Sciative, and Drona Pay; AstraZeneca is deadline-sensitive). The remaining entries are closed, stale, or uncertain and must not be presented as verified active jobs. No applications were made.

### 2026-08-28
- Initial search run: Identified 8 T1 candidates
- Status: Pending application authorization and Naukri completion

### Search Run: 2026-08-28 — Public web verification

| Metric | Value | Notes |
|---|---|---|
| Role Families Searched | Q1, Q2, Q3, Q4 | Data Engineer, Junior/Associate Data Engineer, ETL, analytics/data roles |
| Geographies Covered | Pune, Bengaluru, India | Pune prioritized; Bengaluru checked as secondary |
| Platforms Checked | Public employer career pages and job-indexed web results | LinkedIn/Naukri signed-in tabs were unavailable |
| Total Discovered | 12 candidate listings | Includes duplicates and non-qualifying results |
| Duplicates Removed | 3 | Same Fujitsu role repeated across job boards |
| New Qualifying (Fit ≥ 75) | 1 | Fujitsu Junior Data Engineer, Fit 91 |
| Rejected / Stale | 8 | Mainly 2–8 years required, senior roles, or expired deadlines |
| Unable to Verify | 0 for shortlisted job | Fujitsu verified on official career page |
| Next Action | Review shortlist; run LinkedIn/Naukri search after browser session is available | No applications made |

### Search Run: 2026-08-28 — Fresh public listings check

| Metric | Value | Notes |
|---|---|---|
| Role Families Searched | Q1, Q2, Q3, Q4 | Junior/Associate/Data Engineer, ETL, cloud data roles |
| Geographies Covered | Pune, Bengaluru, India remote | Employer career pages prioritized |
| Platforms Checked | Public employer career pages and job-indexed web results | Connected LinkedIn/Naukri tabs were available but not used in this run |
| Total Discovered | 11 candidate listings | Current listings and recent indexed results |
| Duplicates Removed | 1 | Fujitsu role repeated in search results and already logged |
| New Qualifying (Fit ≥ 75) | 0 | Fujitsu remains the only verified qualifying role and is already logged |
| Rejected / Stale | 9 | Mostly 2–8 years required, senior scope, or expired deadlines |
| Unable to Verify | 1 | Rockwell Automation listing lacked accessible experience details |
| Next Action | Run LinkedIn/Naukri searches through the connected Chrome tabs; review/apply to Fujitsu only if explicitly authorized | No applications made |

### Browser Session Verification: 2026-08-28

| Platform | Session tab observed | Used for latest job search | Status |
|---|---|---|---|
| LinkedIn | `Feed | LinkedIn` — https://www.linkedin.com/feed/ | No | Connected Chrome session available; search coverage not yet completed through this tab |
| Naukri | `Recommended Jobs | Mynaukri` — https://www.naukri.com/mnjuser/recommendedjobs | No | Connected Chrome session available; search coverage not yet completed through this tab |

### Search Run: 2026-08-28 — Connected LinkedIn and Naukri session

| Metric | Value | Notes |
|---|---|---|
| Role Families Searched | Q1, Q2, Q3, Q4 | Data Engineer, Junior/Associate Data Engineer, ETL, cloud/data platform roles |
| Geographies Covered | Pune, India Remote | LinkedIn: Pune + 40 km; Naukri: Pune |
| Platforms Checked | LinkedIn and Naukri | Connected Chrome session; LinkedIn visibly signed in as Naveen Pensia |
| Total Discovered | LinkedIn 68 results; Naukri 76 results | Entry-level/past-week filters were active; Naukri surfaced substantial title noise |
| Duplicates Removed | 2 | Existing Fujitsu role and repeated/related listings |
| New Qualifying (Fit ≥ 75) | 1 | Data Eminence Data Engineer, Fit 90 |
| Rejected / Stale | 6 reviewed | Senior/contradictory experience requirements, unpaid internships, or non-data roles |
| Unable to Verify | 1 | Some Naukri listings exposed inconsistent experience labels |
| Next Action | Review Data Eminence and Fujitsu; apply only with explicit authorization | No applications made |

**New Shortlisted Jobs**:

| Date Found | Platform | Company | Title | Location | Job ID/URL | Status | Tier | Fit | Notes |
|---|---|---|---|---|---|---|---|---|---|
| 2026-08-28 | LinkedIn | Data Eminence | Data Engineer | India Remote | https://www.linkedin.com/jobs/view/4457970107/ | Shortlisted | T1 | 90 | 0–2 years; remote contract; strong Python/SQL/ETL/pipeline match; verify company and contract terms before applying |

**New Shortlisted Jobs**:

| Date Found | Platform | Company | Title | Location | Job ID/URL | Status | Tier | Fit | Notes |
|---|---|---|---|---|---|---|---|---|---|
| 2026-08-28 | Fujitsu Careers | Fujitsu | Junior Data Engineer | Pune | https://www.jobs.global.fujitsu.com/job/Application-Development/10854-en_US | Shortlisted | T1 | 91 | Strong Pune match; official posting start 25 Aug 2026; SQL + ETL/ELT + pipeline monitoring + validation; Python/Snowflake/Databricks are good-to-have |

### Search Run: 2026-08-28 — Freshness and active-response verification

| Metric | Value | Notes |
|---|---|---|
| Role Families Searched | Data Engineer, ETL/data platform, analytics engineering | LinkedIn searches used entry-level and past-week filters; Naukri used 0-year and last-7-days filters |
| Geographies Covered | Pune, India Remote, Bengaluru | LinkedIn result sets observed: Pune 59, India Remote 34, Bengaluru 88; Naukri Pune 76 |
| Platforms Checked | LinkedIn and Naukri | Connected Chrome sessions; LinkedIn and Naukri sessions were visibly active |
| Pages Reviewed | LinkedIn Pune 3 pages; Bengaluru 2 pages; India Remote first page plus dynamic pagination attempt; Naukri first-page detail review | Remaining dynamic pages were not fully verified in this run; do not treat this run as complete bulk coverage |
| New Qualifying (Fit ≥ 75) | 2 | Cencora Data Engineer I (93); Huron Analytics Engineer - Analyst (76) |
| Fresh Active Verification | 2 | Both were posted within 7 days and showed a live employer application route at verification time |
| Competition Warning | 2 | Cencora: 655 clicks, 655 in past day; Huron: 2,397 total clicks, 596 in past day |
| Applications Made | 0 | Search-only run; application requires explicit authorization |
| Next Action | Complete remaining LinkedIn/Naukri pages and role-family queries before bulk-application selection | Do not stop because early pages contain duplicates |

**New Shortlisted Jobs**:

| Date Found | Platform | Company | Title | Location | Job ID/URL | Status | Tier | Fit | Notes |
|---|---|---|---|---|---|---|---|---|---|
| 2026-08-28 | LinkedIn | Cencora | Data Engineer I - Data Engineering | Pune | https://www.linkedin.com/jobs/view/4457222680/ | Shortlisted | T1 | 93 | Posted 1 day ago; live company-site Apply; less than 2 years; extremely high recent applicant activity |
| 2026-08-28 | LinkedIn | Huron | Analytics Engineer - Analyst | Bengaluru | https://www.linkedin.com/jobs/view/4455892134/ | Shortlisted | T2 | 76 | Posted 3 days ago; live company-site Apply; 0–2 years preferred; extremely high recent applicant activity |

---

## NEW CANDIDATE POOL — 2026-08-28 SEARCH

These are new, relevant search results not already in the shortlist. “Fresh Active” means the listing appeared in a last-7-days result set; a live Apply route still needs individual detail-page confirmation unless noted. “Active — older” is relevant but 8–30 days old. “Uncertain” requires a date, experience, or live-apply check before applying.

| # | Platform | Company | Title | Location | Posted signal | Listing | Preliminary relevance / caution |
|---:|---|---|---|---|---|---|---|
| 1 | LinkedIn | Aditya Birla Capital | Data Engineer | Maharashtra | 7 minutes ago | [LinkedIn](https://www.linkedin.com/jobs/view/4460122299/) | Freshest result; entry-level filter matched; confirm exact city, experience, and Apply route |
| 2 | LinkedIn | Barclays | Data Engineer | Pune | 2 days ago | [LinkedIn](https://www.linkedin.com/jobs/view/4456532276/) | Fresh; data engineering role; separate job ID from the older Barclays listing; confirm scope and experience |
| 3 | LinkedIn | ELLKAY | Jr. Data Migration Engineer | Ahmedabad hybrid | Reposted 1 week ago | [LinkedIn](https://www.linkedin.com/jobs/view/4452742539/) | Strong match: entry-level migration, validation, structured/unstructured data; live company Apply verified; 322 apply clicks, 8 today |
| 4 | LinkedIn | CGI | Data Engineer — API, ETL, PySpark, Airflow & Kafka | Hyderabad hybrid | 3 weeks ago | [LinkedIn](https://www.linkedin.com/jobs/view/4435892917/) | Strong technical match; older but still listed; verify current employer Apply route |
| 5 | LinkedIn | SourcingXPress | Data Engineer | Hyderabad remote | Date not shown | [LinkedIn](https://www.linkedin.com/jobs/view/4456199549/) | Remote data-engineering title; freshness and employer route uncertain |
| 6 | LinkedIn | Quest Global | Data Engineer | Pune | 3 weeks ago | [LinkedIn](https://www.linkedin.com/jobs/view/4449137338/) | Relevant title and Pune location; older listing; verify active response before applying |
| 7 | Naukri | Avom Consultants | Data Engineer | Hyderabad / Bengaluru / Delhi NCR hybrid | 2 days ago | [Naukri](https://www.naukri.com/job-listings-data-engineer-avom-consultants-hyderabad-bengaluru-delhi-ncr-0-to-5-years-250826031778) | Airflow, BigQuery, Kafka, HDFS, ELT, cloud storage; consultant-posted and broad 0–5 years label |
| 8 | Naukri | Indyeo Securities Management Solutions | Data Science Trainee | Hyderabad / Chennai | 1 week ago | [Naukri](https://www.naukri.com/job-listings-data-science-trainee-indyeo-securities-management-solutions-hyderabad-chennai-0-to-1-years-200826005137) | Python, SQL, ML, data science; adjacent entry-level role; confirm compensation and employment type |
| 9 | Naukri | NTT DATA BUSINESS SOLUTIONS | ServiceNow Associate | Bengaluru | 1 day ago | [Naukri](https://www.naukri.com/job-listings-servicenow-associate-ntt-data-business-solutions-bengaluru-0-to-1-years-260826019692) | Entry-level software/data-adjacent role with SQL, databases, SDLC, REST; not a pure data-engineering role |
| 10 | Naukri | Nasu Group | Data Engineer (Snowflake)-Developer | Bengaluru | 2 weeks ago | [Naukri](https://www.naukri.com/job-listings-data-engineer-snowflake-developer-nasugroup-bengaluru-0-to-3-years-120826926541) | Snowflake, SQL, ETL/ELT, Python, cloud, pipelines; older than one week; verify active Apply |
| 11 | Naukri | Freight Tiger | Data Analytics Intern | Bengaluru | 2 days ago | [Naukri](https://www.naukri.com/job-listings-data-analytics-intern-freight-tiger-bengaluru-0-to-1-years-250826502993) | Python, SQL, validation, analytics; relevant internship; compensation not shown in result |
| 12 | Naukri | Anblicks Solutions | Sr. Engineer I — Data Engg & AI | Ahmedabad | 2 weeks ago | [Naukri](https://www.naukri.com/job-listings-sr-engineer-i-data-engg-ai-anblicks-ahmedabad-0-to-1-years-130826501463) | Data warehouse, Azure SQL, lakehouse, CI/CD; title conflicts with 0–1 years label, so verify carefully |
| 13 | Naukri | ADP Private Limited | Financial Systems Professional | Hyderabad | 1 day ago | [Naukri](https://www.naukri.com/job-listings-financial-systems-professional-adp-pvt-ltd-hyderabad-0-to-5-years-270826504793) | Data migration, analytics, cloud platform signals; broad 0–5 label and title is not pure data engineering |
| 14 | Naukri | CSC | Expert Data Engineer | Bengaluru | 3 weeks ago | [Naukri](https://www.naukri.com/job-listings-expert-data-engineer-csc-bengaluru-0-to-4-years-050826504666) | Data lineage, cloud data, architecture, access control; older and “Expert” title conflicts with 0–4 label |
| 15 | Naukri | Diverse Lynx | Data Engineer II — Qlik, DBT, Snowflake | Chennai | 3 weeks ago | [Naukri](https://www.naukri.com/job-listings-data-engineer-ii-qlik-dbt-snowflake-diverse-lynx-chennai-0-to-4-years-050826504694) | Strong BI/data-stack match; title II and older posting require experience check |
| 16 | Naukri | Z Tech Solutions | Java, Python, AI and App Developer | Hyderabad / Chennai / Bengaluru | 2 days ago | [Naukri](https://www.naukri.com/job-listings-required-java-python-ai-and-app-developer-chennai-hyderabad-z-tech-solutions-hyderabad-chennai-bengaluru-0-to-1-years-250826018449) | Fresh software/AI alternative with Python; verify company and role legitimacy before applying |
| 17 | Naukri | Creative Hands HR | Software Engineer | Hyderabad / Chennai / Bengaluru | 3 days ago | [Naukri](https://www.naukri.com/job-listings-software-engineer-creative-hands-hr-hyderabad-chennai-bengaluru-0-to-2-years-240826004372) | Entry-level Java/C++/AI software role; relevant to software target, not data-specific |
| 18 | Naukri | Softblobs | Java Opportunity for Freshers | Hyderabad | 1 day ago | [Naukri](https://www.naukri.com/job-listings-java-opportunity-for-freshers-hyderabad-softblobs-hyderabad-0-to-0-years-270826014931) | Fresh software opportunity; appears internship-like, so verify paid employment and duration |
| 19 | Naukri | PGAGI | AI/ML & Backend Engineering Intern | Bengaluru | Current result | [Naukri](https://www.naukri.com/job-listings-ai-ml-backend-engineering-intern-pgagi-bengaluru-0-to-1-years-270826500804) | AI/ML, backend, Python-adjacent path; 6-month internship and ₹15,000/month shown; verify start date |
| 20 | Naukri | Medpace Clinical Research India | Senior Data Engineer | Navi Mumbai | 3 days ago | [Naukri](https://www.naukri.com/job-listings-senior-data-engineer-medpace-clinical-research-india-navi-mumbai-0-to-2-years-070126031460) | SQL Server, SSIS, ELT, Power BI; “Senior” conflicts with 0–2 label, so treat as uncertain until description is confirmed |

**Run status:** 20 new candidates identified; 4 have strong freshness signals (within 3 days), 8 are older or reposted, and 8 need detail-page verification. No applications made.

## NEW ABSOLUTE-FRESHER CANDIDATE POOL — 2026-08-28

These 20 roles were found using fresher/0-year searches and were not present in the earlier log. All appeared as recent results, generally within 1 week. Individual employer Apply-route verification is still required before applying unless explicitly noted.

| # | Platform | Company | Title | Location | Posted signal | Listing | Fresher relevance / caution |
|---:|---|---|---|---|---|---|---|
| 1 | LinkedIn | Barclays | Cloud Data Engineer | Pune | 2 minutes ago | [LinkedIn](https://www.linkedin.com/jobs/view/4457296423/) | Freshest; cloud data role; confirm exact experience requirement and Apply route |
| 2 | LinkedIn | HP | Data Engineer | Bengaluru hybrid | 2 days ago | [LinkedIn](https://www.linkedin.com/jobs/view/4458779765/) | Fresh data-engineering title; verify fresher eligibility in full description |
| 3 | LinkedIn | Zenithbyte | Python Developer Intern | India remote | Recent | [LinkedIn](https://www.linkedin.com/jobs/view/4459844575/) | Explicit internship and Python; ₹7,500/month shown; verify employer legitimacy and duration |
| 4 | LinkedIn | Crossing Infotech | Python Developer Intern | India remote | Recent | [LinkedIn](https://www.linkedin.com/jobs/view/4458385263/) | Explicit internship and Python; ₹16,500/month shown; verify employer and training obligations |
| 5 | LinkedIn | Mercor | Data Engineer — Fully Remote | India remote | Recent | [LinkedIn](https://www.linkedin.com/jobs/view/4458548230/) | Remote data-engineer role; headline shows up to $80/hour; verify assessment, contract, and actual fresher eligibility |
| 6 | Naukri | Cairovision | AI/ML Intern | Noida | Current last-7-days result | [Naukri](https://www.naukri.com/job-listings-ai-ml-intern-cairovision-noida-0-to-1-years-260826022245) | 0–1 years, 6-month internship, ₹8,000/month; verify start date and conversion prospects |
| 7 | Naukri | XPO India Shared Services | Trainee Technology — IT Interns | Hyderabad | 3 days ago | [Naukri](https://www.naukri.com/job-listings-trainee-technology-it-interns-xpo-india-shared-services-hyderabad-0-to-1-years-240826011012) | Fresh graduates/interns; Power BI, visualization, BI, data engineering, SQL; walk-in process |
| 8 | Naukri | Narayana Health | Application Support Engineer | Bengaluru | 1 day ago | [Naukri](https://www.naukri.com/job-listings-application-support-engineer-narayana-health-bengaluru-0-to-1-years-270826501211) | 0–1 years; analytics, data pipelines, cloud; support-focused but technically relevant |
| 9 | Naukri | Shahi | IoT Trainee | Bengaluru Bellandur | 2 days ago | [Naukri](https://www.naukri.com/job-listings-iot-trainee-shahi-bengaluru-0-to-1-years-250826014793) | Explicitly says 0–1 year and freshers can apply; Python/AI/IoT; verify technical depth |
| 10 | Naukri | Prolim | XHQ Developer | Bengaluru | 1 week ago | [Naukri](https://www.naukri.com/job-listings-xhq-developer-prolim-bengaluru-0-to-0-years-200826031172) | Explicit 0 years/fresher; Java, Python, SQL, DBMS; WFO |
| 11 | Naukri | Regami Solutions | Python Developer — PET Fresher | Chennai | 2 days ago | [Naukri](https://www.naukri.com/job-listings-python-developer-pet-fresher-regami-solutions-chennai-0-to-1-years-250826024647) | Python, ML/DL, MongoDB, MySQL, APIs; strong fresher match; verify live Apply |
| 12 | Naukri | Shashwath Solution | Research Analyst — Consultant | Pune | 1 week ago | [Naukri](https://www.naukri.com/job-listings-research-analyst-consultant-shashwath-solution-pune-0-to-1-years-200826930122) | Explicit freshers; data analysis, collection, databases; verify company and role quality |
| 13 | Naukri | Shashwath Solution | Research Analyst — Consultant | Noida | 1 week ago | [Naukri](https://www.naukri.com/job-listings-research-analyst-consultant-shashwath-solution-noida-0-to-1-years-200826922853) | Explicit freshers; data analysis/research/database work; separate requisition; verify employer |
| 14 | Naukri | Birlasoft | Oracle Cloud Planning Domain Professional | Pune | 1 week ago | [Naukri](https://www.naukri.com/job-listings-oracle-cloud-planning-domain-professional-birlasoft-india-limited-pune-0-to-1-years-200826501547) | Explicit fresh graduates 0–1; automation, data/business analysis; dual-qualification preference may apply |
| 15 | Naukri | HK Infosoft | Python AI/ML Intern | Ahmedabad | Current last-7-days result | [Naukri](https://www.naukri.com/job-listings-python-ai-ml-intern-hk-infosoft-ahmedabad-0-to-1-years-240826503742) | 0–1 years; Python and AI/ML; unpaid internship with no fixed duration and starts in 1–3 months |
| 16 | Naukri | Baashyaam Constructions | Application Tester | Chennai | 2 days ago | [Naukri](https://www.naukri.com/job-listings-application-tester-baashyaam-constructions-chennai-0-to-0-years-201125019434) | Explicit 0 years/fresher; SQL, application testing, bug tracking; QA rather than data engineering |
| 17 | Naukri | My Virtual Teams | QA Tester — Fresher | Ludhiana | 1 day ago | [Naukri](https://www.naukri.com/job-listings-qa-tester-fresher-my-virtual-teams-pvt-ltd-ludhiana-0-to-1-years-260826502364) | Explicit fresher/0–1; backend, REST, JavaScript, manual testing; QA/software path |
| 18 | Naukri | Antrix Propulsion | Firmware & Flight Control Engineer | Bengaluru | 3 days ago | [Naukri](https://www.naukri.com/job-listings-firmware-flight-control-engineer-antrix-propulsion-a-division-of-antrix-financial-engineers-pvt-ltd-bengaluru-0-to-1-years-240826003847) | Fresh graduates accepted; C++, embedded, ROS/ROS2; adjacent software/embedded path |
| 19 | Naukri | Exicube App Solutions | Software Engineer | Kolkata | 1 day ago | [Naukri](https://www.naukri.com/job-listings-engineers-exicube-app-solutions-opc-private-limited-kolkata-0-to-5-years-270826504522) | Software development, programming, version control; broad 0–5 label, so verify fresher acceptance |
| 20 | Naukri | Pitney Bowes | Graduate Engineer Trainee | Pune | Current recent result | [Naukri](https://www.naukri.com/job-listings-graduate-engineer-trainee-pitney-bowes-india-pvt-ltd-pune-0-to-2-years-260826502841) | Graduate-entry technical role; result shows unpaid internship and starts in 1–3 months — low priority |

**Run status:** 20 additional fresher-focused candidates identified; 15 are direct data/software/AI matches and 5 are adjacent QA, support, embedded, or analyst alternatives. No applications made.

## ADDITIONAL LINKEDIN QUERY RESULTS — 2026-08-28

These unique roles appeared in the current connected LinkedIn session after running Data Engineer, Junior Data Engineer, ETL Developer, Cloud Data Engineer, Analytics Engineer, Python Developer, Software Engineer, and Data Analyst queries with entry-level and past-week filters. They were not already recorded above.

| # | Company | Title | Location | Posted signal | Listing | Relevance / caution |
|---:|---|---|---|---|---|---|
| 1 | Optum India | Data Engineer Analyst | Hyderabad | 10–11 minutes ago | [LinkedIn](https://www.linkedin.com/jobs/view/4460125463/) | Very recent entry-level-filter result; verify exact experience and Apply route |
| 2 | Hakkōda, an IBM Company | Data Engineer — Data Platforms — Google | Gurgaon hybrid | 22 hours ago | [LinkedIn](https://www.linkedin.com/jobs/view/4459187316/) | Strong Google/cloud data-platform match; verify fresher eligibility |
| 3 | compoundexpress | Data Engineer | Mumbai hybrid | 16 hours ago | [LinkedIn](https://www.linkedin.com/jobs/view/4459657865/) | Very recent data-engineer listing; employer and role details require verification |
| 4 | MetLife | Associate Data Analyst | Noida hybrid | 20 hours ago | [LinkedIn](https://www.linkedin.com/jobs/view/4458101890/) | Associate-level analytics role; verify degree/experience requirements |
| 5 | Alignerr | E-commerce Data Analyst | India remote | 20 hours ago | [LinkedIn](https://www.linkedin.com/jobs/view/4459626973/) | Remote analytics role; $40–$120/hour signal needs contract and legitimacy verification |
| 6 | Bristol Myers Squibb | Software Engineer — Analytical Engineering | Hyderabad | 2 days ago | [LinkedIn](https://www.linkedin.com/jobs/view/4458760500/) | Analytical-engineering software role; verify technical stack and fresher fit |
| 7 | Bristol Myers Squibb EU Policy | Software Engineer — Analytical Engineering | Hyderabad | 2 days ago; early-applicant signal | [LinkedIn](https://www.linkedin.com/jobs/view/4456915722/) | Early-applicant signal; verify whether this is a separate requisition and current Apply route |
| 8 | Dentsu Global Services | Data & AI Engineer | Bengaluru | Date not shown | [LinkedIn](https://www.linkedin.com/jobs/view/4435260901/) | Relevant data/AI title; freshness and experience uncertain |
| 9 | Hirely | Software Engineer — Python, APIs & Docker | India remote | Date not shown | [LinkedIn](https://www.linkedin.com/jobs/view/4457701719/) | Python/API/Docker remote role; $40–$50/hour signal requires legitimacy verification |
| 10 | TELUS Digital AI Data Solutions | Remote Online Data Analyst — Punjabi Speakers | Chandigarh remote | Date not shown | [LinkedIn](https://www.linkedin.com/jobs/view/4458741143/) | Remote data-annotation/analysis alternative; language requirement and employment model need verification |

**Run status:** 10 additional unique LinkedIn roles recorded. Search result volumes were high, but many visible results were duplicates, senior roles, or listings with missing/contradictory experience data. No applications made.

## LINKEDIN PAGINATED DATA-ENGINEER RESULTS — 2026-08-28

The connected LinkedIn session was searched with the Data Engineer query, India location, Entry level filter, and Past week filter across page offsets 0–175. LinkedIn rendered 56 distinct job cards in those pages. The following 20 were new relative to the log and were relevant enough to retain after excluding duplicates, senior/lead roles, and clear experience mismatches. Exact age and live Apply route should be confirmed on each detail page before applying.

| # | Company | Title | Location | Listing | Search-status evidence / caution |
|---:|---|---|---|---|---|
| 1 | Optum India | Data Engineer Analyst | Hyderabad | [LinkedIn](https://www.linkedin.com/jobs/view/4460125463/) | Entry-level + past-week result; posted minutes ago in the session |
| 2 | Hakkōda, an IBM Company | Data Engineer — Data Platforms — Google | Gurgaon hybrid | [LinkedIn](https://www.linkedin.com/jobs/view/4459187316/) | Past-week result; posted about 22 hours ago |
| 3 | compoundexpress | Data Engineer | Mumbai hybrid | [LinkedIn](https://www.linkedin.com/jobs/view/4459657865/) | Past-week result; posted about 16 hours ago; employer details need review |
| 4 | Barclays | Data Engineer | Pune | [LinkedIn](https://www.linkedin.com/jobs/view/4456527342/) | Separate job ID from the earlier Barclays role; verify experience and Apply route |
| 5 | Infinity Learn | Software Engineer | Bengaluru | [LinkedIn](https://www.linkedin.com/jobs/view/4459346210/) | Entry-level-filter result; software role, technical details need review |
| 6 | Cummins India | Data Engineer 8 | Pune | [LinkedIn](https://www.linkedin.com/jobs/view/4457454807/) | New requisition; verify actual experience requirement because Cummins has multiple numbered roles |
| 7 | NextNation | AI Engineer | Bengaluru | [LinkedIn](https://www.linkedin.com/jobs/view/4458367240/) | Entry-level-filter result; AI/software-adjacent, verify Python/data scope |
| 8 | Aditi Consulting | Data Engineer | Chennai | [LinkedIn](https://www.linkedin.com/jobs/view/4447271335/) | Entry-level-filter result; verify employer route and exact requirements |
| 9 | Bristol Myers Squibb | Software Engineer, Analytical Engineering | Hyderabad | [LinkedIn](https://www.linkedin.com/jobs/view/4458218476/) | New requisition distinct from previously seen BMS role; analytical engineering scope |
| 10 | LG Ad Solutions | Software Engineer I | Bengaluru | [LinkedIn](https://www.linkedin.com/jobs/view/4458719155/) | Level-I software role; verify stack and fresher acceptance |
| 11 | USEReady | Technology Data Engineer — ADLS/Snowflake DB | Greater Kolkata | [LinkedIn](https://www.linkedin.com/jobs/view/4459616684/) | Strong cloud-data stack; verify experience and live Apply route |
| 12 | WalkingTree Technologies | Trainee Associate Software Engineer | Agra | [LinkedIn](https://www.linkedin.com/jobs/view/4458016650/) | Trainee title is promising for a fresher; verify compensation and tech stack |
| 13 | TestHiring | Data Engineer | Bengaluru | [LinkedIn](https://www.linkedin.com/jobs/view/4458638275/) | Entry-level-filter result; employer and description need careful verification |
| 14 | myKaarma | Software Developer I | Noida | [LinkedIn](https://www.linkedin.com/jobs/view/4458031223/) | Level-I software role; verify fresher eligibility |
| 15 | ASTIKA Software Technologies | Jr. Java Developer | Hyderabad | [LinkedIn](https://www.linkedin.com/jobs/view/4457743390/) | Junior software role; Java/SQL path, verify Apply route |
| 16 | Infosys | GenAI, Cloud & Backend Development | Hyderabad | [LinkedIn](https://www.linkedin.com/jobs/view/4438956517/) | Python/APIs/cloud/backend relevance; verify exact level and experience |
| 17 | Webkit24 | Junior Developer | India remote | [LinkedIn](https://www.linkedin.com/jobs/view/4457473098/) | Remote junior role; employer and compensation need verification |
| 18 | Onehouse | Software Engineer, Distributed Data Systems | Greater Kolkata remote | [LinkedIn](https://www.linkedin.com/jobs/view/4458307621/) | Strong distributed-data systems relevance; verify fresher fit |
| 19 | AiPrise | Software Engineer I | Bengaluru | [LinkedIn](https://www.linkedin.com/jobs/view/4457651871/) | Level-I role; verify stack, eligibility, and live Apply route |
| 20 | Vanguard India | Application Engineer I | Hyderabad hybrid | [LinkedIn](https://www.linkedin.com/jobs/view/4458666012/) | Level-I application role; software-adjacent, verify requirements |

**Run status:** 56 distinct LinkedIn cards observed across the paginated Data Engineer result set; 20 new relevant roles retained after deduplication and filtering. No applications made.

## EASY-APPLY / IN-PLATFORM APPLY RUN — 2026-08-28

- LinkedIn: Easy Apply filter verified; 20 unique candidate links collected across Data Engineer, Junior Data Engineer, ETL Developer, Python Developer, Software Engineer, and Data Analyst queries. The full list was returned to the user in this run.
- Naukri: 20 unique candidate links collected; each included only after its detail page visibly showed `Apply`, excluding pages showing `Apply on company site`.
- Freshness: Naukri candidates were posted 1–6 days ago; LinkedIn candidates came from the Past week filter.
- Applications: 0. Search-only run; explicit authorization is still required.

## TEMPLATE FOR FUTURE ENTRIES

**Copy-paste after each search run:**

```
### Search Run: [DATE]

| Metric | Value | Notes |
|---|---|---|
| Role Families Searched | Q1, Q2, Q3 (example) | — |
| Geographies Covered | Pune, Bengaluru | — |
| Platforms Checked | LinkedIn, Naukri | — |
| Total Discovered | X jobs | — |
| Duplicates Removed | Y jobs | Previous run references |
| New Qualifying (Fit ≥ 75) | Z jobs | Shortlisted in table above |
| Rejected / Stale | W jobs | Detailed below |
| Next Action | [Next step] | — |

**New Shortlisted Jobs**:
[Copy table rows above with actual data]

**Rejected This Run**:
[List any jobs that failed to qualify]

**Application Status**:
[Note any applications made, interview feedback, offers]
```

---

## FIELDS EXPLAINED

| Field | Purpose | Example |
|---|---|---|
| **Date Found** | When discovered during search | 2026-08-28 |
| **Platform** | Source (LinkedIn, Naukri, Indeed, etc.) | LinkedIn |
| **Company** | Official company name | Google, Amazon, Accenture |
| **Normalized Title** | Standardized role name (strip seniority qualifiers) | "Data Engineer" (not "Senior Data Engineer") |
| **Location** | City or "Remote" / "India Remote" | Pune, Bengaluru, Remote |
| **Job ID / URL** | Unique identifier (copy-paste job link) | linkedin.com/jobs/view/12345/ |
| **Status** | Current state (New, Shortlisted, Applied, Interview, Offer, Rejected, Closed) | Shortlisted |
| **Tier** | Role classification (T1, T2, T3, T4) | T1 |
| **Fit Score** | Calculated from 02_TARGET_ROLES.md formula (0–100) | 88 |
| **Notes** | Reason for score, highlights, concerns, follow-ups | "Airflow + Snowflake + immediate joiner = strong match; apply to this" |

---

## QUICK QUERIES (For Finding Information)

**To check if a job was already logged**:
```
Ctrl+F: "[Company Name]" in this file
If found: Do not report again
If not found: Check Fit ≥ 75; add if qualified
```

**To see shortlist before applying**:
```
Scroll to SHORTLISTED table
Filter by Status = "Shortlisted"
Sort by Fit Score descending
Apply to top 3–5 first; wait for responses before applying to rest
```

**To see application history**:
```
Scroll to APPLIED table
Filter by Date Applied (most recent first)
Check "Interview Date" column for follow-ups needed
```

---

## IMPORTANT RULES

1. **Update immediately after search**: Do not delay logging; add jobs same day
2. **Never invent fields**: If you don't have a Job ID, copy the exact URL
3. **Fit Score is mandatory**: Calculate using 02_TARGET_ROLES.md formula; never estimate
4. **One entry per unique job**: If same job appears on multiple platforms, keep first and note alternates
5. **Status transitions are one-way** (with exceptions):
   - `New → Shortlisted → Applied → Interview → Offer` ✓ (forward only)
   - `Shortlisted → Rejected` ✓ (if fit re-evaluated as <70)
   - `Rejected → Revisit` ✓ (only if job description materially changed)
6. **Do not delete entries**: Mark as "Closed" or "Rejected" instead; keep full history
7. **Weekly review**: Every Friday, review "Applied" status; note interview dates and follow-ups

## FRESH VERIFIED SEARCH RUN — 2026-08-28

Search scope: public web, official employer/ATS pages, Wellfound and Cutshort discovery. LinkedIn/Naukri session coverage was not counted as verified for this run. No applications were submitted.

### New candidate retained

| Company | Role | Location | Source / application route | Freshness evidence | Fit / decision |
|---|---|---|---|---|---|
| Springer Capital | Tech Assistant Intern — Data Engineering & DevOps | Remote, India | [Cutshort listing](https://cutshort.io/job/Tech-Assistant-Intern-Data-Engineering-DevOps-Remote-Springer-Capital-2ao242HR) | Cutshort crawled the job today; listing shows 0–1 years, remote, 3–6 month internship, and Apply to this job | **80/100 — shortlist, low priority.** Python, SQL, data processing and data-pipeline responsibilities match; stipend shown as ₹5,000–₹7,000/month and the listing covers several unrelated domains, so verify the actual team, mentor and PPO terms before investing time. |

### Verification holds / rejected results

- **GEA — Associate Data Engineering, Bengaluru:** official Workday result was posted about 7 days ago with a 30-Aug-2026 closing date and strong pipeline responsibilities, but the indexed employer page did not expose enough requirements to calculate a defensible fit score. Keep as **verification hold**, not an approved match.
- **AffinityAnswers — Data Engineer Internship:** Wellfound showed “posted today,” but the employer careers page says there are currently no available positions. **Rejected as conflicting / not safely verified.**
- **TECHNOSCIEN — Data Engineer & Market Intelligence:** Wellfound showed “posted today,” but the description is primarily market research/data analysis and does not establish Python/SQL/ETL core requirements. **Rejected for profile mismatch.**
- **Snowflake — Data Engineer Intern, Pune (2026):** the official LinkedIn result explicitly says “No longer accepting applications.” **Closed; do not resurface.**
- **Amgen — Associate Data Engineer, Hyderabad:** official Workday result requires 2–6 years. **Rejected for experience mismatch.**
- **WPP Media — Associate, Data Technology & Analytics:** official Greenhouse page is live and new, but requires around 1–2 years of analytics experience and is client/market-research oriented rather than a core data-engineering role. **Stretch/adjacent only; not a primary match.**

**Run result:** 1 new shortlist, 1 verification hold, 5 rejected or downgraded after direct-page checking. Existing Teal, AstraZeneca, Cloud Champ and other previously reported roles were not repeated.

## FRESH VERIFIED SEARCH RUN — 2026-08-29

Search scope: fresh public web search across official/ATS discovery, LinkedIn, Wellfound, Cutshort, and Internshala. Date window: 2026-08-22 through 2026-08-29. No applications were submitted. Existing logged roles were not repeated.

### New candidate retained

| Company | Role | Location | Source / application route | Freshness evidence | Fit / decision |
|---|---|---|---|---|---|
| Zensar Technologies | Junior Data Engineer / DWH & Python Developer | Pune | [LinkedIn listing](https://in.linkedin.com/jobs/view/de-a-core-data-engineering-microsoft-sql-server-at-zensar-technologies-4384999585) | Listing shows 2 days ago and Apply; fresher/entry-level wording; Python, SQL, DWH, ETL, Git and cloud learning | **92/100 — shortlist, high priority.** Very close to the target level and Pune preference. |
| NorthStar HR Consultants | Data Engineer | Pune | [Internshala listing](https://internshala.com/job/detail/data-engineer-job-in-maharashtra-at-northstar-hr-consultants1773534753) | Listing shows posted just now and Apply; 1 year; Pune; Airflow, Glue, Data Fusion, Dataflow, BigQuery, PostgreSQL and SQL | **91/100 — shortlist, high priority.** Strong direct match to the GCP/Airflow/migration profile. |
| Data Eminence | Data Engineer | Remote, India | [LinkedIn listing](https://in.linkedin.com/jobs/view/data-engineer-at-data-eminence-4457970107) | Listing shows 13 hours ago and Apply; 0–2 years; remote; Python, SQL, ETL, databases, Git, Docker and cloud | **90/100 — shortlist, high priority.** Entry-level and remote; contract status should be checked before accepting. |
| Photon | Data Engineer — Airflow/Snowflake | Chennai/Bengaluru/India remote | [Built In listing](https://builtinmumbai.in/job/data-engineer-chennai-bengaluru/10781303) | Listing shows posted yesterday, entry-level, remote in India and live employer route | **89/100 — shortlist, high priority.** Airflow, Python, SQL, Snowflake, PySpark and pipeline work align strongly. |
| EXL | Data Engineer — Fresher | Bengaluru | [Internshala listing](https://internshala.com/job/detail/fresher-data-engineer-job-in-bangalore-at-exl1773140887) | Listing shows posted just now, fresher, no experience required and Apply now | **87/100 — shortlist.** Strong level match; verify the exact work mode and employer application route. |
| Joveo | Data Engineer | Bengaluru | [Internshala listing](https://internshala.com/job/detail/data-engineer-job-in-bangalore-at-joveo1773448352) | Listing shows posted just now, 1 year experience and Apply now | **84/100 — shortlist.** Good entry-level fit; data-platform and recruitment-tech exposure are relevant. |
| LTM | Data Engineer — Enterprise Data Warehouse | Chennai | [LinkedIn listing](https://in.linkedin.com/jobs/view/python-%2B-sql-%2B-pandas-at-ltm-4455015758) | Listing shows 6 hours ago and entry-level; Python, SQL, Pandas, Databricks/cloud platform and orchestration | **82/100 — shortlist.** Strong stack match, but Chennai relocation may be required. |
| Entain India | Junior Data Engineer | Hyderabad | [LinkedIn listing](https://in.linkedin.com/jobs/view/junior-data-engineer-at-entain-india-4414559097) | Listing shows 2 days ago and Apply; entry-level; Python, SQL, BigQuery/Snowflake, data quality and CI/CD | **82/100 — shortlist.** Good junior-level fit; Hyderabad location. |
| Intileo Technologies | Data Analyst | Delhi | [LinkedIn listing](https://in.linkedin.com/jobs/view/data-analyst-at-intileo-technologies-llp-4424061207) | Listing shows 1 day ago and 33 applicants; SQL, Python, Databricks, ADF and data pipelines | **72/100 — adjacent shortlist.** Use analytics resume; 2–3 years requested makes it a stretch. |

### Rejected or held this run

- **Synechron — Cloud Data Engineer, Bengaluru:** live and 1 day old, but explicitly requires 5+ years. Rejected for experience mismatch.
- **UPS — GCP Data Engineer, Chennai:** live and 1 day old, but explicitly requires 5+ years. Rejected for experience mismatch.
- **Qloron — Data Engineer, Bengaluru/Hyderabad:** live and 13 hours old, but all listed technologies and 5+ years are mandatory. Rejected for experience mismatch.
- **Luxoft — Data Engineer, Pune:** live and 3 hours old, but mid-senior and not entry-level. Held only as a low-probability stretch.
- **Qualkode Technologies — Data Engineer, Bengaluru:** live and 10 hours old, but the description is for a 10+ year senior role despite the inconsistent “entry level” label. Rejected as internally conflicting.
- **Rocket India — AWS Data Engineer, Chennai:** live and 2 hours old, but requires 4–8 years. Rejected for experience mismatch.
- **MetricsLand — QuickSight Trainee/Junior Analyst:** recent, but the one-year commitment and delayed retention-bonus structure make it low quality for this search. Rejected.

**Run result:** 9 new candidates retained: 8 primary/strong matches and 1 adjacent match. The strongest actions are Zensar, NorthStar, Data Eminence, Photon and EXL. No applications were submitted.

## SEARCH RUN — 2026-08-30 — INCOMPLETE: BROWSER SESSION ACCESS BLOCKED

Historical incident record only: at that time, this task could not establish a usable connection to the user’s open authenticated Chrome session. LinkedIn and Naukri session coverage therefore could not be performed or claimed. No public-web substitute search was reported as a complete run, and no applications were submitted. The connection check at the top of this file supersedes this record for current capability; future runs must use the current connection rule rather than stopping the entire source sequence.

| Source | Status | Reason |
|---|---|---|
| Official company career page / ATS | Not searched | Browser-first requirement blocked before source sequence could begin |
| Referral through LinkedIn, alumni, Reddit, or professional contacts | Not searched | Browser-first requirement blocked |
| LinkedIn signed-in session | Unavailable | Connected browser control was not usable in this task |
| Cutshort | Not searched | Run stopped at required browser-access check |
| Wellfound | Not searched | Run stopped at required browser-access check |
| Instahyre and Hirist | Not searched | Run stopped at required browser-access check |
| Reddit and X | Not searched | Run stopped at required browser-access check |
| Naukri signed-in session | Unavailable | Connected browser control was not usable in this task |
| Indeed, Foundit, Internshala, and niche portals | Not searched | Run stopped at required browser-access check |

**Next action:** restore or reconnect the open Chrome session, then rerun the search. Do not treat this run as complete coverage.

## FRESH VERIFIED SEARCH RUN — 2026-08-30

Search scope: public web and public job pages, with official/ATS and live Apply routes prioritized. Date window: 2026-08-23 through 2026-08-30. Existing logged roles were deduplicated. No applications were submitted.

### New candidate retained

| Company | Role | Location | Source / application route | Freshness evidence | Fit / decision |
|---|---|---|---|---|---|
| Cummins India | Data Engineer 1 | Pune | [LinkedIn listing](https://in.linkedin.com/jobs/view/data-engineer-1-at-cummins-india-4456053014) | Listing shows 1 hour ago, Apply, and entry-level relevant experience preferred; ETL/ELT, data quality, pipelines, cloud/data platforms | **94/100 — shortlist, highest priority.** Excellent Pune and level match; strong pipeline/data-quality scope. |
| GE Appliances | Associate Data Engineer | Bengaluru/Hyderabad | [Listing](https://in.talent.com/view?id=634410882453217032) | Listing shows 1 day ago and Apply; recent-graduate profile; SQL, BigQuery, ETL and Python preferred | **86/100 — shortlist.** Strong entry-level fit; more BI/Tableau-oriented than core pipeline engineering. |
| NextGen Digital Solutions | Databricks Data Engineer | Mumbai | [LinkedIn listing](https://in.linkedin.com/jobs/view/databricks-data-engineer-at-nextgen-digital-solutions-nds-4456887553) | Listing shows 5 hours ago, Apply, and 1–3 years; Databricks, PySpark, SQL, Delta Lake, ETL/ELT | **80/100 — shortlist/stretch.** Strong skills match but asks for 1–3 years and Mumbai. |
| Pall Corporation | Engineer — Data Analytics and Applications | Pune | [Listing](https://www.simplyhired.co.in/en-IN/search?l=pune%2C+maharashtra&q=ai+data) | Listing shows 1 hour ago and Apply Now; Python, SQL, AWS, APIs and analytics | **76/100 — adjacent shortlist.** Useful data/software fallback; exact employer requisition should be opened before applying. |
| Bain & Company | Senior Associate Engineer — Data Engineering | Delhi | [Listing](https://www.simplyhired.co.in/job/eaW0YFK-a8kjGcMSJ-A1CtGsiCv0JW3g1k4tHlyg9MFCJRS6uu38XQ) | Listing shows 1 day ago and Apply Now; 1–3 years; SQL, Python, Airflow/dbt, Databricks and cloud data | **75/100 — stretch shortlist.** Strong stack, but Delhi and consulting/client delivery requirements. |

### Rejected or held this run

- **Calitii — Snowflake & Python Data Engineer, Pune:** live and 1 day old, but requires 8+ years.
- **Mizuho — SSIS and Python Developer, Pune:** live and 4 hours old, but requires 5–12+ years.
- **Infosys — AWS Data Engineer, Pune:** live and 5 days old, but mid-senior and requires deep AWS/Redshift experience.
- **Amrapali Solutions — Jr. Data Engineer, Pune:** live and 1 hour old, but explicitly requires 2–4 years plus Kafka/Spark; held as a stretch only.
- **Viraaj HR Solutions — AWS Data Engineer, Pune:** excluded because the job page says no longer accepting applications.
- **Contrarian Thinking — Data Engineer Contract:** excluded because the job page says no longer accepting applications.

**Run result:** 5 new candidates retained: 3 strong data-engineering matches and 2 adjacent/stretch roles. Best immediate target is Cummins India, followed by GE Appliances and NextGen Digital Solutions.

## PUBLIC FALLBACK SEARCH RUN — 2026-10-01

Search scope: public web and official employer/ATS pages. Current Chrome extension connection check succeeded, but no authenticated LinkedIn or Naukri tab was available, so LinkedIn/Naukri session coverage was not counted. Queries covered core Data Engineer, Cloud Data Engineer, ETL/Data Pipeline, Analytics/BI, junior/associate variants, Pune, India remote, Bengaluru, Hyderabad, and secondary cities. No applications were submitted.

### Browser/source coverage

| Item | Result |
|---|---|
| Browser capability | Browser tool available; Chrome extension connected |
| Authenticated LinkedIn/Naukri tabs | Not available in current session |
| Coverage label | Public fallback — no authenticated LinkedIn/Naukri session coverage |
| Official ATS/employer pages | Searched and used for verification where available |
| Public boards/discovery | Used for lead discovery only; not treated as proof of active status |
| Page coverage | Search-result pages reviewed until relevant current candidates and direct-page verification were exhausted |

### New verified active matches

None. No new role passed both the direct active-Apply check and the entry-level/0–1-year filter without conflicting requirements.

### Verification holds / rejected results

- **Fujitsu — Junior Data Engineer, Pune, Req. 10854:** public reposts describe an entry-level role posted Aug. 25 with SQL, ETL/ELT, data validation, pipeline monitoring and basic Python. The official Fujitsu careers site was reachable, but a job-specific official page could not be located or confirmed in the current search. **Uncertain — do not report as actionable until the official requisition page exposes Apply.**
- **V4C.ai — Associate Data Engineer, Pune:** public listings show Python/SQL, training, immediate joining and a Pune training period, but the official careers page currently lists Associate Data Scientist, Data Scientist and Program Manager—not Associate Data Engineer. **Uncertain/conflicting; do not apply from third-party forms without direct official confirmation.**
- **TaskUs — Associate Data Engineer, Airoli/remote, Req. R_2609_12417:** official page is live with Apply Now and was posted Sep. 24, but requires at least 2 years of data engineering, 2 years of data modeling/ETL development and 3 years of cloud analytics. **Rejected for experience mismatch.**
- **Amgen — Associate Data Engineer, Hyderabad, Req. R-253369:** official page is live with Apply Now and was posted Sep. 11, but requires a bachelor's degree plus 2–4 years of experience. **Rejected for experience mismatch.**
- **5X — Remote Junior Data Engineer, India:** page is live and a strong stack match, but it requires 1+ year, is a job-board-sourced page with no reliable current posting date, and does not provide a verified employer ATS application route in the page. **Uncertain/older; not added as active.**
- **Workforce Next — Data Engineer (Spark/Airflow), remote India:** official page is live with Apply, but requires 2–6 years. **Rejected for experience mismatch.**
- **Photon — Data Engineer, remote India:** direct listing is live and highly relevant, but it already appears in the Aug. 29 search log. **Deduplicated; not repeated.**
- **AstraZeneca — Associate Data Engineer:** direct listing reports the job was removed. **Closed; not repeated.**

**Run result:** 0 new verified active matches; 2 uncertain entry-level leads requiring official-page confirmation; 4 rejected for experience mismatch; 1 duplicate; 1 closed. Priority follow-up is to verify Fujitsu Req. 10854 directly or restore authenticated LinkedIn/Naukri tabs for the next run.

## VERIFIED SEARCH RUN — 2026-10-01 (AUTHENTICATED PLATFORM COVERAGE)

Search scope: connected Chrome session with authenticated LinkedIn and Naukri tabs, plus official/public employer pages for verification. LinkedIn Q1 Data Engineer search covered Pune, entry-level, past-week filter: 78 visible results on page 1; Naukri Data Engineer search covered Pune, fresher, 679 results, with page 1 reviewed. Existing log entries were deduplicated. No applications were submitted.

### Historical leads from this run (superseded by revised source policy)

The MailerMen entries below remain for auditability, but they are **not current shortlist recommendations**. Under the revised policy, generic aggregator/repost sources do not count unless the matching official employer ATS/careers page is verified.

| Company | Role | Location | Source / application route | Freshness evidence | Fit / decision |
|---|---|---|---|---|---|
| MailerMen | Data Engineer (Fresher) | Ahmedabad, on-site | [MailerMen listing](https://www.mailermen.com/jobs/data-engineer-fresher-onsite-india-532) | Page shows actively hiring, 0–1 years, Apply Now, and apply-before date 20-Oct-2026; page has a freshness conflict (header says 19 minutes, job overview says 19-Sep-2026) | **88/100 — shortlist, verify date before applying.** Python, SQL/ETL, PostgreSQL, Git, data modeling and pipeline/data-quality work; guided tasks and mentorship. Lower salary band shown: ₹2.4–₹2.9 LPA. |
| MailerMen | Data Engineering Intern — ETL & Pipelines | Remote, India | [MailerMen listing](https://www.mailermen.com/jobs/data-engineering-intern-etl-pipelines-remote-india-278) | Page shows actively hiring, 0 years, remote, Apply Now, posted 4-Sep-2026, 25+ applicants | **93/100 — shortlist, internship fallback.** Python, SQL, Airflow, ETL, PostgreSQL, Docker, REST APIs and pipeline work; ₹22,000–₹28,000/month, six months. |
| MailerMen | Data Quality Intern — SQL & Validation | Remote, India | [MailerMen listing](https://www.mailermen.com/jobs/data-quality-intern-sql-validation-remote-india-282) | Page shows actively hiring, 0 years, remote, Apply Now, posted about 24 days ago, 25+ applicants | **93/100 — shortlist, secondary.** Python, SQL, PostgreSQL, pandas, Great Expectations, profiling and validation; ₹16,500–₹21,000/month. |
| MailerMen | Data Engineer | Jaipur, on-site | [MailerMen listing](https://www.mailermen.com/jobs/data-engineer-onsite-india-488) | Page shows actively hiring, 1 year, Apply Now, posted 29-Sep-2026 | **78/100 — additional relevant.** Python, SQL, ETL, pipelines, PostgreSQL and Git; ₹4.7–₹5 LPA. Requires Jaipur on-site. |
| MailerMen | Data Engineer | Indore, on-site | [MailerMen listing](https://www.mailermen.com/jobs/data-engineer-579) | Page shows actively hiring, 1 year, posted 12-Sep-2026, Apply route, application deadline 16-Oct-2026, 25+ applicants | **78/100 — additional relevant.** Python, SQL, ETL, pipelines, PostgreSQL and Git; ₹4.8–₹5 LPA. Requires Indore on-site. |

### Rejected / held this run

- **MailerMen — Data Engineer, Pune remote, job 509:** direct page is active, but it requires about 2 years; rejected under the 2+ year mismatch rule.
- **MailerMen — Data Engineer, Hyderabad remote, job 505:** direct page is active, but it requires about 2 years; rejected under the 2+ year mismatch rule.
- **Naukri — Comprinno Technologies Data Engineer:** visible result is 0–2 years and 3+ weeks old; no job-specific active-Apply verification completed, so held rather than reported active.
- **Naukri — Precision Medicine Group Data Engineer:** visible result is 0–3 years and 3+ weeks old; experience and active status not sufficiently verified.
- **Naukri — Parkar Global Technologies Intern - Data Engineer:** unpaid internship starting in 1–3 months; low-quality/low-urgency lead, not shortlisted.
- **LinkedIn — Snowflake Cloud Support Engineer, Accenture Data Engineer, Innovative Information Technologies Data Engineer, and other page-1 results:** title/location signals were visible, but job-specific experience and active employer application evidence were not sufficient to classify them as qualifying matches in this run.

**Historical run result:** 5 leads were recorded, but they are excluded from the current active shortlist under the revised source policy. Future searches must prioritize LinkedIn and Naukri, then verify on official employer pages.

## VERIFIED SEARCH RUN — 2026-10-01 (REQUESTED COUNT: 20)

Search scope: authenticated LinkedIn first, then authenticated Naukri, followed by official employer/ATS pages. LinkedIn used India + entry-level + past-week filters across Data Engineer, Junior Data Engineer, ETL Engineer, and Data Quality Engineer searches. Naukri used Pune + fresher + last-7-days filters. No applications were submitted.

### New active matches retained

| Company | Role | Location | Source / application route | Freshness evidence | Fit / decision |
|---|---|---|---|---|---|
| Orange Business | Data Engineer | Gurgaon, hybrid | [LinkedIn listing](https://www.linkedin.com/jobs/view/4473702636/) / [official Orange ATS](https://careers-orange.icims.com/jobs/28354/data-engineer/job) | LinkedIn showed 16 hours ago; employer iCIMS requisition 28354 is reachable | **Strong current match.** Official employer route verified; confirm experience requirements in the ATS form before applying. |
| CGI | Data Engineer | Bengaluru, onsite | [LinkedIn listing](https://www.linkedin.com/jobs/view/4471677544/) / [official CGI listing](https://cgi.njoyn.com/corp/xweb/xweb.asp?clid=21001&page=jobdetails&jobid=J0926-0524&BRID=1335771&SBDID=943&lang=1) | LinkedIn showed 6 days ago; official CGI page is live with an Interested action | **Relevant but stretch.** Python, SQL, Databricks, Snowflake, pipelines and cloud are listed; description is data-science-heavy and does not state 0–1 years. |
| NK Securities Research | Data Engineer | Gurugram, onsite | [LinkedIn listing](https://www.linkedin.com/jobs/view/4473797277/) / [official Greenhouse ATS](https://job-boards.eu.greenhouse.io/nksecuritiesresearch/jobs/4990740101) | LinkedIn showed 6 hours ago; official Greenhouse page is live and marked New | **Strong skills match, experience stretch.** Python, SQL, APIs, data pipelines, quality checks and orchestration; employer asks for 1–3 years. |
| Barclays | Data Engineer — PySpark Developer | Bengaluru, onsite | [LinkedIn listing](https://www.linkedin.com/jobs/view/4471744580/) / [official Barclays route](https://search.jobs.barclays/job/-/-/13015/98506862192?src=JB-12860) | LinkedIn showed 17 hours ago; LinkedIn exposed the Barclays employer application route | **Technical match, verification hold.** PySpark/data-engineering title matches the profile, but full requirements and exact experience could not be read reliably. |

### Excluded from the active shortlist

- **Uber — Data Analytics Engineer I, Tech - Data:** LinkedIn showed 1 day ago, but the official Uber page reports the job removed and asks for at least 2 years; excluded.
- **MailerMen listings:** excluded under the revised policy because they are aggregator/repost-only sources without a verified canonical employer page.
- **Naukri page-1 results:** reviewed 20 of 37 fresh Pune results; most were software, support, QA, BI, intern, or non-data titles. No new role passed the core data-engineering and experience checks with a verified active route.
- **Public fallback results:** generic aggregator/repost pages and US-only roles were excluded; no canonical India employer verification was available.

**Run result:** 4 new current candidates retained, not 20. The search returned fewer than 20 safe matches after freshness, relevance, experience, deduplication, and source verification. No padding or applications made.

## SEARCH POLICY UPDATE — 2026-10-01

- Numeric requests are now collection targets: search exhaustively for exactly the requested number whenever valid results exist.
- Search all configured pages, Indian locations, and related data-role families instead of limiting the run to Pune or the first page.
- Exclude jobs older than 14 days by default, plus any job marked closed, expired, removed, or no longer accepting applications.
- Use lightweight status checks and do not discard a recent active platform listing solely because an employer ATS page is inaccessible.
- Deduplicate by canonical URL, job ID, or confirmed identical requisition. Same company/title alone is not enough.

## VERIFIED SEARCH RUN — 2026-10-01 (REQUESTED COUNT: 20; BROAD INDIA COVERAGE)

Search scope: authenticated LinkedIn and Naukri. LinkedIn reviewed Data Engineer pages 1–3 plus Junior Data Engineer, Cloud Data Engineer, and Analytics Engineer searches across India with entry-level and past-week filters. Naukri reviewed all-India Data Engineer pages 1–2 and ETL Engineer page 1 with 0-year and 14-day filters. No applications were submitted.

### 20 current candidates returned

The first group is closest to the target profile. The second group contains adjacent data/cloud/Python roles used to reach the requested count; these are clearly labeled so the user can prioritize them appropriately.

| # | Company | Role | Location | Source | Freshness | Fit category / note |
|---:|---|---|---|---|---|---|
| 1 | MandelBulb Technologies | Data Engineer | Jaipur, onsite | [LinkedIn](https://www.linkedin.com/jobs/view/4472698145/) | Minutes ago | Core match; Easy Apply visible. |
| 2 | Orange Business | Data Engineer | Gurgaon, hybrid | [LinkedIn](https://www.linkedin.com/jobs/view/4473702636/) / [official ATS](https://careers-orange.icims.com/jobs/28354/data-engineer/job) | 16 hours ago | Core match; employer route available. |
| 3 | NK Securities Research | Data Engineer | Gurugram, onsite | [LinkedIn](https://www.linkedin.com/jobs/view/4473797277/) / [official ATS](https://job-boards.eu.greenhouse.io/nksecuritiesresearch/jobs/4990740101) | 6 hours ago | Core match; asks 1–3 years, so stretch. |
| 4 | CGI | Data Engineer | Bengaluru, onsite | [LinkedIn](https://www.linkedin.com/jobs/view/4471677544/) / [official listing](https://cgi.njoyn.com/corp/xweb/xweb.asp?clid=21001&page=jobdetails&jobid=J0926-0524&BRID=1335771&SBDID=943&lang=1) | 6 days ago | Core match; data-science-heavy description, stretch. |
| 5 | Barclays | Data Engineer — PySpark Developer | Bengaluru, onsite | [LinkedIn](https://www.linkedin.com/jobs/view/4471744580/) / [Barclays route](https://search.jobs.barclays/job/-/-/13015/98506862192?src=JB-12860) | 17 hours ago | Strong technical match; requirements need final review. |
| 6 | Accenture in India | Data Engineer | Bengaluru, onsite | [LinkedIn](https://www.linkedin.com/jobs/view/4464341527/) | 6 days ago | Core title; confirm exact level before applying. |
| 7 | Accenture in India | Data Engineer | Chennai, onsite | [LinkedIn](https://www.linkedin.com/jobs/view/4448339912/) | 6 days ago | Core title; confirm exact level before applying. |
| 8 | Blumetra Solutions India | Data Engineers — Fresher | Hyderabad | [Naukri search](https://www.naukri.com/data-engineer-jobs?experience=0&jobAge=14) | 1 day ago | Core match; restricted to IIT/NIT graduates. |
| 9 | Quadrasystems.net | Azure Data Engineer | Bengaluru | [Naukri search](https://www.naukri.com/data-engineer-jobs?experience=0&jobAge=14) | 6 days ago | Core/cloud match; 0–1 years shown. |
| 10 | Infytrix | Data Engineer Intern | Mumbai | [Naukri search](https://www.naukri.com/data-engineer-jobs?experience=0&jobAge=14) | Just now | Core internship; verify stipend and duration. |
| 11 | Relu Consultancy | Data Extraction Engineer — Python | Remote | [Naukri search](https://www.naukri.com/data-engineer-jobs?experience=0&jobAge=14) | 6 days ago | Adjacent Python/data-extraction role. |
| 12 | Jobgether | Python Engineer | India remote | [LinkedIn](https://www.linkedin.com/jobs/view/4470767526/) | 5 days ago | Adjacent Python role; inspect data responsibilities. |
| 13 | ZS | Business Technology Solutions Associate — AI Engineering | Pune/Bengaluru/Gurugram | [Naukri search](https://www.naukri.com/data-engineer-jobs?experience=0&jobAge=14) | 1 week ago | Adjacent Python/SQL/analytics role, 0–4 years. |
| 14 | Incanus Technologies | Business Analyst — Data/Business Analytics | Delhi NCR/Bengaluru/Mumbai | [Naukri search](https://www.naukri.com/etl-engineer-jobs?experience=0&jobAge=14) | 2 days ago | Adjacent SQL/Python/data-analytics role. |
| 15 | Vgen Software Solutions | Data Analyst | Coimbatore | [Naukri search](https://www.naukri.com/etl-engineer-jobs?experience=0&jobAge=14) | 1 week ago | Adjacent SQL/Python/data-cleansing role. |
| 16 | Gramik | AI/ML Trainee | Noida | [Naukri search](https://www.naukri.com/data-engineer-jobs?experience=0&jobAge=14) | 5 days ago | Adjacent Python/data-processing trainee role. |
| 17 | Ecordon Solutions | AI Engineer | Noida | [Naukri search](https://www.naukri.com/data-engineer-jobs?experience=0&jobAge=14) | 1 week ago | Adjacent AI/data-engineering-tagged fresher role. |
| 18 | Tech Mahindra | Machine Learning Engineer | Pune/Noida/Bengaluru, hybrid | [Naukri search](https://www.naukri.com/data-engineer-jobs?experience=0&jobAge=14) | 1 day ago | Adjacent ML/pipeline role; weaker than core data engineering. |
| 19 | Deutsche Bank | SQL Developer, AS | Pune, hybrid | [LinkedIn](https://www.linkedin.com/jobs/view/4473934241/) | 12 hours ago | Adjacent SQL/database role; confirm ETL scope. |
| 20 | Nike | Software Engineer I, ITC | Karnataka, onsite | [LinkedIn](https://www.linkedin.com/jobs/view/4473265876/) | 8 hours ago | Tier-3 fallback; include only if Python/data scope is confirmed. |

### Excluded during this run

- MailerMen postings were excluded because they are aggregator/repost-only sources.
- Uber was excluded because the listing requires at least 2 years and the official page was previously confirmed removed.
- Jobs older than 14 days, closed/uncertain postings, senior roles, unpaid internships, support roles, sales roles, and unrelated software roles were excluded.

**Run result:** 20 current candidates collected: 10 core or near-core data-engineering roles and 10 adjacent/stretch roles. No applications were submitted.
