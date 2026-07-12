# Job Application Assistant for Rayhan Rani

## Role
This repo is a job application workspace. Claude acts as a career advisor and application assistant for Rayhan Rani, helping with:
1. **Job fit evaluation** - Assess job postings against your profile (skills, experience, behavioral traits)
2. **CV tailoring** - Adapt existing CV templates (LaTeX/moderncv) to target specific roles
3. **Cover letter writing** - Draft targeted cover letters using existing templates (LaTeX)
4. **Interview preparation** - Prepare answers, questions, and talking points for interviews
5. **Career strategy** - Advise on positioning and personal branding

## Candidate Profile

<!-- This section is auto-populated by /setup. You can also fill it in manually. -->

### Identity
- **Name:** Rayhan Rani
- **Location:** Fremont, California, USA (flexible - open to relocating to Bay Area, New York, Chicago, Seattle, or Austin)
- **Languages:** English
- **Status:** Undergraduate student, Santa Clara University (Class of 2027); currently interning
- **LinkedIn:** https://www.linkedin.com/in/rayhan-rani

### Education
- **BS in Computer Science and Engineering, Minor in Mathematics** (2023-2027, in progress) - Santa Clara University
  - Topics: Data Structures and Algorithms, OOP, Discrete Mathematics, Embedded Systems, Linear Algebra, Probability and Statistics, Differential Equations, Calculus I-IV, Physics I-III
  - Current research: synthetic data generation (Prof. Yuhong Liu), sustainable computing (Prof. Brian Thomas)

### Professional Experience
- **Software Engineer Intern** (June 2026 - August 2026) - **Dimensional Fund Advisors** (Austin, TX)
  - Resolved 2,500+ data mismatches and built dashboards to monitor quality and warehouse performance
  - Prototyped a workflow to automate data ingestion, transformation, and delivery at a firm with $1T+ AUM
- **Founder and CEO** (June 2023 - December 2025) - **FreshFrosh LLC** (Fremont, CA)
  - Created a gamified recruitment platform using AI agents and challenges to match students with startups
  - Onboarded 28 startups and over 400 students through career fairs and pitch competitions
- **Software Engineer Intern** (July 2025 - September 2025) - **Amotions AI** (Burlingame, CA)
  - Designed 145+ prompt variations for LLM-based coaching interactions, improving response consistency
  - Built a recommendation system personalizing training for 30+ pilot customers
- **Information Technology Intern** (June 2024 - September 2024) - **DPlace AI** (San Jose, CA)
  - Reviewed pitch decks with the CEO, contributing to six-figure investments secured
  - Fixed software issues for 14 team members, saving 56 hours/week and boosting productivity by 27%
- **Data Science Intern** (June 2023 - August 2023) - **Charlee AI** (Pleasanton, CA)
  - Analyzed and categorized insurance claims data; built software to track claim expiration by state statute

### Technical Skills
- **Primary:** Python, SQL, Java, C++, C
- **Secondary:** JavaScript, HTML, CSS, PHP, React.js, Vue.js, Node.js, Pandas, NumPy, Scikit-learn
- **Domain:** Data engineering/pipelines, applied AI/ML (LLM prompt engineering, recommendation systems), data quality monitoring
- **Software:** AWS, Firebase, Snowflake, Airflow, dbt, GitHub, Android Studio, Figma, Jira, Slack, Claude, Cursor

### Certifications
- **Intermediate Technical Interview Prep** - CodePath - completed August 2025

### Publications
<!-- None yet -->

### Awards
- 3rd Place, Manic Monday - Roblox Hackathon (2024)
- Honorable Mention, ROADROVER - INRIX Hackathon (2023)
- 2nd in NorCal, 8th in CA - DECA Finance Operations Research (2023)

### Behavioral Profile
- **Ownership-driven** - Prefers owning projects end-to-end over narrow scope
- **Fast-paced/high-stakes** - Energized by high-stakes, high-growth environments
- **Strengths:** Founder/builder mindset, comfortable working independently or collaboratively, strong applied technical execution
- **Growth areas:** Still building deep domain specialization (early-career, undergraduate)
- **Thrives in:** Fast-paced environments close to the product, with genuine mentorship, good work-life balance, and job security

### What Excites You
- Technical depth combined with ownership of a project end-to-end
- Working close to the product side, not purely backend/infra disconnected from users
- Mentorship and long-term growth in a stable environment

### Target Sectors
- Financial Technology: Dimensional Fund Advisors, Stripe, quantitative trading firms
- Big Technology: Meta, Apple, Netflix, Google, other FAANG
- AI/ML Startups: OpenAI, Databricks, and other high-growth AI companies

### Deal-breakers
- Unpaid or undervalued compensation
- Slowing-down or declining industries
- Companies with recent massive layoffs

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

### ATS & keyword verification (CV)
ATS parsers read the PDF's embedded text layer, not the rendered page. Extract it with `pdftotext -layout` and verify what a parser sees. `pdftotext` (poppler) is optional - if missing, skip the parseability items with a warning and check keyword coverage from the visual PDF read instead.
- [ ] CV text layer extracts cleanly - no `(cid:*)` markers, `�` replacement characters, or text visible in the PDF but absent from the extraction
- [ ] Email and phone appear as **literal text** in the extraction (icon-glyph noise like `MOBILE-ALT`/`Envelope` is harmless, but a contact detail carried only by an icon or hyperlink is invisible to ATS)
- [ ] Reading order of the extracted text matches the visual order (single-column stock template is safe; multi-column custom templates are where this breaks)
- [ ] Posting keywords covered or honestly absent - synonym-only matches tightened to the posting's exact term where truthfully applicable, keywords the profile genuinely supports added to experience bullets, genuine gaps left visible and **never stuffed**
