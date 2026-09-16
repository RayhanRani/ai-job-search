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

The subject line is generated separately by the calling tool, always
"Interest in <target company>" - do not draft one, and do not print a
Subject line in your output.

## Step 1: Your identity

Read `.claude/skills/job-application-assistant/01-candidate-profile.md` for
name, school, and major only.

## Step 2: Your story

This is the real personal voice for the email's opening - not your resume,
your actual story:

> Grew up watching Shark Tank and building Legos, which made me passionate
> about problem solving. Working proficiency in Python, SQL, C, and
> JavaScript. Founded a profitable startup and interned at a few companies
> of varying sizes across technology, finance, insurance, and sales.
> Strong management and communication skills.

Draw on this for the opening 1-2 sentences of every email - genuine,
personality-forward, not a resume recitation. Vary the specific angle and
phrasing draft to draft (which detail you lead with, how you phrase it) so
it doesn't read as a copy-pasted paragraph, but stay true to this actual
story - never invent a different origin story or add traits not implied
here.

## Step 3: Your experience (pick exactly one)

Read `.claude/skills/job-application-assistant/02-network-experience-menu.md`
for the fixed list of five experiences. Choose whichever ONE best relates to
something in their profile or the target company's domain. Never mention
more than one; never combine two.

## Step 4: Confirm they're a former employee of the target company

Parse their profile for confirmation they used to work at the target
company (not currently there) - find the specific role and dates. If the
profile doesn't clearly show this (e.g. they're actually still there, or
the target company doesn't appear at all), say so plainly in the output
instead of drafting a misleading email.

Also note anything else genuine and specific about their time there or
their path since - what they worked on, what they moved on to, any project
or team mentioned.

## Step 5: Draft the email

**Target 130-170 words in the body** (a bit more room than a pure ask email
since it opens with a real personal intro) - not counting the sign-off.
Every sentence should still carry real information; don't pad.

**Body, in this order, woven together naturally (not as a bulleted list):**
1. Open with 1-2 sentences of genuine personal introduction drawn from
   Step 2 - who you are, what got you into this, in your own voice.
2. Pivot to something specific and genuine about **their** time at the
   target company or their path since - proof you actually read their
   background, not a form letter.
3. One sentence connecting your own background: the one experience from
   Step 3, stated concretely (real numbers, real company name).
4. State plainly and warmly that you'd really like to work at the target
   company - direct honesty reads better than dancing around it.
5. Ask if they'd be open to connecting in whatever way works best for them
   (a call, coffee, or just continuing over email), and if they know anyone
   there they'd be willing to introduce you to, that it would mean a lot.
   Genuine and low-pressure, not a demand.
6. Mention you've attached your resume and dropped your GitHub below.
7. Close with real warmth - looking forward to hearing back, not a generic
   sign-off.

**Rules:**
- Sound like a specific real person wrote this about this specific person -
  never a template with the name swapped in. If the draft would read
  identically for a different recipient with the details changed, rewrite
  it.
- No em-dashes. Use commas or periods.
- No cliches: cut "passionate about" (except as it appears in Step 2's own
  wording), "would love to connect," "great to e-meet," "leverage my
  skills," "reaching out because," "I hope this email finds you well,"
  "hit the ground running."
- Never fabricate anything about them that isn't visible in the provided
  profile text, and never alter the numbers or facts in the five
  experiences from Step 3 or the story in Step 2.
- Warm, direct, genuinely personal - contractions are fine.
- Sign off with your full name (from Step 1), then on separate lines:
  "Resume attached" and your GitHub link from Step 6.

## Step 6: Your GitHub

https://github.com/REPLACE_WITH_YOUR_USERNAME

Use this exact URL in the sign-off. If it's still the placeholder above,
print it in the output as-is rather than inventing a different one -
that's a signal to update this file, not to guess.

## Step 7: Output

Print which experience you picked and why, then confirmation of the
former-employee relationship you found (or, if you couldn't confirm one,
say so instead of the line below), then the body only - no Subject line,
that's handled separately.

```
Experience used: <# and title> - because <the overlap>
Former employee confirmed: <role> at <target company>, <dates found>

Body:
<email body>
```
