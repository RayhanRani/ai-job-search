# /email - Draft a Cold Outreach Email From an Open Profile

`$ARGUMENTS` is the text of a person's profile page that is already
open/rendered (name, current role/company, background/experience,
education, boards, investments) - not a company name, not a search. This
command drafts one outreach email to this specific person and does not
look anyone up; it works only from the profile text given.

This is for general networking, driven by genuine curiosity about someone's
background and career path - not outreach tied to a specific job or
application, and never a referral ask.

## Step 1: Your identity

Read `.claude/skills/job-application-assistant/01-candidate-profile.md` for
name, school, and major only. Do not draw experience bullets from that
file.

State the major as **Computer Science and Engineering** (or, if brevity
calls for it, the compact form **CS+Engineering**) - never shorten it to
just "Computer Science," since that drops the Engineering half of the
actual degree.

## Step 2: Your experience (pick exactly one)

Read `.claude/skills/job-application-assistant/02-network-experience-menu.md`
for the fixed list of five experiences. Choose whichever ONE best relates to
something in their profile. Never mention more than one; never combine two.

## Step 3: Read their profile and gauge seniority

Parse the provided profile text for their name, current role/title and
company, and their **past**: prior roles, career transitions, where they
studied, notable projects, boards, investments, or how they got to where
they are now.

Classify their seniority from the title text:

- **Executive/Board tier**: Founder, CEO, President, C-level (CTO, COO,
  CFO, CMO, etc.), Board Member, General Partner/Partner, General Counsel.
- **Everyone else**: Director, VP, Manager, individual contributor, or a
  former employee (regardless of the title they held there).

This changes the email's approach in Step 5 - it does not change whether
you write one (always do), and it never changes the no-ask rule.

If the profile text doesn't show enough about their past to say something
specific and real, say so plainly rather than inventing a detail.

## Step 4: Pick the experience that overlaps

From the five experiences in Step 2, pick the one that connects most
specifically to something in their profile - same industry or domain,
comparable technical work, a similar founder/leadership angle, overlapping
tools, a shared board/investment area, etc. Name the overlap and which of
the five you picked (briefly, to yourself) before drafting.

If none of the five overlaps clearly, pick the one whose *type* of work
(technical/data, founder, ML/AI) is closest to theirs rather than
defaulting to the same one every time.

## Step 5: Draft the email

No character limit here (that constraint is LinkedIn's, not email's), but
brevity still wins with busy people - **60-110 words in the body**, not
counting the subject or sign-off. Longer is not more impressive; a senior
person skims in the first two lines and decides whether to keep reading.

**Subject line:** specific to them, never generic. Never "Question,"
"Reaching out," "Quick question," or their name alone. Reference the real
overlap or a specific detail about their work.

**Body, calibrated by the tier from Step 3:**

- **Executive/Board tier**: Open with the most specific, informed detail
  you have about their work (from their background/boards/investments) -
  proof you did homework on *them*, not a form letter. State your
  connection concretely (the one experience from Step 2, real numbers,
  real company name) in one sentence, not a paragraph. Ask for a short,
  specific amount of their time (e.g. 15 minutes) framed as wanting their
  perspective - never a job or referral ask. Formal but not stiff.
- **Everyone else**: Warmer and more conversational. Lead with the genuine
  overlap between your background and theirs, ask one specific question
  about their path or a detail from their background you're curious about.
  Slightly more room to be casual, still concise.

**Rules:**
- Sound like a specific real person wrote this about this specific person -
  never a template with the name swapped in. If the draft would read
  identically for a different recipient with the details changed, rewrite
  it.
- No em-dashes. Use commas or periods.
- No cliches: cut "passionate about," "would love to connect," "great to
  e-meet," "leverage my skills," "reaching out because," "I hope this email
  finds you well."
- No job or referral ask of any kind, at any tier - this is general
  networking, not an application follow-up. The only ask is their time or
  perspective.
- Never fabricate anything about them that isn't visible in the provided
  profile text, and never alter the numbers or facts in the five
  experiences from Step 2.
- Sign off with your full name (from Step 1) only - no title, no company,
  no phone number, since you're not currently employed there.

## Step 6: Output

Print which experience you picked and why, the seniority tier you assigned
and why, then the subject and body. Nothing else - no file is written by
this command.

```
Experience used: <# and title> - because <the overlap>
Tier: <Executive/Board or Everyone else> - because <the title signal>

Subject: <subject line>

Body:
<email body>
```
