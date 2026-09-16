# /network - Draft a Connection Invite From an Open Profile

`$ARGUMENTS` is the text of a LinkedIn profile that is already open/rendered
- not a company name, not a search. This command drafts one connection
invite for this specific person and does not look anyone up; it works only
from the profile text given.

This is for general networking, driven by genuine curiosity about someone's
background and career path - not outreach tied to a specific job or
application.

## Step 1: Candidate background

Read `.claude/skills/job-application-assistant/01-candidate-profile.md` in
full - identity, education, all professional experience, independent
projects, research, awards, everything. You need the whole picture to find
a real overlap in Step 3, not just the top line.

## Step 2: Read their profile

Parse the provided profile text for their name, current role/title and
company, and - most importantly - their **past**: prior roles, career
transitions, where they studied, notable projects, or how they got to where
they are now.

If the profile text doesn't show enough about their past to say something
specific and real, say so plainly rather than inventing a detail.

## Step 3: Find the single most specific overlap

Before writing anything, scan both backgrounds (yours from Step 1, theirs
from Step 2) for the most specific, genuine point of overlap or
relatability available - ranked roughly in this order of how well they
land, most specific/rare first:

1. A near-identical experience: same specific school program, same
   hackathon/competition, same specific company, same named research area.
2. A shared uncommon path: both founders, both did a notable career pivot,
   both came from a non-obvious background into the same field.
3. A shared broad category: same general field (e.g. data engineering,
   applied AI), same school (different program), same city/region.
4. If nothing above is available, their most interesting/distinctive career
   detail on its own, framed as genuine curiosity.

Pick exactly one. A specific, narrow overlap beats a vague, broad one - "we
both built things as founders before this" beats "we're both in tech."
Name the overlap you picked (briefly, to yourself) before drafting, so the
invite is built around it rather than bolted onto a generic template.

## Step 4: Draft the invite

**Target 290-300 characters** (LinkedIn's hard cap is 300). This is real
estate to use, not a safe minimum to clear - a 120-character draft that
plays it safe is a worse invite than a 298-character one that actually
sells you. Draft, count, and if you're under 290, go back and add
specificity (a real detail, a sharper reason, a second concrete anchor from
your own background) rather than padding with filler words. Never exceed
300 - trim from the least specific phrase first if you go over.

Include, woven together naturally rather than as separate bullet-like
sentences:
- Who you are: name plus the one real anchor from your background that
  connects to the overlap you picked in Step 3 - not your whole resume,
  just what's relevant to *this* person.
- The specific overlap itself, stated concretely (name the school, the
  company, the pivot, the field - not "similar background").
- One specific, real detail about **their** past that you're genuinely
  curious about, drawn only from what's actually in the profile.
- A light, natural reason for connecting: curiosity about their journey,
  not a job or referral ask.

**Rules:**
- Sound like a specific real person wrote this about this specific person -
  never a template with the name swapped in. If the draft would read
  identically for a different person with the details changed, rewrite it.
- No em-dashes. Use commas or periods.
- No cliches: cut "passionate about," "would love to connect," "great to
  e-meet," "leverage my skills," "reaching out because."
- No job or referral ask of any kind - this is general networking, not an
  application follow-up.
- Never fabricate anything about them that isn't visible in the provided
  profile text, and never fabricate or embellish anything about the
  candidate beyond what's in their profile.
- Warm, direct, genuinely curious tone - contractions are fine, this should
  read like a real message, not a cover letter.

## Step 5: Output

Print the overlap you picked, then the invite text and its character
count. Nothing else - no file is written by this command.

```
Overlap: <the one specific thing you picked>

Invite draft (<count>/300):
<invite text>
```
