# /email - Cold Outreach Email to a Former Employee

`$ARGUMENTS` is formatted exactly like this:

```
Target company: <company name>

Profile:
<the text of a former employee's profile page, already open/rendered>
```

This command drafts one outreach email to a **former employee of the
target company** - someone who used to work there but has since moved on.
It's built specifically for the "you used to work somewhere I really want
to work, would you help me get in" ask, which only makes sense once
someone has already left - it is not for current employees or executives.

The subject line, greeting, opening intro paragraph, closing paragraph
(the connection ask, with the target company's name substituted in), and
sign-off are all fixed and assembled separately by the calling tool for
consistency across every email - **do not draft any of those, and do not
print them in your output.** You only draft the one body paragraph in
between (Step 4 below).

## Step 1: Identify the recipient

Find their first name as it appears on the profile - that's all the
calling tool needs to build the greeting.

## Step 2: Your experience (pick exactly one)

Choose whichever ONE of these five best relates to something in their
profile or the target company's domain. Never mention more than one; never
combine two. Never alter these numbers or facts - they're fixed, not
adjustable per recipient.

1. **Software Engineer Intern, Dimensional Fund Advisors** (Austin, TX,
   Jun-Aug 2026) - resolved 44,900+ data mismatches and built dashboards to
   monitor data quality and warehouse performance; prototyped a workflow to
   automate data ingestion, transformation, and delivery at a firm with
   $1T+ AUM.
2. **Founder and CEO, FreshFrosh LLC** (Fremont, CA, Jun 2023-Dec 2025) -
   built a gamified recruitment platform using AI agents and challenges to
   match students with startups; onboarded 28 startups and 400+ students
   through career fairs and pitch competitions.
3. **Software Engineer Intern, Amotions AI** (Burlingame, CA, Jul-Sep
   2025) - designed 145+ prompt variations for LLM-based coaching
   interactions, improving response consistency; built a recommendation
   system personalizing training for 30+ pilot customers.
4. **Information Technology Intern, DPlace AI** (San Jose, CA, Jun-Sep
   2024) - reviewed pitch decks with the CEO and recommended key changes
   that helped secure six-figure investments; fixed software issues for 14
   team members, saving 56 hours/week and boosting productivity 27%.
5. **Data Science Intern, Charlee AI** (Pleasanton, CA, Jun-Aug 2023) -
   analyzed and categorized insurance claims data; built software to track
   claim expiration dates by state-specific statute.

## Step 3: Confirm they're a former employee of the target company

Parse their profile for confirmation they used to work at the target
company (not currently there). Note the role and dates if the profile
gives them, but a bare headline mention (e.g. "Ex-Plaid, Docker,
Cloudflare") is enough to confirm former employment on its own, even
without a role or dates - don't require more than that to proceed. Only
say so plainly in the output and skip drafting if the profile doesn't
show former employment at all (e.g. they're actually still there, or the
target company never appears).

Also note anything else genuine and specific about their time there -
what they worked on, any project or team mentioned - for Step 4. If
nothing beyond the bare confirmation is available, that's fine; Step 4
has a fallback for that case.

## Step 4: Draft the body paragraph

**Exactly one paragraph.** This is the only part of the email you write -
it sits between a fixed intro paragraph (name, school, a personal story)
and a fixed closing paragraph (the connection ask, naming the target
company, plus the resume/GitHub mention) that are both assembled
separately; you don't draft either of those, and this paragraph should not
duplicate anything from them.

Weave these three things together in roughly equal proportion - don't let
any one of them dominate the paragraph or crowd the others out:
1. One specific, genuine detail about them - not a recap of their career
   since leaving. They already know their own career path; don't narrate
   it back to them (no "you went from X to Y to Z", no tour of everywhere
   they've been). Prefer, in order:
   - a concrete detail about what they worked on or built while at the
     target company specifically, if the profile shows one (a role, a
     project, a team), or
   - if the profile only confirms they used to work there without
     describing what they did (e.g. just a headline like "Ex-Plaid,
     Docker, Cloudflare"), their current professional focus or area of
     expertise instead - stated as what they do, not as a sequence of
     where they've done it.
2. One sentence connecting your own background: the one experience from
   Step 2, stated concretely (real numbers, real company name).
3. A genuine, specific reason you want to work at the target company -
   never generic enthusiasm ("genuinely love," "dream company," "amazing
   place to work," "incredible opportunity") without something real behind
   it. Ground it in one of:
   - a concrete, accurate detail of what the company actually builds or
     the problem it works on, stated specifically enough that it couldn't
     apply to just any company in the space - only if you're genuinely
     confident it's correct, or
   - the real overlap between the company's domain and the experience you
     named in Step 2 - the specific kind of problem that experience and
     this company both involve.
   If you're not confident about a specific claim regarding the company
   itself, use the second option rather than risk stating something
   inaccurate - never fall back to vague praise instead.

Target 90-100 words total. Each of the three points above is one clause
or one short sentence, not a paragraph of its own.

**Rules:**
- Sound like a specific real person wrote this about this specific person -
  never a template with the name swapped in for the parts you control. If
  this paragraph would read identically for a different recipient with the
  details changed, rewrite it.
- Plain text only. No markdown of any kind - no `**bold**`, no asterisks,
  no bullet characters, no headers. This gets displayed and copied as-is,
  not rendered, so any markdown syntax shows up as literal stray
  characters in the final email.
- No em-dashes. Use commas or periods.
- No cliches: cut "passionate about," "would love to connect," "great to
  e-meet," "leverage my skills," "reaching out because," "I hope this email
  finds you well," "hit the ground running," "genuinely love," "dream
  company/job," "amazing company," "incredible opportunity."
- Never fabricate anything about them that isn't visible in the provided
  profile text, and never alter the numbers or facts in the five
  experiences from Step 2. Never state a "fact" about the target company
  you're not genuinely confident is accurate.
- Warm, direct, genuinely personal - contractions are fine.

## Step 5: Output

Print which experience you picked and why, then confirmation of the
former-employee relationship you found (or, if you couldn't confirm one,
say so instead of the line below), then the recipient's first name, then
the body paragraph only. **Plain text throughout, including these
reasoning lines - no `**bold**` or other markdown anywhere in the
output.**

```
Experience used: <# and title> - because <the overlap>
Former employee confirmed: <role and dates if known, otherwise "role/dates not shown"> at <target company>
Recipient: <their first name>

Middle:
<the body paragraph from Step 4>
```
