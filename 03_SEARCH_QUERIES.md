# OPTIMIZED SEARCH QUERIES

## QUERY STRATEGY

**Principle**: Reduce unnecessary overlap while maintaining exhaustive coverage of the configured role families, geographies, and result pages.

**Execution order**:
1. Primary queries (Q1–Q4) in each priority geography → highest yield
2. Search all configured priority geographies before concluding that T1/T2 results are low
3. Add secondary queries (Q5–Q6) only if Primary exhausted for role family
4. Skip T3/T4 queries only for a narrow T1/T2 search; a complete/bulk search must also execute the configured T3/T4 queries and review every page.

## USER REQUESTED COUNT

Interpret commands such as `search 20 jobs`, `run job search 10`, or `find 5 jobs` as a request to **collect exactly that many new, relevant, verified active jobs whenever exhaustive configured coverage provides enough valid results**.

- Search authenticated LinkedIn first, then authenticated Naukri, then official employer ATS pages.
- Use secondary platforms only when the primary sources produce fewer qualifying matches than requested.
- Keep searching until the requested count is reached or every configured source, page, location, and role-family query is exhausted.
- Never fill the requested number with duplicates, unrelated roles, jobs older than 14 days, closed jobs, aggregator-only listings, or uncertain application routes.
- If fewer jobs qualify after exhaustive coverage, return the actual count and state why the target was not reached.
- A bare `run job search` means use a default target of up to 10 new verified jobs, subject to the same quality rules.

**Coverage rule**:
- Before executing LinkedIn or Naukri queries, run the live Chrome-connection check in `00_JOB_SEARCH_OS.md`. Do not infer access from a previous run or a tab URL stored in the workspace.
- Do not stop because several results are duplicates or already logged.
- Review every page returned by the active filters until pagination ends or the platform clearly reports no more matching results; do not stop after the first page or after finding a few candidates.
- Keep a per-platform/per-query page cursor and result count so later runs can resume without silently skipping pages.
- A job is not excluded from the report merely because it has high competition; mark the competition signal instead.
- Discovery and application are separate: platform listings are discovery leads until the official job-specific application page is verified.
- After LinkedIn/Naukri discovery, perform a lightweight status check for each candidate and exclude anything marked closed, expired, removed, or no longer accepting applications. Use the official employer ATS/careers page when available for the application route; do not let an inaccessible ATS page alone discard a recent, clearly active platform listing. Only if the requested count is still unmet may you use Cutshort, Wellfound, Instahyre, Hirist, Reddit communities, X, Indeed, Foundit, Internshala, or another approved secondary source for discovery. Generic aggregators and scraped repost sites are excluded.

---

## PRIMARY QUERIES (High Yield, Execute First)

### Q1 — Core Data Engineer (Tier 1)

**LinkedIn**:
```
"Data Engineer" | location: {GEOGRAPHY}
"Junior Data Engineer" | location: {GEOGRAPHY}
```
**Note**: These 2 return ~95% overlap; run once, then filter by "Experience level" / "Entry-level"

**Naukri**:
```
Search: "Data Engineer"
Filters: Experience: 0-1 years, Location: {GEOGRAPHY}
```

**Yield**: Usually 20–50 results per geography. Stop only when the requested count is reached with verified, relevant, active jobs or when all filtered pages are exhausted.

---

### Q2 — Cloud Data Engineer (Tier 1)

**LinkedIn**:
```
"Data Engineer" AND ("BigQuery" OR "Snowflake" OR "Databricks" OR "GCP" OR "Cloud")
Location: {GEOGRAPHY}
```

**Naukri**:
```
Search: "Data Engineer" ("BigQuery" OR "Snowflake" OR "Databricks")
Filters: Experience: 0-1 years, Location: {GEOGRAPHY}
```

**Yield**: 10–25 jobs. Often overlaps Q1 by 40%; deduplicate before ranking.

---

### Q3 — ETL / Data Pipeline (Tier 1)

**LinkedIn**:
```
("ETL" OR "ETL Engineer" OR "Data Pipeline" OR "Data Pipeline Engineer")
Location: {GEOGRAPHY}
```

**Naukri**:
```
Search: "ETL" OR "Data Pipeline"
Filters: Experience: 0-1 years, Location: {GEOGRAPHY}
```

**Yield**: 5–20 jobs. High-relevance, low overlap with Q1/Q2.

---

### Q4 — Analytics Engineer (Tier 1 Technical)

**LinkedIn**:
```
"Analytics Engineer" OR "BI Developer" OR "Business Intelligence Engineer"
Location: {GEOGRAPHY}
**Important**: Filter descriptions for Python/SQL/Airflow/warehouse mentions; reject pure BI tool roles
```

**Naukri**:
```
Search: "Analytics Engineer"
Filters: Experience: 0-1 years, Location: {GEOGRAPHY}
```

**Yield**: 5–15 jobs. Medium-to-high relevance; some pure BI (Tableau-only) noise.

---

## SECONDARY QUERIES (Use Only If Primary < 5 Qualifying Jobs)

### Q5 — SQL + Python Developer (Data-Focused)

**LinkedIn**:
```
("SQL Developer" OR "Python Developer") AND ("data" OR "warehouse" OR "pipeline")
Location: {GEOGRAPHY}
**Important**: Reject non-data roles (backend-only, web dev)
```

**Naukri**:
```
Search: "SQL Developer" "Python"
Filters: Location: {GEOGRAPHY}
```

**Note**: High noise (catches backend roles); only run if Q1–Q4 exhausted.

**Yield**: 15–40 jobs, ~40% irrelevant.

---

### Q6 — Databricks Engineer (Tier 1 Specialized)

**LinkedIn**:
```
"Databricks" AND ("Engineer" OR "Developer" OR "Architect")
Location: {GEOGRAPHY}
```

**Naukri**:
```
Search: "Databricks" OR "Databricks Engineer"
Filters: Location: {GEOGRAPHY}
```

**Yield**: 2–8 jobs, very high relevance if found.

### Q9 — Data Migration / Data Operations (Tier 1 Specialized)

```
"Data Migration Engineer" OR "Data Operations Engineer" OR "Data Quality Engineer"
("Python" OR "SQL" OR "Airflow" OR "BigQuery" OR "Snowflake" OR "ETL")
Location: {GEOGRAPHY}
```

Use this because Naveen’s strongest evidence is migration, orchestration, validation, and warehouse work that may not appear under the exact “Data Engineer” title.

### Q10 — Data Platform / Warehouse Variants (Tier 1 Specialized)

```
("Data Platform Associate" OR "Junior Data Platform Engineer" OR "BigQuery Engineer" OR "Snowflake Engineer")
(Python OR SQL OR Airflow OR ETL OR migration)
Location: {GEOGRAPHY}
```

Use after Q1–Q4 across LinkedIn, ATS pages, Cutshort, and Wellfound. Deduplicate aggressively.

---

## TERTIARY QUERIES (Use Only If T1/T2 Coverage < 3 Qualifying Jobs)

### Q7 — Software Engineer Entry-Level (Tier 3 Fallback)

**LinkedIn**:
```
("Software Engineer" OR "Software Developer" OR "Backend Developer")
AND ("Python" OR "fresher" OR "0-1 years" OR "Associate")
Location: {GEOGRAPHY}
**Important**: Filter for Python/backend/cloud focus; reject frontend-only (React/Flutter)
```

**Naukri**:
```
Search: "Software Engineer" OR "Backend Developer"
Filters: Experience: 0-1 years, Location: {GEOGRAPHY}
```

**Yield**: 30–100 jobs, ~50% irrelevant (pure web dev, mobile).

---

### Q8 — Graduate / Associate Data Engineer (Tier 4 Opportunistic)

**LinkedIn**:
```
"Graduate" AND ("Data Engineer" OR "Software Engineer" OR "Technology Analyst")
Location: {GEOGRAPHY}
```

**Naukri**:
```
Search: "Graduate" "Data Engineer"
Filters: Experience: Fresher, Location: {GEOGRAPHY}
```

**Yield**: 5–20 jobs, variable quality.

---

## GEOGRAPHY PRIORITY & BATCHING

### Batch 1 (Priority A) — Execute First

```
☐ Pune (on-site preference)
☐ India Remote / Remote India / Work From Home India
```

**When to move to Batch 2**: After all Batch 1 result pages and all configured T1/T2 role families have been reviewed, regardless of how many qualifying jobs were found.

---

### Batch 2 (Priority B) — If Needed

```
☐ Bengaluru
☐ Hyderabad
```

**When to move to Batch 3**: After all Batch 1 and Batch 2 result pages and all configured T1/T2 role families have been reviewed.

---

### Batch 3 (Priority C) — Last Resort

```
☐ Mumbai
☐ Delhi NCR / Gurugram / Noida
☐ Chennai
☐ Ahmedabad
☐ Kolkata
```

**Stopping condition**: Search every configured city when the user requests a complete/bulk job search. Repetition is handled by deduplication, not by ending coverage early.

---

## SEARCH EXECUTION CHECKLIST

For each search run, complete this checklist before reporting:

```
SEARCH PHASE:
[ ] Q1 (Data Engineer) — Batch 1 geographies
[ ] Q2 (Cloud Data Engineer) — Batch 1 geographies
[ ] Q3 (ETL / Data Pipeline) — Batch 1 geographies
[ ] Q4 (Analytics Engineer) — Batch 1 geographies
[ ] Deduplicate Q1–Q4 results

[ ] Review all Batch 1 pages and record page ranges; do not stop based on a qualifying-job count.

[ ] Q1–Q4 — Batch 2 geographies (Bengaluru, Hyderabad)
[ ] Deduplicate against Batch 1

[ ] Review all Batch 2 pages and record page ranges; continue to secondary queries for complete coverage.

[ ] Q5 (SQL + Python data) — Batch 1 geographies
[ ] Q6 (Databricks) — Batch 1 geographies
[ ] Deduplicate

[ ] Review all Q5–Q6 pages; use Q7–Q8 when configured role coverage still has gaps.

[ ] Q7 (Software Engineer fresher) — all configured geographies for complete/bulk searches
[ ] Q8 (Graduate Data Engineer) — all configured geographies for complete/bulk searches

COVERAGE REPORT:
[ ] Record date, platforms searched, queries executed, geographies covered
[ ] Page ranges reviewed per query/platform: ___
[ ] Fresh active: ___ | Active older: ___ | Closed-contact: ___ | Uncertain: ___
[ ] Total discovered: ___ | Deduplicated: ___ | New qualifying: ___ | Rejected/stale: ___
[ ] Upload new jobs to 08_SEARCH_LOG.md
```

---

## PLATFORM-SPECIFIC NOTES

### LinkedIn
- Use "Title" + "Keywords" + "Location" fields
- Filter by "Experience level" when available (Fresher, Entry-level, Associate)
- Note job post date, closing status, and applicant/competition indicators; do not skip solely due to competition
- Click "Company" to verify legitimacy (avoid fake/spam postings)
- Verify that Apply/Easy Apply is still present and functional before classifying a role as active

### Official employer ATS / career pages
- Use LinkedIn, Cutshort, Wellfound, Reddit, and X to discover the company and job ID.
- Search the employer’s own careers page for the same requisition.
- Apply there when the job-specific page shows an active Apply/Submit action.
- Record discovery source and canonical application source separately.

### Cutshort, Wellfound, Instahyre, and Hirist
- Use these only after LinkedIn and Naukri, and only to discover employers/requisitions that can be verified on an official job page.
- Use Wellfound for startup roles; use Instahyre and Hirist for curated Indian technology hiring.
- Verify current status and experience requirements on the employer page.
- Treat old reposts, generic pages, and missing Apply actions as Uncertain.

### Generic aggregators and repost sites
- Do not search or report generic aggregators as a primary source.
- Do not treat “actively hiring,” salary widgets, repost dates, or aggregate result pages as proof that a job is current.
- A listing discovered there can be retained only if the matching official employer job page is found, exposes the posted/closing information, and has a working Apply/Submit action.
- If the official page cannot be found, classify the lead as Uncertain and exclude it from the requested job count.

### Reddit and X
- Search recent posts for exact job IDs, referral offers, and hiring-manager signals.
- Never treat “DM to apply,” a shortened link, or a job-alert account as proof that a role is open.
- Verify the employer’s official page before reporting or applying.

### Naukri
- Use "Designation" field (pre-filtered by role)
- Set "Work Experience" filter to "0–2 years"
- Check "Job Post Date" in results (sort by newest)
- Confirm the listing is open and the Apply action is available; record applicant/competition signals when visible
- Naukri often shows your profile fit % (>60% = likely qualified)
- Use "Save job" feature; sync with this log weekly

### Other Sources (Secondary Only)
- **Indeed**: Use when LinkedIn/Naukri results plateau
- **Internshala**: Useful for graduate/entry-level tech roles
- **Angel List**: Startup data roles (usually smaller salary bands)
- **Company career pages**: Direct apply if company is on watchlist (04_COMPANY_TARGETS.md)

---

## TOKEN EFFICIENCY NOTES

**Original queries had 40–50% redundancy due to:**
- Q1: 4 title variants (collapsed to 2 primary, filtered by experience level)
- Q2/Q3: Overlapping cloud warehouses (merged into single query)
- Q5: Vague "Python Developer" catches non-data roles (now requires "data" keyword)
- Q7: No experience filter (added experience level constraints)

**Optimized reduction**: ~40–50% fewer queries, same or better coverage.

---

## DO NOT REPEAT QUERIES

**Once a query is executed for a geography in the current search run:**
- Do not repeat the same query unnecessarily, but do complete every result page in that query.
- Do not assume results remain fresh for 7 days; re-verify active status and posted/closing dates each time a job is reported. Prefer the newest seven-day results and exclude aggregator-only or date-conflicted listings.
- Record in 08_SEARCH_LOG.md: query, geography, page range, result count, fresh/active/closed counts, and last verification time.

---

## CUSTOM QUERIES (Save Here When Useful)

Add new queries below only if they consistently return high-quality results (Fit ≥ 75):

```
[Save as Q9, Q10, etc. when discovered]
```
