# /contact - Find Alumni and Draft Connection Invites

`$ARGUMENTS` is a company name. Find Santa Clara University alumni working there, and draft a short LinkedIn connection invite for each one. Goal: warm introductions that can lead to a referral.

## Step 1: Candidate background

Read `.claude/skills/job-application-assistant/01-candidate-profile.md` for identity and background to draw the "summary of me" from (name, school, major, relevant experience).

## Step 2: Find alumni

**Only surface people in Rayhan's actual target roles** - read the Career Goals / target roles from `01-candidate-profile.md` (currently: Software Engineer, Data Engineer, AI Engineer / Member of Technical Staff, Product Manager). Sales, growth, account management, marketing, and other non-target functions are out of scope even if the person is a confirmed SCU alum at the company - skip them rather than including them to pad the count.

LinkedIn profile pages are login-walled and not reliably fetchable - use WebSearch (not bulk scraping) to surface public, indexed profiles, running one search per target role rather than one generic search:

- `site:linkedin.com/in "Santa Clara University" "<company>" software engineer`
- `site:linkedin.com/in "Santa Clara University" "<company>" data engineer`
- `site:linkedin.com/in "Santa Clara University" "<company>" "machine learning" OR "AI engineer"`
- `site:linkedin.com/in "Santa Clara University" "<company>" product manager`

For every candidate that surfaces, independently verify with a second, more targeted search (`"<name>" "<company>" "Santa Clara University" linkedin`) before including them - the broad `site:` search produces false positives (wrong school, wrong company, or a role that turns out to be outside the target list once the full snippet is read). Also confirm they are **currently** at the company, not a past employee, and **located in the United States** - drop anyone based outside the US (a search snippet naming a non-US city, or a profile explicitly located abroad, disqualifies them). Drop anyone who doesn't verify on any of these criteria rather than guessing.

Collect up to 5 distinct, verified, currently-employed, US-based, target-role people: name, current title, location, and LinkedIn URL. This is the primary tier and the bar stays strict - never relax SCU verification, current employment, or US location to fill it.

**If the primary tier comes up short of 5**, fill the remaining slots from a secondary tier: confirmed SCU alumni, currently employed at the company, specifically **located in the Bay Area** - role can be outside the target list for this tier only (location is the relaxed criterion, not verification or employment status). Search `site:linkedin.com/in "Santa Clara University" "<company>"` (no role term) and check locations for Bay Area matches among people not already collected. Label these clearly as secondary/location-based fill in the output, separate from the primary target-role tier.

**If primary + secondary combined still fall short of 4**, open a third tier: confirmed SCU alumni, currently employed at the company, located anywhere on the **West Coast** (CA, OR, or WA - not just Bay Area). Role can still be outside the target list, same as the secondary tier. SCU verification and current employment stay non-negotiable in every tier - only the geography keeps widening. Label these clearly as third-tier/West-Coast fill, separate from the other two.

**4 is the floor to aim for across all three tiers combined.** Only report fewer than 4 if West Coast candidates genuinely can't be found either - state plainly which searches came up empty at each tier.

**Stay within LinkedIn's personal-use norms**: a handful of targeted lookups per company, not bulk collection. Don't retry aggressively against login walls.

## Step 3: Draft the invite

For each alum, draft a LinkedIn connection note:
- **Hard limit: under 300 characters** (LinkedIn's actual connection-note cap). Count every draft and trim until it's under.
- Include: a one-line summary of who you are (name, school, relevant background), why you're reaching out (shared SCU connection + genuine interest in their team/role/company), and one specific, real detail to connect on (drawn from what's actually visible about them - their role, team, or the company's work - never invented).
- Tone: warm, brief, no direct "give me a referral" ask - that's the longer-game goal, not the opening line. A natural, low-pressure note gets a reply; a transactional one doesn't.
- Never fabricate details about the alum that weren't actually found - if little is visible beyond their name/title, keep the note more general rather than inventing shared interests.

## Step 4: Output

Write to `contacts/<company>.md`:

```markdown
# Alumni Outreach - <Company>

## <Name> - <Title> (<Location>)
LinkedIn: <url>
**Invite draft (<char count>/300):**
> <invite text>

## <Name> - <Title> (<Location>)
...
```

Print the same summary in the response.
