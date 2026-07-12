# /cover - Draft a Cover Letter

`$ARGUMENTS` is a job posting (URL or pasted text). Draft a plain-text cover letter using the fixed template below, based on the candidate's real profile. No LaTeX, no fabrication.

## Step 1: Candidate background

Read `.claude/skills/job-application-assistant/01-candidate-profile.md` for identity, education, experience, skills, and projects. This is the only source of truth for what the candidate can honestly claim.

## Step 2: Parse the posting

Fetch/read the posting (WebFetch, or curl if the page is JS-rendered and WebFetch only returns the shell). Extract: company name, role title, named contact (if any), and the 3-5 requirements that matter most.

For the "why this company" bracket, verify any specific claim about the company via WebFetch/WebSearch first - never state a fact about the company you haven't actually confirmed.

## Step 3: Draft, using this exact template

Fill every bracket; keep the surrounding sentences exactly as written since this is the candidate's established voice.

```
Dear [Company] Hiring Team,

I'm writing to apply for the [Role Title] position at [Company]. As a Computer Science and Engineering student at Santa Clara University with a minor in Mathematics, I'm drawn to [specific thing about the role/team/mission that genuinely excites you, grounded in the posting], and I want to build my career at the intersection of [relevant technical area, e.g. data systems and AI].

This past summer, as a Software Engineer Intern at Dimensional Fund Advisors, I built a Python pipeline that parsed thousands of YAML-based dbt schema files across a large data warehouse, resolving more than 2,500 data mismatches for a firm managing over $1 trillion in assets. [Optional: one sentence connecting this directly to something in the job posting.] That work required exactly the kind of technical rigor and comfort with ambiguity that [Company/role] demands.

[Second experience paragraph - swap in whichever is most relevant to this posting: Amotions AI's LLM/recommendation work, FreshFrosh's founder experience, or coursework. Pick 1-2 experiences that map most directly onto the job's stated requirements.] My coursework in Data Structures and Algorithms, Discrete Mathematics, and Probability and Statistics has given me a strong foundation, and I'm comfortable working across Python, C++, Java, and SQL.

[Company] stands out to me because of [one specific, genuine, verified reason tied to their culture, mission, or technical approach - avoid generic praise]. I'd welcome the opportunity to bring my [1-2 real traits, e.g. data engineering background and comfort with ambiguity] to your team.

Thank you for considering my application. I look forward to the opportunity to discuss how I can contribute.

Sincerely,
Rayhan Rani
```

**Rules:**
- No em-dashes. Use commas or periods.
- No cliches: cut "passionate about," "hit the ground running," "great fit," "leverage my skills."
- Every claim must be backed by something real in the profile. If a requirement is a genuine gap, don't paper over it.
- Target 250-300 words total. Never exceed 350.
- Match the language of the posting.

## Step 4: Output

Write the plain-text letter to `covers/CL_<company>.txt` (create the folder if needed, lowercase company name, underscores for spaces) and print it in the response.
