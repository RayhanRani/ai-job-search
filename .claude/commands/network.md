# /network - Draft a Connection Invite From an Open Profile

`$ARGUMENTS` is the text of a LinkedIn profile that is already open/rendered
- not a company name, not a search. This command drafts one connection
invite for this specific person and does not look anyone up; it works only
from the profile text given.

This is for general networking, driven by genuine curiosity about someone's
background and career path - not outreach tied to a specific job or
application.

## Step 1: Your identity

Read `.claude/skills/job-application-assistant/01-candidate-profile.md` for
name, school, and major only - the "who I am" line of the invite. Do not
draw experience bullets from that file.

State the major as **Computer Science and Engineering** (or, if the
character budget is tight, the compact form **CS+Engineering**) - never
shorten it to just "Computer Science," since that drops the Engineering
half of the actual degree.

## Step 2: Your experience (pick exactly one)

Read `.claude/skills/job-application-assistant/02-network-experience-menu.md`
for the fixed list of five experiences. Choose whichever ONE best relates to
something in their profile - the clearest, most specific overlap, not
necessarily the most impressive one. Never mention more than one; never
combine two.

## Step 3: Read their profile

Parse the provided profile text for their name, current role/title and
company, and - most importantly - their **past**: prior roles, career
transitions, where they studied, notable projects, or how they got to where
they are now.

If the profile text doesn't show enough about their past to say something
specific and real, say so plainly rather than inventing a detail.

## Step 4: Pick the experience that overlaps

From the five experiences in Step 2, pick the one that connects most
specifically to something in their profile - same industry or domain,
comparable technical work, a similar founder/leadership angle, overlapping
tools, etc. Name the overlap and which of the five you picked (briefly, to
yourself) before drafting, so the invite is built around a real connection
rather than a generic one.

If none of the five overlaps clearly, pick the one whose *type* of work
(technical/data, founder, ML/AI) is closest to theirs rather than defaulting
to the same one every time.

## Step 5: Draft the invite

**Target 290-300 characters** (LinkedIn's hard cap is 300, and this budget
includes the closing "Can we connect?"). This is real estate to use, not a
safe minimum to clear - a 120-character draft that plays it safe is a worse
invite than a 298-character one that actually sells you. Draft, count, and
if you're under 290, go back and add specificity (a sharper detail about
them, a sharper reason) rather than padding with filler words. Never exceed
300 - trim from the least specific phrase first if you go over.

Include, woven together naturally rather than as separate bullet-like
sentences:
- Who you are: name, school, plus the one experience from Step 2 that
  connects to the overlap you picked in Step 4 - stated concretely (real
  numbers, real company name), not vaguely.
- One specific, real detail about **their** past that you're genuinely
  curious about, drawn only from what's actually in the profile.
- End with exactly: **Can we connect?**

**Rules:**
- Sound like a specific real person wrote this about this specific person -
  never a template with the name swapped in. If the draft would read
  identically for a different person with the details changed, rewrite it.
- No em-dashes. Use commas or periods.
- No cliches: cut "passionate about," "would love to connect," "great to
  e-meet," "leverage my skills," "reaching out because."
- The invite always ends with "Can we connect?" verbatim - no other
  closing line, and no referral or job ask beyond that.
- Never fabricate anything about them that isn't visible in the provided
  profile text, and never alter the numbers or facts in the five
  experiences from Step 2.
- Warm, direct, genuinely curious tone - contractions are fine, this should
  read like a real message, not a cover letter.

## Step 6: Output

Print which experience you picked and why, then the invite text and its
character count. Nothing else - no file is written by this command.

```
Experience used: <# and title> - because <the overlap>

Invite draft (<count>/300):
<invite text>
```
