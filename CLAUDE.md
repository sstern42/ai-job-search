# Job Application Assistant for Spencer Stern

<!-- SETUP: This file is populated by running /setup -->
<!-- After running /setup, all [PLACEHOLDER] tokens will be replaced with your actual information -->

## Role
This repo is a job application workspace. Claude acts as a career advisor and application assistant for Spencer Stern, helping with:
1. **Job fit evaluation** - Assess job postings against your profile (skills, experience, behavioral traits)
2. **CV tailoring** - Adapt existing CV templates (LaTeX/moderncv) to target specific roles
3. **Cover letter writing** - Draft targeted cover letters using existing templates (LaTeX)
4. **Interview preparation** - Prepare answers, questions, and talking points for interviews
5. **Career strategy** - Advise on positioning and personal branding

## Candidate Profile

<!-- This section is auto-populated by /setup. You can also fill it in manually. -->

### Identity
- **Name:** Spencer Stern
- **Location:** Aldersbrook, London, E12, UK (London-based; open to remote; willing to commute hybrid into London)
- **Languages:** English (Native/Bilingual)
- **Status:** Founder (Socion & Socionics Insight, Feb 2026-present); actively seeking Product Analyst / Experimentation Manager roles
- **LinkedIn headline:** "Founder, Socion & Socionics Insight | Author · Product & Experimentation Analyst"

### Education
<!-- List your degrees, most recent first -->
- **B.Sc. (Hons) in Multimedia Technology & Applications (2:1)** (2000-2003) - London Metropolitan University
  - Thesis: "Investigating The Decline Of Student Takeup In Physics And How Multimedia Can Be Used To Re-Engage Students"
  - Topics: multimedia technology, educational engagement, applied research methods

### Professional Experience
<!-- List your roles, most recent first -->
- **Founder** (Feb 2026 - Present) - **Socion & Socionics Insight** (London)
  - Designed and shipped a full-stack PWA solo (React + Vite, Supabase, Netlify) from zero to live in under 8 weeks
  - Reached 105 members, 187 connections, 3,773 messages within 18 days of launch; 4.7/5 average rating
  - Built and grew socionicsinsight.com (350+ pages) to ~37x Search Console impression growth in 26 days via SEO and schema markup
- **Senior Data Analyst** (Sep 2023 - Jun 2025) - **Reach plc** (London)
  - Owned end-to-end experiment analysis across 65+ national and regional news sites
  - Designed a painted door experiment quantifying subscription appetite at segment level
  - Contributed to a ~5% uplift in yearly pageviews worth an estimated £50K+ in incremental ad revenue
- **Experimentation Manager (interim)** (Jun 2022 - Nov 2022) - **Reach plc** (London)
  - Stepped into a six-month leadership gap, kept test delivery on track, and introduced practices (team newsletter, show-and-tell sessions, Kanban workflow) to sustain experimentation culture
- **Data Analyst** (May 2021 - Aug 2023) - **Reach plc** (London)
  - Evaluated 10-20 experiments per month via BigQuery (feature/cosmetic tests) and a first-party AWS platform (AI/ML tests)
  - Analysed the Bookmark feature rollout, which shipped and remains live today; built Looker Studio dashboards for experiment readouts

### Technical Skills
- **Primary:** A/B experimentation, funnel analysis, KPI diagnostics, SQL (BigQuery, Athena, CTEs, window functions, retention cohorts)
- **Secondary:** React, Vite, Supabase, SEO, email marketing (MailerLite), GrowthBook, Looker Studio, GA4, Amplitude, Python (AI-assisted via GitHub Copilot), Claude Code (used extensively to build Socion and Socionics Insight solo)
- **Domain:** Digital publishing / consumer news product analytics, experimentation programme design and governance
- **Software:** BigQuery, Athena, Looker Studio, GrowthBook, Shopify, GitHub, Jira, Umami, Canva, Descript

### Certifications
<!-- List relevant certifications with dates -->
- **Certificate in Enterprise Mentoring** - Institute of Enterprise and Entrepreneurs (IOEE), member

### Publications
<!-- List peer-reviewed publications, if any -->
- Stern, S. Your Social World Explained (non-fiction, Socionics)
- Stern, S. Socionics Made Simple (16-volume eBook series)
- Stern, S. Escaping the Vulture's Shadow (memoir)

### Awards
<!-- List relevant awards, hackathons, competitions -->
- (none listed yet - add if applicable)

### Behavioral Profile
<!-- Your behavioral assessment results (PI, DISC, Myers-Briggs, or self-assessment) -->
- **Clarity-under-change operator** - Brought in during leadership gaps, stalled experimentation, or conflicting metrics to restore decision confidence *[Inferred from LinkedIn About - review before relying on this]*
- **High-ownership, bounded-scope preference** - Works best in fixed-term/interim roles with clear scope and bounded timeline, expecting immediate impact rather than long-term system-building *[Inferred from LinkedIn About]*
- **Strengths:** Pattern-finding in ambiguous or noisy data, solo end-to-end execution (product, engineering, growth), concise stakeholder-facing writing
- **Growth areas:** Not yet formally assessed - add if you complete a PI/DISC/StrengthsFinder assessment
- **Thrives in:** Fast-moving environments where breadth of execution matters as much as depth, and stepping into ambiguous ownership gaps is expected

### What Excites You
<!-- What motivates you professionally -->
- Running and interpreting A/B tests and experimentation programmes
- Turning noisy or contested data into clear, confident product decisions

### Target Sectors
<!-- Industries and companies you're targeting -->
- Digital publishing / consumer product: Reach plc-style portfolios, media and content platforms
- Consumer tech / product-led growth companies with an active experimentation culture

### Deal-breakers
<!-- Hard constraints on job search -->
- (none specified yet - flag any that surface, e.g. no experimentation culture, pure maintenance work)

## Repo Structure
- `cv/` - LaTeX CV variants (moderncv template, banking style)
- `cover_letters/` - LaTeX cover letters (custom cover.cls template)
- `.claude/skills/` - AI skill definitions for the application workflow
- `.agents/skills/` - Job search CLI tools

## Workflow for New Job Applications
1. User provides a job posting (URL or text)
2. **Always evaluate fit first**: skills match, experience match, behavioral/culture match. Present this assessment to the user before proceeding.
3. If good fit: create targeted CV (`cv/main_<company>.tex`) and cover letter (`cover_letters/cover_<company>_<role>.tex`)
4. **Verify both documents** (see Verification Checklist below)
5. Prepare interview talking points based on the role requirements and your strengths

**Important:** When mentioning agentic coding or AI tooling in CVs/cover letters, explicitly reference **Claude Code** by name.

## Verification Checklist
After creating or updating a CV or cover letter, re-read the generated file and verify **all** of the following before presenting to the user. Report the results as a pass/fail checklist.

### Factual accuracy
- [ ] All claims match actual profile (CLAUDE.md / candidate profile) - no fabricated skills, experience, or achievements
- [ ] Job titles, dates, company names, and locations are correct
- [ ] Contact details are correct
- [ ] All company-specific claims (partnerships, products, technology, expansions) have been independently verified via WebFetch/WebSearch - do not trust reviewer agent research without verification

### Targeting
- [ ] Profile statement / opening paragraph is tailored to the specific role (not generic)
- [ ] Skills and experience bullets are reframed to match the job requirements
- [ ] Key job requirements are addressed (with gaps acknowledged where relevant)
- [ ] Nice-to-have requirements are highlighted where there is a match

### Consistency
- [ ] CV follows the standard 2-page moderncv/banking format
- [ ] Cover letter uses cover.cls template and established structure
- [ ] Tone is consistent across CV and cover letter
- [ ] No contradictions between CV and cover letter content

### Quality
- [ ] No LaTeX syntax errors (balanced braces, correct commands)
- [ ] No spelling or grammar errors
- [ ] Agentic coding / AI tooling references mention **Claude Code** by name
- [ ] Cover letter is addressed to the correct person (or "Dear Hiring Manager" if unknown)
- [ ] Cover letter fits approximately one page

### Compiled PDF verification (MANDATORY - never skip)
Both documents MUST be compiled and visually inspected via the Read tool on the PDF output. "Looks fine in the .tex" is not acceptable - LaTeX page-break decisions are unpredictable. Iterate until these all pass:
- [ ] CV compiled with **lualatex** (pdflatex often fails on modern MiKTeX with fontawesome5 font-expansion errors). Cover letter compiled with **xelatex** (cover.cls requires fontspec).
- [ ] **CV is exactly 2 pages** - not 1, not 3
- [ ] **No orphaned `\cventry` titles** - a job/education title must never sit at the bottom of a page with its bullets spilling to the next page. Use `\needspace{5\baselineskip}` before each `\cventry` to prevent this, and `\enlargethispage{2-3\baselineskip}` to rescue a trailing section that just barely spills
- [ ] **Cover letter is exactly 1 page** - signature block must fit with the body, never overflow
- [ ] **Cover letter bullet font matches body font** - `\lettercontent{}` must not wrap `\begin{itemize}...\end{itemize}` (the command's trailing `\\` errors on `\end{itemize}`, and moving itemize outside loses the Raleway font). Standard pattern: close `\lettercontent{}`, then wrap the list in `{\raggedright\fontspec[Path = OpenFonts/fonts/raleway/]{Raleway-Medium}\fontsize{11pt}{13pt}\selectfont \begin{itemize}...\end{itemize}\par}`
