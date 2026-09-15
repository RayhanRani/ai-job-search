# /update - Technical Proficiency Gap Note (Technologies only, additive)

`$ARGUMENTS` is a job posting (URL or pasted text). Produces a **separate note** - never edits the candidate's actual resume/profile files.

## Candidate's existing Technologies (baseline - only ever added to, never reordered or removed from)

Read `.claude/skills/job-application-assistant/01-candidate-profile.md` for the current list. As of writing:

- **Technologies:** React.js, Vue.js, Node.js, Pandas, NumPy, Jupyter, Scikit-learn, GitHub, Android Studio, AWS, Firebase, Figma, Jira, Slack, Snowflake, Airflow, dbt, Claude, Cursor

Languages (C, C++, Python, SQL, Go, JavaScript, TypeScript, Java, HTML/CSS) are **never touched** - leave them exactly as-is in the After version, no additions, no reordering.

## Steps

1. Fetch/read the posting. Extract every specific technical skill, language, or tool it lists as required or preferred.
2. For each skill found, check whether it (or a clear synonym) is already in the Technologies list above.
3. Sort into two groups for the note:
   - **Already have:** posting skill + which existing item it matches
   - **New addition:** posting skill not currently in the list - the candidate has confirmed they either already know it or will learn it before the role starts, so this gets added
4. **Abbreviate long terms using standard, widely-recognized industry shorthand** before adding them - e.g. "Continuous Integration/Continuous Delivery" or "Continuous Delivery and Integration" -> "CI/CD", "Machine Learning" -> "ML", "Artificial Intelligence" -> "AI", "Object-Oriented Programming" -> "OOP", "User Interface" -> "UI". Only abbreviate to a form a recruiter or ATS would immediately recognize - never invent a shorthand. Do this for every new addition before the character count matters.
5. **Character budget: the After Technologies line must stay within the same length as the Before line** (measured with the "• Technologies: working experience with " prefix included) - it has to fit the same space on the one-page resume, so it can't just keep growing.
   - Compute the Before line's character count first.
   - Append the new-addition skills.
   - If that pushes past the Before length, **rank every existing item by relevance to this specific posting** (explicitly named > synonym > topically close > no connection at all) - do not just look at position in the list. Bump the **least relevant** existing items first, one at a time, until the line is back within budget, regardless of where they originally sat in the list. Never bump a "new addition" to make room, since those are the ones the posting actually asked for.
   - Report exactly which existing items got bumped, and note that they were the lowest-ranked for this posting, not just the last ones listed.
6. Do not modify the candidate's actual Technical Proficiency section, profile file, or any resume file. This command only writes the note below.

## Output

Write to `updates/TP_<company>.txt` (create the folder if needed). **If this file already exists for the company** (e.g. a different role at the same company was checked earlier), overwrite it completely with this run's note - don't merge, append, or create a second file. The file always reflects the most recently checked posting for that company. Print the note in the response too:

```
Technical Proficiency Gap Note - <Company>

Already have:
- <posting skill> (matches: <existing item>)
- ...

New additions (appended to Technologies):
- <posting skill>
- ...

Bumped to make room (least relevant to this posting, removed to keep the line's character count matching Before):
- <existing skill>, if any
- ...

--- Before / After preview (not applied - for reference only) ---

BEFORE (current):
Technical Proficiency August 2017-Present
• Languages: working proficiency in C, C++, Python, SQL, Go, JavaScript, TypeScript, Java, HTML/CSS
• Technologies: working experience with React.js, Vue.js, Node.js, Pandas, NumPy, Jupyter, Scikit-learn,
GitHub, Android Studio, AWS, Firebase, Figma, Jira, Slack, Snowflake, Airflow, dbt, Claude, Cursor

AFTER (Languages unchanged, new skills appended to Technologies):
Technical Proficiency August 2017-Present
• Languages: working proficiency in C, C++, Python, SQL, Go, JavaScript, TypeScript, Java, HTML/CSS
• Technologies: working experience with React.js, Vue.js, Node.js, Pandas, NumPy, Jupyter, Scikit-learn,
GitHub, Android Studio, AWS, Firebase, Figma, Jira, Slack, Snowflake, Airflow, dbt, Claude, Cursor, <new additions>
```
