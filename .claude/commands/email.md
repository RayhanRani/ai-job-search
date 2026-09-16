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

The subject line, greeting, opening self-introduction, and sign-off are
all fixed and assembled separately by the calling tool for consistency
across every email - **do not draft any of those, and do not print them in
your output.** You only draft the middle section (Step 3 below).

## Step 1: Identify the recipient

Find their first name as it appears on the profile - that's all the
calling tool needs to build the greeting.

## Step 2: Your experience (pick exactly one)

Read `.claude/skills/job-application-assistant/02-network-experience-menu.md`
for the fixed list of five experiences. Choose whichever ONE best relates to
something in their profile or the target company's domain. Never mention
more than one; never combine two.

## Step 3: Confirm they're a former employee of the target company

Parse their profile for confirmation they used to work at the target
company (not currently there) - find the specific role and dates. If the
profile doesn't clearly show this (e.g. they're actually still there, or
the target company doesn't appear at all), say so plainly in the output
instead of drafting a misleading middle section.

Also note anything else genuine and specific about their time there or
their path since - what they worked on, what they moved on to, any project
or team mentioned.

## Step 4: Draft the middle section

**Target 100-140 words across exactly two paragraphs, separated by a
blank line.** This is only the middle of the email - it gets placed
between a fixed opening (name, school, a personal story) and a fixed
closing ("Best, Rayhan") that you don't write. Every sentence should carry
real information; don't pad.

**Paragraph 1 - them, and the connection:**
1. Something specific and genuine about **their** time at the target
   company or their path since - proof you actually read their background,
   not a form letter.
2. One sentence connecting your own background: the one experience from
   Step 2, stated concretely (real numbers, real company name).

**Paragraph 2 - why this company, and the ask:**
3. A genuine, **specific** reason you want to work at the target company -
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
4. Ask if they'd be open to connecting in whatever way works best for them
   - a call, or just continuing over email - and if they know anyone there
   they'd be willing to introduce you to, that it would mean a lot. Genuine
   and low-pressure, not a demand.
5. End with, verbatim: "I've attached my resume and linked my Github
   here." - plain text, no invented URL or file reference. The user
   attaches the file and adds the hyperlink themselves afterward.

**Rules:**
- Sound like a specific real person wrote this about this specific person -
  never a template with the name swapped in for the parts you control. If
  the middle section would read identically for a different recipient with
  the details changed, rewrite it.
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
the middle section only.

```
Experience used: <# and title> - because <the overlap>
Former employee confirmed: <role> at <target company>, <dates found>
Recipient: <their first name>

Middle:
<the middle section from Step 4>
```
