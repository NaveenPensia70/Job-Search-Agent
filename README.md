````
# Job Search Operating System

A structured, profile-driven job search workspace for discovering relevant entry-level Data Engineering and Software Engineering roles in India and remote locations.

## Purpose

This system helps to:

- Search for fresh and relevant job opportunities
- Prioritize LinkedIn and Naukri
- Search across multiple pages and locations
- Return the requested number of valid jobs when available
- Avoid duplicate, stale, closed, and irrelevant listings
- Rank roles according to profile fit
- Separate active, older, closed, and uncertain opportunities
- Maintain a history of discovered and applied jobs
- Prevent applications without explicit authorization

## Candidate Profile

- Target profile: Entry-level Data Engineer / Software Engineer
- Experience: Approximately 0–1 year
- Preferred locations: India and remote
- Availability: Within 15 days
- Primary skills:
  - Python
  - SQL
  - Apache Airflow
  - ETL and data pipelines
  - BigQuery
  - Snowflake
  - Databricks
  - GCP and AWS
  - Data migration
  - PostgreSQL and MySQL
  - Docker and Git

## Target Roles

### Primary Roles

- Data Engineer
- Junior Data Engineer
- Associate Data Engineer
- Cloud Data Engineer
- ETL Engineer
- Data Pipeline Engineer
- Big Data Engineer
- Data Migration Engineer
- Data Quality Engineer
- Analytics Engineer
- Data Platform Engineer

### Related Roles

- Data Analyst
- BI Developer
- SQL Developer
- Database Developer
- Cloud Engineer — Data Track
- Python Backend Developer
- Software Engineer
- Associate Software Engineer

## Search Priorities

The search follows this source order:

1. LinkedIn
2. Naukri
3. Official company career pages and ATS platforms
4. Employee or alumni referrals
5. Cutshort, Wellfound, Instahyre, and Hirist
6. Other approved job platforms only when necessary

Generic aggregators, scraped listings, repost-only websites, and untrusted sources are excluded unless an official company listing can be verified.

## Freshness Rules

- Jobs posted within the last 7 days are preferred.
- Jobs posted 8–14 days ago may be included if still active.
- Jobs older than 14 days are excluded by default.
- Closed, expired, removed, or “no longer accepting applications” listings are not included in the active results.
- Recently closed but highly relevant roles may be listed separately as contact opportunities.

## Requested Job Counts

A command such as:

```text
search 20 jobs
````

means that 20 valid and relevant jobs should be collected when sufficient results are available.

The search should continue through:

- Additional result pages
- Multiple role families
- Multiple Indian locations
- Remote opportunities
- Approved job platforms

The system must not fill the result with duplicates, stale jobs, unrelated roles, or unverified listings.

If fewer than the requested number are available, the result should clearly explain the coverage gap.

## Deduplication

Jobs are considered duplicates when they have the same:

- Job ID
- Canonical application URL
- Clearly identical requisition

Company name and job title alone are not enough to mark a listing as a duplicate because companies may have multiple openings for the same role.

## Job Status Categories

Search results are grouped into:

- Fresh Active
- Active — Older
- Closed — Contact Opportunity
- Rejected
- Uncertain

Each job should include, when available:

- Company
- Job title
- Location
- Source
- Posted date
- Verification date
- Job ID
- Application URL
- Experience requirement
- Matching skills
- Fit score
- Competition indicators
- Rejection reason, if excluded

## Safety Rules

Finding jobs does not mean applying to them.

Applications require an explicit command such as:

```
Apply to job 3
```

or:

```
Apply to the Fresh Active jobs
```

The system must not:

- Apply automatically
- Upload a resume without permission
- Enter personal information without permission
- Fabricate skills, experience, education, or certifications
- Submit applications to closed or suspicious listings
- Send mass messages
- Expose private contact information

## Workspace Files

| File | Purpose |
|---|---|
| `00_JOB_SEARCH_OS.md` | Main search workflow and operating rules |
| `01_PROFILE.md` | Candidate profile, skills, experience, and preferences |
| `02_TARGET_ROLES.md` | Target roles, role tiers, and fit-scoring rules |
| `03_SEARCH_QUERIES.md` | Search queries and role-family combinations |
| `04_COMPANY_TARGETS.md` | Target companies |
| `06_APPLICATION_RULES.md` | Application safety and authorization rules |
| `07_RESUME_MAP.md` | Resume selection guidance |
| `08_SEARCH_LOG.md` | Search history, job records, duplicates, and application status |

## Example Commands

### Search

```
search 20 jobs
search 10 fresh Data Engineer jobs
search 20 jobs across India
search 15 remote data engineering jobs
search 20 jobs from LinkedIn and Naukri first
search 20 jobs posted within the last 7 days
```

### Read-Only Mode

```
Search 20 jobs in read-only mode. Do not edit files.
```

```
Inspect the search results, but do not change any files.
```

### Debugging

```
Debug the last search and explain why fewer jobs were returned.
```

```
Show all excluded jobs and the reason for exclusion.
```

```
Show which pages, platforms, and locations were searched.
```

### Applications

```
Search only. Do not apply.
```

```
Prepare applications for jobs 1, 3, and 5, but do not submit.
```

```
Apply only to job 2 after showing me the final application.
```

## Privacy Notice

This workspace may contain personal profile information, resume references, job history, and application records.

Before making the repository public:

- Remove phone numbers and personal email addresses.
- Review `08_SEARCH_LOG.md`.
- Remove private recruiter or contact information.
- Do not commit resumes unless intentionally shared.
- Do not commit passwords, cookies, API keys, or browser session data.
- Consider keeping the repository private.

## Limitations

Job availability, posting dates, application status, and platform search results can change frequently.

The system reports only what can be verified during each search session. It does not guarantee that every available job is discovered or that an application will receive a response.


```
Before making the GitHub repository public, review `01_PROFILE.md` and `08_SEARCH_LOG.md` because they contain personal and historical job-search information.
```
