# APPLICATION RULES — OPTIMIZED

**Authority**: 01_PROFILE.md (your facts), 02_TARGET_ROLES.md (scoring + resume mapping), 08_SEARCH_LOG.md (what you've applied to)

---

## FUNDAMENTAL RULE

**Finding jobs ≠ permission to apply.**

- `"Run job search"` or `"Find jobs"` = search, dedupe, filter, score, rank. **Do NOT apply.**
- `"Apply to [list]"` or `"Apply to top N jobs"` = apply ONLY when explicitly authorized.

---

## APPLICATION PRIORITY

**Apply in this order**:

1. **Tier 1 roles** with Fit ≥ 85 (use R1 resume)
2. **Tier 1 roles** with Fit 75–84 (use R1 resume)
3. **Tier 2 roles** with Fit ≥ 80 (use R1 or R3 per resume map)
4. **Tier 2 roles** with Fit 70–79 (use R1 or R3)
5. **Tier 3 roles** ONLY if T1/T2 volume <3 shortlisted jobs (use R2)

**Batch strategy**: Build the complete qualifying application queue first. When the user explicitly authorizes bulk applications, process the whole authorized queue in manageable batches while recording each submission; never silently limit the search to the top 3–5 jobs.

## SOURCE HIERARCHY AND APPLICATION SEQUENCE

1. Official employer career page / ATS — canonical application route
2. Employee or alumni referral with an exact job ID
3. LinkedIn — discovery, recruiter outreach, and employee discovery
4. Cutshort — curated startup/product technology roles
5. Wellfound — startup roles
6. Instahyre and Hirist — secondary curated technology sources
7. Reddit and X — leads and referrals only
8. Naukri, Indeed, Foundit, and Internshala — supplemental volume and recruiter inbound

When an official ATS exists, apply there first and then send the targeted referral/recruiter message. If only a verified platform route exists, use that route and record it as canonical.

Browser capability note: Markdown rules cannot create or repair Chrome access. Before claiming LinkedIn or Naukri session coverage, use the live connection check in `00_JOB_SEARCH_OS.md` and record the result. If the connection is unavailable, continue the official/public source search as `Public fallback — no authenticated LinkedIn/Naukri session coverage`; do not claim that the user’s authenticated session was inspected or stop all other source searches.

## REFERRAL / RECRUITER OUTREACH RULE

For each strong verified role, prepare one short message containing company, exact job ID, role, matching stack, location preference, and truthful availability within 15 days. Do not send mass messages, resumes without context, or requests to “search for any job.” A referral enhances a specific application; it does not replace requisition verification.

## LISTING STATUS CHECK BEFORE APPLYING

- Confirm the job was posted recently enough for the user’s stated freshness preference.
- Confirm the listing still shows a live Apply/Easy Apply/application route and is not closed, expired, removed, or no longer accepting responses.
- A search-engine result, “actively hiring” label, or generic company careers page does not prove that a specific requisition is open. The job-specific application page must be checked on the verification date.
- If the job-specific URL returns 404/410, redirects to a generic jobs page, or its Apply/Submit action cannot be confirmed, do not present it as actionable; mark it **Uncertain** or **Closed** in `08_SEARCH_LOG.md`.
- If a role is discovered through Reddit, X, LinkedIn content, Cutshort, Wellfound, Instahyre, Hirist, or another mirror, record both `Discovery Source` and `Canonical Application Source`; only the canonical source determines active status.
- Record posted date, closing date, last-verified date, and visible applicant/competition signals in `08_SEARCH_LOG.md`.
- If a highly relevant role closed within the previous 7 days, do not apply through a dead link. Move it to **Closed — contact opportunity** and look for a publicly listed recruiter/HR authority.

## CLOSED-RECENTLY CONTACT WORKFLOW

- Search only public sources for the hiring authority: the closed job page, official employer careers page, official company LinkedIn page, or a public recruiter profile.
- Record public name, title, channel, source URL, and verification date.
- Never guess email formats, scrape private contact details, or present an unverified person as HR.
- If no public recruiter/HR contact exists, report: “No public hiring contact found,” and retain the official requisition URL for monitoring.

## BULK SEARCH AND APPLICATION QUEUE

- A complete search means reporting every unique qualifying active role found across all configured pages, role families, locations, and both primary platforms—not just the highest-ranked example.
- Separate the queue into Fresh Active, Active — older, Closed — contact opportunity, and Uncertain.
- Deduplicate by job ID/URL first, then company + normalized title + location, including cross-platform duplicates.
- Do not apply automatically from a search command. Accept explicit commands such as “Apply to all Fresh Active matches” or “Apply to these listed jobs.”

---

## DO NOT APPLY IF

**Auto-reject application if ANY of these conditions exist**:

1. **Experience requirement fundamentally incompatible**
   - Requires 3+ years AND no "flexible" language
   - You have <0.5 years in that specific domain AND role shows 2+ years required
   - **Exception**: If role says "We'll train you" or emphasizes mentorship

2. **Major required skills are absent** (from your PROFILE)
   - Requires Python + SQL + you're missing both
   - Requires specific tool (e.g., "Informatica mandatory") + you have no exp
   - Requires certification (AWS, GCP, Databricks) you don't have AND role won't train
   - **Exception**: If job says "Willing to train" or role is entry-level

3. **Unrelated to data/software domains**
   - Pure sales, telemarketing, customer support, data entry
   - Non-technical operations, HR, finance, administrative
   - If in doubt: Check job description for technical responsibilities

4. **Application requires fabricated information**
   - Never claim certification you don't have (AWS, GCP, Databricks, etc.)
   - Never claim project you haven't built
   - Never inflated previous experience timeline
   - Never false employment dates
   - See TRUTH RULE below

5. **Suspicious or low-quality**
   - Unknown company with no online presence
   - Job posting has obvious spelling errors, vague terms, or sketchy language
   - Salary is commission-only or suspiciously low (<₹3L for entry-level)
   - Company name looks like phishing (e.g., "Amazen" instead of "Amazon")
   - Listing is closed, expired, removed, or no longer accepting applications

---

## RESUME SELECTION RULES

**Use mapping from 02_TARGET_ROLES.md**:

| Job Type | Resume | Version |
|---|---|---|
| **T1 Data roles** (Data Engineer, Junior/Associate, Cloud, ETL, Analytics Engineer) | **R1 Data Engineering** | Latest (v1) |
| **T2 Analytics/BI/SQL** (BI Developer, Data Analyst, SQL Dev, Analytics Engineer) | **R1 or R3** | Check role description; if Python/Airflow emphasis → R1; if pure SQL/BI → R3 |
| **T2 Cloud Data/Platform** (Cloud Engineer data track, Data Platform Engineer) | **R1 Data Engineering** | Latest (v1) |
| **T3 Software** (Backend, Full Stack, Python Developer) | **R2 Software Engineering** | Latest (v2) |
| **T4 Graduate/Associate** | **R1 (if data track)** or **R2 (if software)** | Check job for tech focus |

**Custom selection rule**: If job emphasizes 60%+ Python/SQL/Airflow/warehouse → use R1. If 60%+ JavaScript/React/APIs → use R2.

**Resume files** (confirm these exist and are current):
- R1: `naveen_pensia_data_engineer_v1.pdf`
- R2: `naveen_pensia_fullstack_v2.pdf`
- R3: `naveen_pensia_analytics_v1.pdf`

---

## APPLICATION CUSTOMIZATION STRATEGY

**Rule**: Only customize if ROI is high. Otherwise, reuse template answers.

### High-Value Applications (Customize)
- Tier 1, Fit ≥ 85
- Company is on watchlist (04_COMPANY_TARGETS.md Priority A)
- Application requires essay/detailed answers
- **Customization effort**: 20–30 min per application

### Medium-Value Applications (Light Customize)
- Tier 1, Fit 75–84
- T2 roles with strong fit
- Use template + 1–2 custom points per question
- **Effort**: 5–10 min per application

### Low-Value Applications (Template Only)
- Tier 2, Fit 70–74
- Tier 3, any fit
- Copy-paste same answers across roles
- **Effort**: 2–3 min per application

---

## APPLICATION QUESTIONS — ANSWER SOURCES

**Never fabricate**. Use only PROFILE + existing resumes.

### Common Question: "Why are you interested in this role?"

**Template Answer** (customize company name + 1–2 specific details):

> I'm an entry-level Data Engineer with 6 months of hands-on experience building Airflow-orchestrated ETL pipelines for large-scale data migrations (3.71 TB Snowflake to BigQuery). I'm drawn to [Company] because [1 specific detail: e.g., "you use modern data stack—Airflow, dbt, Snowflake", or "your data platform team is building X public tech", or "your engineering blog on Y impressed me"]. I want to deepen my expertise in [specific skill gap or focus area], and this role seems like the ideal next step.

---

### Common Question: "Tell us about a project you're proud of."

**Answer Options** (from PROFILE projects):

1. **Snowflake → BigQuery Migration** (strongest for data roles)
   - Migrated 3.71 TB Snowflake → BigQuery Iceberg format
   - Built Airflow DAGs for orchestration, hash-based partitioning, parallel export
   - Implemented AI-assisted data validation using Python scripts
   - Result: Zero data loss, 40% query performance improvement

2. **Metadata-Driven Airflow Pipeline** (if technical depth needed)
   - Built reusable Airflow DAGs that dynamically adjust concurrency based on load
   - Used Snowflake schema metadata to auto-discover tables
   - Reduced pipeline failures by 60% through better error handling
   - Leveraged Python for custom transformations

3. **React Component Library** (for software/full-stack roles)
   - Built 30+ reusable React components (buttons, forms, modals, data tables)
   - Created CRUD modules + REST APIs in Node.js/Express
   - Integrated MongoDB for persistence
   - Deployed using Docker and Git workflows

4. **Full-Stack Projects** (Tutora, HostelTrade)
   - **Tutora**: React + Node.js backend + MongoDB
   - **HostelTrade**: Flutter app + Firebase + Supabase

---

### Common Question: "What's your strongest technical skill?"

**Answer** (Tailor by role):

- **For Data roles**: "Python and SQL. I've built 15+ production ETL pipelines using Python for transformation logic and SQL for data quality checks. I'm most confident with Airflow orchestration and Snowflake/BigQuery."
  
- **For Software roles**: "Python backend development and REST API design. I've built scalable APIs in Node.js/Express and have deep experience with databases (PostgreSQL, MongoDB). I'm also comfortable with frontend React development."

---

### Common Question: "Why should we hire you as a fresher/entry-level?"

**Answer Template**:

> While I'm early in my career, I bring production-grade experience: I've shipped real ETL systems that handle TB-scale data migrations, solved complex technical problems (e.g., partitioning strategies, data reconciliation), and learned fast in a professional setting [Jan–Aug 2026 at Onix]. I'm eager to grow, I ask thoughtful questions, and I don't shy away from jumping into unfamiliar tech stacks. My foundation in Python, SQL, and cloud is solid, so I can be productive from day one in [specific role] while continuing to deepen expertise under your team's guidance.

---

### Common Question: "Do you have experience with [specific tool: Databricks / BigQuery / Airflow / etc.]?"

**Answer Truthfully**:

| Tool | Your Level | Answer |
|---|---|---|
| Airflow | Strong | "Yes, I've built production Airflow DAGs with dynamic concurrency, error handling, and metadata-driven configs." |
| Python | Strong | "Yes, 6+ months building transformation logic, data validation scripts, and APIs in production." |
| SQL | Strong | "Yes, I write optimized queries for Snowflake and BigQuery, including window functions and performance tuning." |
| BigQuery | Strong | "Yes, I migrated 3.71 TB Snowflake data to BigQuery Iceberg format and built ETL pipelines using Cloud Composer." |
| Snowflake | Strong | "Yes, I designed schemas, wrote partition strategies, and executed large-scale migrations." |
| Databricks | Moderate | "I have foundational knowledge (Spark transformations, Delta Lake) but limited production experience. I'm eager to deepen this." |
| GCP | Strong | "Yes, I've used GCP services (BigQuery, Cloud Composer, GCS Storage Transfer Service) extensively in my data work." |
| Informatica | Limited/None | "I haven't used Informatica but I'm comfortable learning new ETL platforms. My Python/SQL foundation transfers well." |
| React | Moderate | "Yes, I've built 30+ reusable React components and two full-stack projects. I'm solid on component state and hooks." |
| Terraform / IaC | Limited/None | "I have basic experience with Docker and Git; I'm comfortable learning infrastructure-as-code tools." |

**Do NOT claim experience you lack.** Instead, emphasize adjacent skills and willingness to learn.

---

## LOGGING APPLICATIONS

**After each application, update 08_SEARCH_LOG.md**:

```
| Date Applied | Platform | Company | Title | Location | Job ID/URL | Resume Version | Status | Interview Date |
| 2026-08-28 | LinkedIn | [Company] | Data Engineer | Pune | [URL] | R1_v1 | Applied | — |
```

Record within same day application is sent. Add follow-up date 7 days later if no response.

---

## INTERVIEW FOLLOW-UP

**After interview scheduled**:
- Update 08_SEARCH_LOG.md with interview date and time
- Note any custom questions asked (for future reference)
- Send brief thank-you email within 24 hours (optional; check company culture)
- Prepare: Review company + role description again; be ready to discuss your migration project

---

## TRUTH RULE (Critical)

**You must never fabricate**:
- Experience (employment dates, project involvement, technical contributions)
- Skills or certifications (AWS Cloud Graduate is real; AWS Solutions Architect is not)
- Projects (HostelTrade, Tutora are real; don't invent others)
- Education (MCA 2024–2026 is real; don't claim early graduation)
- Achievements (3.71 TB migration is real; don't inflate to 10 TB)
- Responsibilities (if you co-built with others, say so; don't claim solo ownership)
- Salary history or current compensation

**Penalty for dishonesty**: Loss of reputation, job termination, legal consequences.

**Better approach**: Highlight what you DID do. Highlight eagerness to learn what you haven't. Be honest about gaps.

---

## REJECTION FEEDBACK (Optional)

If a company offers rejection feedback, **do not argue**. Instead:
- Acknowledge the gap (e.g., "I see, I lack experience with Spark")
- Ask if you can apply again after gaining that experience
- Update 08_SEARCH_LOG.md with reason: "Rejected — missing Spark experience; revisit in 3 months"
- Move on to next application

---

## BATCH APPLICATION CHECKLIST

Before hitting "Submit" on each batch (3–5 jobs):

```
[ ] Job company ≠ on exclusion list?
[ ] Fit ≥ 70 (per 02_TARGET_ROLES.md formula)?
[ ] Experience requirement met or "flexible" stated?
[ ] Core required skills match your PROFILE?
[ ] Resume selected per mapping (R1/R2/R3)?
[ ] Customization done (if high-value job)?
[ ] No fabricated information in answers?
[ ] Application template reviewed for errors/typos?
[ ] Job logged in 08_SEARCH_LOG.md?
```

**After submission**: Wait 48–72 hours before next batch. Avoid spam perception.

**Outcome measurement**: Record discovery source, official ATS used, referral requested/received, recruiter contacted, response, interview call, and rejection reason. Review after 20 verified applications or four weeks and shift effort toward sources producing interviews.
