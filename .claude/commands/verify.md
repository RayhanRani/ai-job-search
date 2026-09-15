# /verify - Quick Match Check

`$ARGUMENTS` is a job posting (URL or pasted text). Output `MATCH` or `NO MATCH`, followed by one brief bullet giving the reason. Nothing else.

## Step 1: Candidate baseline

Read `.claude/skills/job-application-assistant/01-candidate-profile.md`. Relevant fact for this check:
- Undergraduate at Santa Clara University, expected graduation **June 2027**

## Step 2: Parse the posting

Fetch/read the posting (WebFetch, or curl if the page is JS-rendered and WebFetch only returns the shell). Extract the degree requirement and its timing: does it require a degree already conferred (or conferred before some start/application date earlier than June 2027), or does it accept a June 2027 expected graduation / current student?

## Step 3: Decide

Output `MATCH` if the degree requirement is compatible with a June 2027 graduation (accepts current students, new grads, or "expected graduation" language).

Output `NO MATCH` if the posting requires an already-completed degree before a start date earlier than June 2027, or if the posting is not currently open / not accepting applications.

## Step 4: Output

Print `MATCH` or `NO MATCH` on the first line, then one brief bullet (under 20 words) with the reason. Nothing else - no company name, no markdown headers.

```
MATCH
- <brief reason>
```
