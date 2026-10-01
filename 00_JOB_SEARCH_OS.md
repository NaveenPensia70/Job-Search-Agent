# JOB SEARCH OPERATING SYSTEM — OPTIMIZED

**Objective**: Find highest-fit entry-level data/software roles in India/remote with zero duplicate applications.

**Profile**: Naveen Pensia | 0.5 yrs data engineering | Pune | Immediate joiner
**Target**: T1 data roles, entry-level (0–1 yr preferred); T2 closely related data roles and flexible 0–2/1–2 year roles may be used to complete a requested result set.
**Primary sources**: LinkedIn and Naukri first, followed by the employer's official ATS/careers page for verification and application. Referrals are supplemental. **Platforms**: Use the connected browser first; use public web search only as fallback. Secondary discovery sources are used only after LinkedIn/Naukri coverage is exhausted. Generic job aggregators and untrusted repost sites are excluded.
**Authority files**: 01_PROFILE.md (skills), 02_TARGET_ROLES.md (tier definitions + scoring), 08_SEARCH_LOG.md (job records)

---

## WORKFLOW

```
DISCOVER (LinkedIn/platforms/communities) → LOCATE OFFICIAL ATS → VERIFY LIVE STATUS
→ DEDUPE (vs. log) → FILTER → SCORE → RANK → APPLY/REFERRAL QUEUE → APPLY → LOG OUTCOME
```

## BROWSER SESSION ACCESS

- Earlier tab observations are history only. They never prove that Chrome is accessible in a later task.
- A live Chrome connection is proven only when the current task can select the supported Chrome extension and retrieve the user's currently open tabs. Record this check before searching LinkedIn or Naukri.
- **Connected**: claim only the necessary existing LinkedIn/Naukri tab, verify its title and URL, then use the normal visible search controls. Do not alter the user's profile, saved jobs, applications, or account settings during a search-only request.
- **Not connected**: continue with official career pages and public sources, but label the run `Public fallback — no authenticated LinkedIn/Naukri session coverage`. Browser unavailability must not be described as full platform coverage and must not prevent the rest of the source ladder from being searched.
- Workspace Markdown cannot install, enable, or repair the Chrome extension. If Chrome cannot be selected, use the Codex desktop app's **Settings → Computer use** to check that Chrome shows **Manage**, that its browser toggle is on, and that the extension is installed in the active Chrome profile. Start a new Codex/Work chat with Chrome selected after changing the setup.
---

## EXECUTION RULES

### Search Phase
- **Use PRIMARY queries first** (Q1–Q4 in 03_SEARCH_QUERIES.md)
- **Run a live browser-connection check before using the connected Chrome LinkedIn and Naukri tabs; use them first only when that check succeeds**
- **Source order is mandatory**: authenticated LinkedIn, authenticated Naukri, official employer ATS/careers pages, referrals, then approved secondary discovery platforms. Do not start with generic web search or job aggregators when LinkedIn/Naukri are available.
- **Requested-count mode**: when the user says `search N jobs`, `run N job search`, or gives another number, treat N as the target number of jobs to collect, not merely a maximum. Continue through all configured pages, locations, role families, and approved sources until N qualifying jobs are collected or the configured coverage is exhausted. Never pad the result with closed, stale, duplicate, unrelated, or unverified listings; if N cannot be reached, report the coverage gap.
- Search every relevant result page for each role-family/geography combination; do not stop after a few duplicates.
- Continue through pagination until the platform reports no next page or all remaining results are clearly outside the filters.
- Search all T1 and T2 role families across Pune, Bengaluru, Hyderabad, Gurugram/Gurgaon, Mumbai, Chennai, Delhi NCR, India Remote, and other configured Indian geographies before concluding that coverage is low.
- Use T3/T4 searches when the target is still not reached, then continue until the full filtered result set is reviewed.
- Record page range reviewed, total results, duplicates, access issues, freshness, active-status evidence, and competition signals.
- Record browser capability status separately from tab history: `Browser tool available`, `Browser tool unavailable`, or `Browser tool not required`.
- Use this source ladder: LinkedIn, Naukri, official employer ATS/careers page, employee/alumni referral, then Cutshort/Wellfound/Instahyre/Hirist, Reddit/X leads, and finally Indeed/Foundit/Internshala for supplemental volume.
- Keep discovery source and canonical application source as separate fields so source conversion can be measured.

### Freshness and Active-Response Verification
- Prefer jobs posted within the last 7 days and label them **Fresh Active**.
- Jobs posted 8–14 days ago may be reported only when the listing is visibly live and accepting applications; label them **Active — older**.
- Jobs posted more than 14 days ago are excluded by default. Include older jobs only when the user explicitly asks for older postings.
- Never present a job as actionable when it says closed, expired, no longer accepting applications, removed, or when the Apply action fails.
- Record exact posted date, last-verified date, closing date if shown, and evidence of an active application path.
- A search-result snippet, “actively hiring” badge, repost, mirror, or conflicting date is not sufficient verification. Open the original application page and confirm a reliable posted date and job-specific active Apply/Submit action. If dates conflict, use the older defensible date and downgrade or exclude the listing. If the page returns 404/410, says closed/expired, redirects only to a generic jobs page, or the application action cannot be confirmed, classify it as **Closed** or **Uncertain**—never as active.
- Do not use generic job aggregators or scraped/reposted sites such as MailerMen as canonical sources. They may only reveal a company or requisition; the official employer page must then be located and verified. If no official page exists, exclude the job from the active shortlist.
- For approved third-party boards, prefer the employer’s job-specific ATS page. Record the verification date and exact evidence.
- Track visible competition indicators such as applicant count, “over 100 applicants,” or click/apply counts. Use them for ranking and warning labels, not as a reason to hide a relevant active job.
- A requested number is a collection target. Return exactly that many when the configured searches produce enough valid jobs, ranked by freshness first and profile fit second. If the target remains unreachable after exhaustive coverage, report the smaller verified count and explain the coverage gap.

### Recently Closed but Highly Relevant
- If a highly relevant job closed within the previous 7 days, place it in a separate **Closed — contact opportunity** section rather than the active shortlist.
- Provide a recruiter/HR contact only when it is publicly listed on the job page, official company careers page, official company LinkedIn page, or a clearly public recruiter profile.
- Record the contact’s name, role, public channel, source URL, and date verified. Never infer an email address or expose private contact details.
- If no public authority contact is available, say so and provide the official careers/requisition link instead.

### Deduplication Phase
- Compare every job against 08_SEARCH_LOG.md before reporting
- Treat as duplicate only when the same job ID, canonical URL, or clearly identical requisition is found. A different requisition ID, posting date, or location is a new job even when the company and title match.
- Use company + normalized title only as a review warning, never as an automatic duplicate decision.
- **Do not repeat** jobs marked: Shortlisted, Applied, Rejected, Closed, or previously shown

### Filtering Phase
- **Auto-reject if**:
  - Requires 2+ years AND no "flexible on experience" language
  - Missing mandatory core skill (Python, SQL, or ETL/pipeline experience)
  - Purely non-technical (sales, telemarketing, customer support, data entry)
  - Posted >90 days ago (stale), unless the listing is explicitly marked actively open and the employer page still accepts applications
- **Auto-accept to shortlist if**:
  - T1 role + Fit ≥ 80 (see 02_TARGET_ROLES.md SCORING FORMULA)

### Scoring Phase
- **Calculate fit using weighted formula** in 02_TARGET_ROLES.md
- Never manually estimate fit; always compute

### Ranking Phase
- **Rank by fit descending** within each tier
- Report all qualifying matches, grouped as "Fresh Active", "Active — older", "Closed — contact opportunity", and "Rejected/uncertain".
- Do not promise a fixed number of active opportunities when verification produces fewer matches. Report the verified active count and separately list closed/uncertain candidates.
- Within each freshness group, rank by fit, then lower visible competition. Place a newer posting ahead of an older posting when fit is reasonably comparable.

### Application Phase
- **Apply only when explicitly authorized** ("Apply to [X]")
- When an official ATS exists, apply there first and then send a targeted referral/recruiter message containing the exact job ID.
- Use resume mapping (02_TARGET_ROLES.md RESUME MAP)
- Never fabricate experience, skills, projects, or education
- Log: Date, company, title, resume version, application status

### Conversion Improvement Loop
- Track verified-active rate, applications, referrals requested/received, recruiter replies, interviews, offers, and rejection reasons by discovery source.
- Review results after 20 verified applications or four weeks and shift effort toward sources producing interviews, not merely listings.
- Keep a direct-ATS control group so referral and platform performance can be compared fairly.

---

## EFFICIENCY RULES

- **Read only files needed for current task**
- **Reuse unchanged queries** — do not repeat searches
- **Consolidate results by batch** — report multiple jobs once, ranked
- **No process guarantees 100% coverage**; state source limitations and dates
- **Coverage report**: For each run, log every query/geography/page range, total discovered, deduplicated, qualifying new jobs, stale/closed jobs, uncertain jobs, and coverage gaps

---

## JOB STATUS TRACKING

```
New → Shortlisted → Applied → Interview → Offer
      ↓
   Rejected (do not revisit unless materially changed)
```

---

## KEY REFERENCES
- Skills & experience → **01_PROFILE.md**
- Role tiers + scoring formula → **02_TARGET_ROLES.md**
- Search queries (optimized) → **03_SEARCH_QUERIES.md**
- Application rules + resume mapping → **06_APPLICATION_RULES.md** + **02_TARGET_ROLES.md**
- Job inventory + dedup log → **08_SEARCH_LOG.md**

## RESEARCH-BASED OPERATING NOTES — 2026-08-28

Recent India-focused discussions describe a crowded entry-level market, inflated experience requirements, and better outcomes from targeted applications plus referrals than from mass applying. Recent user reports particularly favor Cutshort for response quality, while Naukri is described as higher-volume but noisier. These reports guide experiments; Naveen’s own conversion data remains the authority.
