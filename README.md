# AI-Powered Job Search System

A structured approach to job hunting using a Claude Project (or any AI assistant) as your personal career coach. This system helps you evaluate roles, tailor resumes and cover letters, prepare for interviews, and track your search over time.

## The Idea

Instead of starting from scratch every time you apply for a job, you seed an AI project with your career history, resume, and cover letter. Then for each opportunity you just drop in the job posting and let AI do the correlation work: assess fit, tailor your materials, and coach you through the process.

Over time the project becomes a living record of your entire job search with built-in reporting and pattern recognition.

## What You Need to Get Started

Four documents seed your project:

### 1. Career History (the most important one)

Don't write this in AI first. Just start writing in your own words.

- Where you went to school, what you studied, internships, part-time work
- Projects you worked on and what you enjoyed (or didn't)
- Teachers, mentors, or people who helped you along the way and why
- Your first, second, third jobs... title, day-to-day work, projects, decisions
- Stories that go with each role, the hows and whys
- Why you left each position (the honest version, not the interview version)

Give it as much detail as you can remember. Include the good, the bad, and the ugly. The messy parts are actually the most useful: they help AI assess fit honestly, flag potential problem areas early, and coach you through tough interview questions without getting caught off guard.

Write it in whatever format works for you. A Word doc, plain text, bullet points, stream of consciousness. Share as much or as little as you're comfortable with. This is only being shared with AI, not published anywhere. The more context you give, the better the output, but start wherever you are and add more over time. A template is included in `examples/` if you want prompts to get you going, but it's not required.

You can always add more later and replace the file in your project as often as you want.

### 2. Resume

Your current resume, even if it needs work. This becomes the baseline that gets tailored for each application. It will evolve as you learn what's landing and what isn't. Just use whatever you already have. Templates are included in `examples/` if you're starting from scratch, but your own resume is always better as a starting point.

### 3. Cover Letter

A generic cover letter example that shows your preferred voice and style. Same idea: it gets customized per role but starts from a consistent foundation. Again, use your own if you have one. The template in `examples/` is only there if you need a blank starting point.

### 4. Instructions

The rules and preferences that tell AI how to show up every time. Copy the contents of `instructions.md` from this repo into your Claude project instructions (or save as `CLAUDE.md` if using Claude Code).

### 5. References (optional but useful)

Having your references ready in the project saves time when things move fast.

## Directory Structure

Create a `~/job_hunt` folder (or wherever works for you). Each opportunity gets its own folder:

```
~/job_hunt/
  Acme_SrEngineer_Research/
  BigCo_DevOpsLead_Applied/
  StartupX_PlatformEng_Interview/
```

Naming convention: `Company_Role_Stage`

Stages:
- `_Research` - evaluating fit, not yet applied
- `_Applied` - submitted
- `_PhoneScreen` - recruiter call scheduled or completed
- `_Interview` - active interview process
- `_Offer` - offer received
- `_Closed` - no longer active

Rename the folder as the opportunity progresses. If you sync to Google Drive or similar, you get cloud backup for free.

## How to Use the Project

### For Each New Opportunity

1. Start a new chat in the project
2. Drop in the job posting
3. AI evaluates fit before you invest time tailoring anything
4. If it's a go, AI tailors your resume and cover letter
5. Save output to your job folder
6. Rename the chat to `Company_RoleName` so your project stays organized

### Things You Can Ask AI to Do

- **Evaluate fit** - "Is this role worth my time?"
- **Tailor materials** - "Update my resume and cover letter for this posting"
- **Generate variations** - "Give me a few different resume formats so I can pick a style"
- **Interview prep** - "Run me through likely questions for this role"
- **Application help** - "Help me answer these application questions"
- **Debrief** - "The role closed, here's what happened" (captures lessons learned)
- **Reporting** - "Give me a report on everything in this project so far"
- **Self-improvement** - "Re-evaluate my instructions based on previous conversations"
  - Should I update my resume baseline?
  - Are my cover letters landing?
  - Any patterns in which industries or locations respond more favorably?
  - Should I lean into something or change my approach?
- **Situation check** - "What's my current situation and how should that affect my strategy?"

### The Urgency Factor

Your search strategy should reflect your runway. Tell AI your situation and update it as things change:

| Situation | Approach |
|-----------|----------|
| Still employed, exploring | Be selective, optimize for fit |
| Job ending in 6 months | Strategic and targeted |
| On furlough, 3 months runway | Broaden scope, increase volume |
| Running on severance, 1 month | Apply broadly, optimize for speed |
| No safety net | All hands on deck |

AI should factor this into every recommendation.

### Closing an Opportunity

When a role closes at any stage, update the chat with a brief debrief:

- How far did you get?
- What feedback did you receive?
- What came up that you didn't expect?
- What would you do differently?

Rename the chat to reflect the final stage. Over time these debriefs reveal patterns that make your whole approach better.

## Reporting

Because every opportunity follows the same structure, AI can generate reports on demand:

- Roles evaluated vs. applied vs. interview stage
- Which industries or company types are generating traction
- Most frequently requested skills across your target roles
- Which stage you're most commonly exiting at
- Patterns in feedback and debrief notes
- Recommendations for adjusting your approach

This turns gut feelings into concrete data.

## Getting Better Over Time

The whole system improves as you use it:

- Your career history gets richer as you remember more details
- Your resume baseline gets stronger as you learn what works
- Your instructions evolve to match your preferences
- AI memory fills in with your patterns and feedback
- Debrief data accumulates into actionable insights

Replace your seed documents in the project whenever they've meaningfully improved. The instructions, resume, cover letter, and career history are all living documents.

## Files in This Repo

| File | Purpose |
|------|---------|
| `README.md` | This guide |
| `instructions.md` | Claude project instructions (paste into your AI project) |
| `examples/resume-template.md` | Resume template (only if you don't have one yet) |
| `examples/cover-letter-template.md` | Cover letter template (only if you don't have one yet) |
| `examples/career-history-template.md` | Career history template with prompts to get you started |
