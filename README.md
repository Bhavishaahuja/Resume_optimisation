# Resume Optimizer - a ChatGPT skill

Tailors your resume to a job description using the same three-prompt workflow as before, packaged so you no longer have to paste the prompts each time.

| Stage | What happens | You do |
|---|---|---|
| 1. Recruiter audit | A senior recruiter at *that company* gives a match score /100, the top 5 missing keywords and 3 ten-second red flags | Reply **go** |
| 2. XYZ rewrite | Fixes the red flags truthfully and rewrites your experience with Google's XYZ formula (*Accomplished X, measured by Y, by doing Z*), leaving `[X%]` placeholders | Fill in the numbers |
| 3. ATS + skim test | An ATS filter plus a hiring manager on resume #143 of 200 mark each section Read/Skimmed/Skipped, rewrite the weak ones, and return the **final resume** | Copy it into your doc |

It never invents experience or numbers. Anything the resume can't back up goes under "Gaps you can't fake".

## Files

```
resume-optimizer/          <- the skill (upload this folder, zipped)
  SKILL.md
  references/xyz-formula.md
resume-optimizer.zip       <- ready-to-upload zip
custom-gpt/instructions.md <- fallback for a Custom GPT (under 8,000 characters)
```

## Install in ChatGPT (Skills)

1. In ChatGPT, open **Skills** (in the sidebar or Settings, depending on your plan) and choose to upload or create a skill.
2. Upload `resume-optimizer.zip`.
3. Start a new chat and paste: the JD, the company name and your resume (or attach the PDF). The skill starts on its own; you can also call it by name ("use resume-optimizer").

The same folder works as-is in Claude (Settings -> Capabilities -> Skills) and Codex, because they share the `SKILL.md` format.

## Fallback: Custom GPT

If your account doesn't have Skills: **Explore GPTs -> Create -> Configure**, paste `custom-gpt/instructions.md` into *Instructions*, optionally upload `resume-optimizer/references/xyz-formula.md` as *Knowledge*, and turn on Web Search (so it can look at the company).

Conversation starters:
- "Here's the JD, company and my resume - start the audit"
- "Run all 3 stages, I'll fill numbers later"
- "Same resume, new JD"
