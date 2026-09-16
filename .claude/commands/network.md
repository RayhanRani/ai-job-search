# /network - Draft a Connection Invite From an Open Profile

`$ARGUMENTS` is the text of a LinkedIn profile that is already open/rendered
- not a company name, not a search. This command drafts one connection
invite for this specific person and does not look anyone up; it works only
from the profile text given.

This is for general networking, driven by genuine curiosity about someone's
background and career path - not outreach tied to a specific job or
application.

## Step 1: Candidate background

Read `.claude/skills/job-application-assistant/01-candidate-profile.md` for
identity, education, and experience - the "who I am" half of the invite.

## Step 2: Read their profile

Parse the provided profile text for their name, current role/title and
company, and - most importantly - their **past**: prior roles, career
transitions, where they studied, notable projects, or how they got to where
they are now. Center the invite on genuine interest in their journey, not
on a role or company you're targeting.

If the profile text doesn't show enough about their past to say something
specific and real, say so plainly rather than inventing a detail.

## Step 3: Draft the invite

**Hard limit: 300 characters** (LinkedIn's actual connection-note cap).
Count every draft and trim until it's under - every character should be
doing work, so cut anything generic before cutting anything specific.

Include, in as few words as possible:
- Who you are: name plus one real anchor from your background (school and
  focus, or a directly relevant experience) - only what's relevant to this
  specific person, not your whole resume.
- One specific, real detail about **their** past or path that you're
  genuinely curious about - drawn only from what's actually in the profile,
  never invented or generic ("your experience" doesn't count as specific).
- A light, natural reason for connecting: curiosity about their journey,
  not a job or referral ask.

**Rules:**
- No em-dashes. Use commas or periods.
- No cliches: cut "passionate about," "would love to connect," "great to
  e-meet," "leverage my skills."
- No job or referral ask of any kind - this is general networking, not an
  application follow-up.
- Never fabricate anything about them that isn't visible in the provided
  profile text.
- Warm, low-pressure, genuinely curious tone - like a real person reaching
  out, not a template filled in.

## Step 4: Output

Print the invite text and its character count. Nothing else - no file is
written by this command.

```
Invite draft (<count>/300):
<invite text>
```
