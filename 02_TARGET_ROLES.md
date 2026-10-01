# TARGET ROLES & SCORING — OPTIMIZED

## ROLE TIERS (Single Source of Truth)

### T1 — Primary Target (Highest Priority)

**Core data engineering roles matching profile expertise:**

- Data Engineer
- Junior Data Engineer
- Associate Data Engineer
- Data Engineering Associate
- Cloud Data Engineer (BigQuery, GCP, Snowflake, Databricks)
- ETL Developer / ETL Engineer
- Data Pipeline Engineer
- Big Data Engineer
- Analytics Engineer (only if heavily technical: Airflow, SQL, Databricks, warehouse)
- Data Migration Engineer
- Data Operations Engineer (pipeline/platform focus)
- Data Quality Engineer (Python/SQL/ETL focus)
- Data Platform Associate / Junior Data Platform Engineer
- BigQuery Engineer / Snowflake Engineer (entry-level or flexible experience)

**Score bonus**: +15 points if role includes Airflow orchestration or cloud migration

---

### T2 — Strong Adjacent (Secondary Priority)

**Related roles with meaningful overlap:**

- Data Analyst (with Python/SQL + data pipeline/warehouse experience)
- BI Analyst / BI Developer (with Python/SQL + cloud warehouse)
- SQL Developer (with Python and data focus)
- Business Intelligence Engineer (technical, not just Tableau/Power BI)
- Database Developer (with Python or cloud warehouse)
- Cloud Engineer — Data track (GCP/AWS data services)
- Data Platform Engineer (warehouse/lakehouse focus)
- Junior Analytics Engineer (SQL/Python + analytics tools)
- ETL Support Engineer / BI-ETL Engineer (technical pipeline support, not helpdesk)
- Cloud Data Operations Analyst (GCP/AWS data-services focus)

**Score modifier**: -10 points (lower priority than T1, but still strong candidates)

---

### T3 — Software Fallback (Use if T1/T2 insufficient)

**Software roles compatible with data/backend focus:**

- Software Engineer (with Python focus OR backend/cloud OR data platform listed)
- Software Developer (same as above)
- Backend Developer — Python (REST APIs, databases, cloud)
- Full Stack Developer (Python/Node backend + React frontend)
- Associate Software Engineer (entry-level, 0–1 yr)
- Python Developer (non-data: backend, scripting, infrastructure)
- Node.js Developer (backend focus)

**Score modifier**: -20 points (secondary skill overlap only; less ideal fit)

**Warning**: Reject if advertised as "customer-facing" or requires heavy React/Flutter.

---

### T4 — Opportunistic (Borderline/Last Resort)

Only search if T1–T3 coverage is insufficient (<5 qualifying jobs per month):

- Graduate Data Engineer / Graduate Software Engineer
- Technology Analyst (data/technical track only; reject if non-technical)
- Associate Software Engineer (generic, no technical focus listed)
- Junior Developer (generic title; evaluate responsibilities)
- Technical Consultant — Data (if early-career track)

**Score modifier**: -25 points (lower relevance; often mixed signals)

---

## SCORING FORMULA

### Base Score Calculation

```
FIT_SCORE = (EXP_MATCH × 40) + (SKILLS_MATCH × 35) + (LOCATION_MATCH × 15) + (COMPANY_BONUS × 10)

Thresholds:
- FIT ≥ 85: Top Match (apply priority)
- FIT 75–84: Additional Relevant (apply after top matches)
- FIT 70–74: Acceptable (apply if low volume)
- FIT < 70: Borderline (shortlist only if no alternatives)
- FIT < 50: Reject
```

---

### Component Scoring

#### 1. EXPERIENCE MATCH (Max 40 points)

| Requirement | Match | Score | Notes |
|---|---|---|---|
| "0–1 years" OR "fresher" OR "entry-level" | Perfect | +40 | Ideal |
| "1–2 years" | Marginal | +30 | You're at 0.5 yrs; borderline |
| "2–3 years" | Weak | +15 | Only if "flexible on experience" stated |
| "3+ years" | Mismatch | 0 | Auto-reject unless strong override reason |
| "Experience not specified" | Neutral | +20 | Assume mid-level; check description |
| Requires ONLY entry-level + your core skills | Excellent | +45 | Bonus: rare and perfect |

**Modifiers**:
- If role includes "Immediate joiner" or "notice period flexible": +5
- If company emphasizes "training" or "mentorship": +5

---

#### 2. SKILLS MATCH (Max 35 points)

**Method**: Count matching skills from PROFILE against job requirements.

| Skill Category | Your Skills | Match = ? | Points/Match |
|---|---|---|---|
| **CORE (Must-have)** | Python, SQL, ETL/Airflow/pipeline | 1 pt each | +20 total |
| **PRIMARY** | GCP, BigQuery, Snowflake, Databricks, AWS | 0.5 pt each | +10 total |
| **HIGH** | BigLake, Cloud Composer, PostgreSQL, Docker, Git | 0.25 pt each | +3 total |
| **SECONDARY** | React, Node.js, MongoDB, Flutter, Java, C++ | 0.1 pt each | +1 total |

**Penalties**:
- If job requires 1+ core skills you DON'T have: -15 (auto-reject likely)
- If job requires specific certification you lack: -5

**Calculation**:
```
SKILLS_MATCH = (core_found + primary_found + high_found + secondary_found)
Normalize to max 35 points:
  - 5+ skills found = +35
  - 4 skills = +30
  - 3 skills = +25
  - 2 skills = +20
  - 1 skill = +10
  - 0 core skills found = -50 (auto-reject)
```

---

#### 3. LOCATION MATCH (Max 15 points)

| Preference | Match | Points |
|---|---|---|
| Pune (on-site or hybrid) | Exact | +15 |
| India (any city, on-site) | Nearby/Feasible | +10 |
| India Remote (WFH/distributed) | Exact | +15 |
| International Remote | Possible | +12 |
| Requires relocation outside India | Unfeasible | -10 (auto-reject unless overriding factor) |

---

#### 4. COMPANY BONUS (Max 10 points)

| Company Type | Bonus |
|---|---|
| FAANG / Tier-1 tech (Google, Amazon, Microsoft, Meta, Apple) | +10 |
| Strong data engineering company (Databricks, dbt, Stitch, Fivetran, Informatica) | +8 |
| Indian tech leader (TCS, Infosys, HCL, Accenture, Flipkart, Amazon India) | +6 |
| Funded startup (Series B+, known investors) | +5 |
| Mid-size tech company with clear product | +3 |
| Consultancy / services company | +1 |
| Unknown or low online presence | 0 |

---

## RESUME MAPPING

### R1 — Data Engineering (Primary)

**When to use**:
- T1 roles: Data Engineer, Junior/Associate Data Engineer, ETL Developer, Cloud Data Engineer
- T2 roles: Analytics Engineer, Data Analyst (Python/SQL focus), BI Developer (technical)

**Key emphasis**: Python, SQL, Airflow, GCP, BigQuery, Snowflake, 3.71 TB migration project

**File**: naveen_pensia_data_engineer_v1.pdf (or latest version)

---

### R2 — Software Engineering

**When to use**:
- T3 roles: Software Engineer, Backend Developer, Full Stack Developer
- T4 roles: Associate Software Engineer, Graduate Software Engineer (if software track)

**Key emphasis**: Python, JavaScript/React, Node.js, REST APIs, databases, Git, Docker, full-stack projects (HostelTrade, Tutora)

**File**: naveen_pensia_fullstack_v2.pdf (or latest version)

---

### R3 — Analytics / BI

**When to use**:
- T2 roles: Data Analyst, BI Analyst, Business Intelligence Engineer
- T2 roles: SQL Developer, Database Developer
- T2 roles: Cloud Engineer — Data track

**Key emphasis**: SQL, Python, data quality, data validation, Databricks, BigQuery, Snowflake, analytics projects

**File**: naveen_pensia_analytics_v1.pdf (or latest version)

---

### Edge Case Mapping

| Role | Use Resume | Reason |
|---|---|---|
| Data Platform Engineer | R1 | Platform/infrastructure focus; data prioritized |
| Cloud Engineer (Data track) | R1 | Data services emphasis |
| Database Developer | R1 or R3 | If warehouse: R1; if OLTP/MySQL: R3 |
| Technology Analyst | R1 (if data) / R2 (if software) | Check job description for track |
| Graduate [Data/Software] Engineer | R1 or R2 | Match to title's focus; R1 for data |

---

## REJECTION CRITERIA (Auto-Skip)

Auto-reject (score 0) if job requires:

1. **Experience mismatch**: "3+ years required" AND no "flexible" language
2. **Missing core skill**: Requires Python/SQL/ETL but you have zero evidence in PROFILE
3. **Wrong function**: Pure sales, telemarketing, customer support, data entry, non-technical operations
4. **Stale listing**: Posted >90 days ago
5. **Relocation mandatory** outside India (unless explicitly willing)
6. **Visa sponsorship** not available (unless specified available)

---

## POSITIVE SIGNALS (Bonus +5 to +10)

- "Immediate joiner" or "notice period flexible"
- "Training" or "mentorship" mentioned
- "Entry-level" or "0–1 year" explicitly stated
- Company uses Airflow, dbt, or modern data stack
- Role includes "mentor" or "learn" in description
- Flexible on tools/tech stack
- "We'll teach you X" (willingness to train)

---

## COVERAGE REQUIREMENT

Search ALL role families below per geography, in priority order:

1. **T1 Core** (Data Engineer, Junior Data Engineer, Cloud Data Engineer, ETL)
2. **T1 Cloud** (BigQuery, Snowflake, Databricks variants)
3. **T2 Adjacent** (Analytics Engineer, BI Developer, SQL Developer)
4. **T3 Software** (only if T1/T2 < 5 qualifying jobs)
5. **T4 Opportunistic** (only if T1/T2/T3 < 3 qualifying jobs)

---

## NOTES

- Evaluate responsibilities, not title alone
- A role can be reclassified based on actual requirements (e.g., "Data Analyst" with Airflow → T1 candidate)
- Use scoring formula consistently; never estimate fit manually
- If formula gives FIT < 50, do not apply (avoid low-probability spray-and-pray)

## PROFILE POSITIONING FOR SEARCH AND OUTREACH

- **Primary data track**: Entry-level Data Engineer with production experience in Python, SQL, Airflow, GCP, BigQuery, Snowflake, ETL, and a 3.71 TB Snowflake-to-BigQuery migration.
- **Cloud/migration track**: Junior Cloud Data Engineer focused on BigQuery, Cloud Composer/Airflow, GCS, Snowflake migration, partitioning, and data validation.
- **Backend fallback**: Python/backend engineer with REST APIs, PostgreSQL/MySQL/MongoDB, Node.js, Docker, Git, and React project experience.

Always include truthful availability: **Available to join within 15 days**.

Do not combine all three tracks in one resume or outreach message. Use one focused positioning statement per application track.
