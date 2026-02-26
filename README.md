# AI-Powered Job Search System

A structured approach to job hunting using a Claude Project (or any AI assistant) as your personal career coach. This system helps you evaluate roles, tailor resumes and cover letters, prepare for interviews, and track your search over time.

Read the full blog post: [Building an AI-Powered Job Search System with Claude Projects](https://lab.8devops.com/posts/2026-02-26-ai-job-search-system/)

## The Idea

Instead of starting from scratch every time you apply for a job, you seed an AI project with your career history, resume, and cover letter. Then for each opportunity you just drop in the job posting and let AI do the correlation work: assess fit, tailor your materials, and coach you through the process.

Over time the project becomes a living record of your entire job search with built-in reporting and pattern recognition.

## The Philosophy

Your goal is to get interviews. Not every interview will be for your dream job, and that's the point. Every interview you go through makes you sharper, more confident, and better prepared. Your debriefs get richer. Your answers get tighter. Your STAR stories become easier to craft and relate to questions on the fly. Your ability to read a room improves. This system captures all of that progress so that when the role you really, really want comes along, you're not walking in cold. You're walking in with reps.

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

Write it in whatever format works for you. A Word doc, plain text, bullet points, stream of consciousness. Share as much or as little as you're comfortable with. You're sharing this with a cloud AI service, so use the same judgment you would with any SaaS product (see the privacy note below). The more context you give, the better the output, but start wherever you are and add more over time. A template is included in `examples/` if you want prompts to get you going, but it's not required.

You can always add more later and replace the file in your project as often as you want.

Once you have a first draft, bring it into a chat and have AI interview you to fill in the gaps. Tell it: "You are a career development guru. Ask me questions to tease out more information for this career history document." AI will prompt you for details you forgot or didn't think to include: metrics you didn't quantify, projects you glossed over, skills you take for granted, reasons behind decisions. Go through as many rounds as you want. Each pass makes the document richer, and a richer career history means better output from every other part of the system.

### 2. Resume

Your current resume, even if it needs work. This becomes the baseline that gets tailored for each application. It will evolve as you learn what's landing and what isn't. Just use whatever you already have. Templates are included in `examples/` if you're starting from scratch, but your own resume is always better as a starting point.

### 3. Cover Letter

A generic cover letter example that shows your preferred voice and style. Same idea: it gets customized per role but starts from a consistent foundation. Again, use your own if you have one. The template in `examples/` is only there if you need a blank starting point.

### 4. Instructions

The rules and preferences that tell AI how to show up every time. Copy the contents of `instructions.md` from this repo into your Claude project instructions (or save as `CLAUDE.md` if using Claude Code).

### 5. References (optional but useful)

Having your references ready in the project saves time when things move fast. When you're in the chat for a job and they ask for references, just say:

- "They requested my references, create a formatted PDF"
- "I need my references for this application, give me a copy-paste version"
- "Format my references for this role with their relevant context"

AI already knows the role, so it can tailor which details to highlight for each reference. No hunting through old files or reformatting on the fly.

### 6. LinkedIn profile (optional)

Export or print your LinkedIn profile to PDF and upload it. This gives AI another angle on your experience and helps keep your resume, cover letter, and LinkedIn profile consistent with each other. Updating your LinkedIn to match your improved resume is a topic for another day, but having the current version in the project is a good starting point.

If you have the Claude Chrome extension installed, you can also have AI review your LinkedIn profile directly in the browser. Just navigate to your profile and ask it to compare against your resume, suggest improvements, or check for consistency. No export needed.

## Directory Structure

Create a `~/job_hunt` folder (or wherever works for you). Each opportunity gets its own folder. Make sure to update the path in `instructions.md` so AI knows where your files live and can suggest correct folder names when you save output.

```
~/job_hunt/
  Acme_SrDevOpsEngineer_Research/
  BigCo_DevOpsLead_Applied/
  StartupX_PlatformEngineer_Interview/
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
2. Drop in the job posting and just ask what you need:
   - "Is this a fit?"
   - "Give me a resume and cover letter for this"
   - "Is this worth my time?"
3. AI evaluates fit and tailors your materials from what's already in the project
4. Save output to your job folder
5. Rename the chat to `Company_RoleName` so your project stays organized

That's it. No setup per job. Just paste and ask.

### Updating Status as You Go

You don't need a separate tracker. Just tell AI in the chat for that job:

- "I applied for this role"
- "I have a phone screen scheduled for Thursday"
- "I got an interview"
- "I was rejected"

AI will update the folder stage recommendation and adjust its coaching accordingly. If you're moving to interview prep, it shifts gears. If the role closed, it prompts a debrief. Just talk to it like you would a friend helping you with your search.

### Things You Can Ask AI to Do

- **Evaluate fit** - "Is this role worth my time?"
- **Tailor materials** - "Update my resume and cover letter for this posting"
- **Generate variations** - "Give me a few different resume formats so I can pick a style"
- **Interview prep** - "Run me through likely questions for this role"
- **Application help** - "Help me answer these application questions"
- **Debrief** - "The role closed, here's what happened" (captures lessons learned)
- **Reporting** - "Give me a report on everything in this project so far"
- **Unemployment work search** - "Give me my work search report for this week" (generates a table of applications for state unemployment certification)
- **Self-improvement** - "Re-evaluate my instructions based on previous conversations"
  - Should I update my resume baseline?
  - Are my cover letters landing?
  - Any patterns in which industries or locations respond more favorably?
  - Should I lean into something or change my approach?
- **LinkedIn alignment** - "Is my LinkedIn consistent with this resume?" or "What should I update on LinkedIn to match?"
- **Salary negotiation** - "I got an offer at $X, help me with a counter-offer" (AI already knows your target range and the role details)
- **Follow-up emails** - "Draft a thank you note for today's interview" or "I haven't heard back in a week, write a check-in email"
- **Networking outreach** - "Draft a LinkedIn message to a recruiter at this company" or "Help me write a cold email to a connection there"
- **Skills gap analysis** - "Across all the roles I've been looking at, what skills keep coming up that I'm missing?"
- **Behavioral interview prep** - "Give me STAR-format answers for common behavioral questions using my career history"
- **Prepping references** - "Draft a heads-up message to my references about this role so they know what to emphasize"
- **Situation check** - "What's my current situation and how should that affect my strategy?"

### Watching Company Career Pages with Change Detection

If there are companies you'd love to work for but they don't have the right opening yet, don't just check their careers page every week. Use a change detection tool like [changedetection.io](https://changedetection.io) to monitor their job pages automatically. When a new role gets posted, you get notified.

This pairs well with the project workflow: when a notification fires, drop the new posting into a chat and run through the normal fit/tailor cycle. You're first in line instead of finding it two weeks late on a job board.

Tips for setting up career page monitors:
- Point them at the company's careers or jobs page, not the homepage
- Filter for keywords relevant to your target roles so you don't get noise from every new posting
- Consider a separate Claude Project where AI acts as a changedetection.io expert to help you tune your filters and selectors

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

### Debriefing After Interviews

After each interview round, tell AI what happened:

- What questions did they ask?
- What went well?
- What caught you off guard?
- What would you answer differently next time?

AI uses this to sharpen your prep for the next round and builds a library of real interview questions over time. The more you debrief, the better your prep gets.

### Closing an Opportunity

When a role closes at any stage, update the chat with a final debrief:

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

The more detail you capture along the way (debriefs, status updates, interview notes, feedback), the richer the reports get. At the end of a search you can generate a comprehensive final report with real stats on response rates, stage conversion, which industries responded, what skills kept coming up, and how your approach evolved. It's a satisfying way to close out a search and useful reference material if you ever go through it again.

### Unemployment Work Search Reports

If you're collecting unemployment benefits, most states require you to document your job search activity for weekly or biweekly certification. Instead of tracking this separately, just ask AI to generate a work search report for the last 7 days. It pulls from your conversations in the project and outputs a table like:

| Date Applied | Company Name | Company Website | Position Title | How Applied | Result |
|---|---|---|---|---|---|

Copy-paste ready for whatever form your state needs. If your state requires different columns, just tell AI and it will adjust the format.

## Review Everything Before It Goes Out

This is important: always read every resume and cover letter AI generates before you send it. Even with instructions telling it not to, AI will sometimes hallucinate, exaggerate, or misrepresent your experience. It might say you led a project you only contributed to, claim you have experience in an industry you've never worked in, or inflate a metric you can't back up.

Getting caught in an interview trying to explain something on your resume that isn't true is not a position you want to be in. You are the final quality check.

When you catch AI doing something wrong repeatedly, tell it to remember. Be specific:

- "Add a memory: I did not work in healthcare, stop mentioning it"
- "Add a memory: I did not complete the SOC2 audit, I only started the readiness process"
- "Add a memory: my team was 4 people, not 7"

The instructions tell AI not to fabricate, but it will still get things wrong, especially early on before it has enough corrections to work from. The more you correct it, the better it gets. Treat the first few rounds as a calibration period where you're training it on what's actually true about your career.

## A Note on Privacy

You are sharing your career history and personal details with a cloud AI service. Treat it the same way you would any cloud SaaS product. The data lives on their servers and is subject to their privacy policies. Don't share anything you wouldn't be comfortable putting in a Google Doc or Dropbox. Most AI providers have data handling policies you can review, and some offer options to opt out of training. Read the fine print for whichever service you use.

## Getting Better Over Time

The whole system improves as you use it:

- Your career history gets richer as you remember more details
- Your resume baseline gets stronger as you learn what works
- Your instructions evolve to match your preferences
- AI memory fills in with your patterns and feedback
- Debrief data accumulates into actionable insights

All of your seed documents can be replaced at any time. As you go through the process, you'll land on resume formats you prefer, cover letter styles that feel right, and career history details you want to add or refine. Swap them out in the project whenever a newer version is better. These are living documents, not one-time uploads. The instructions themselves will evolve too as you figure out what works for your search.

## Tools That Pair Well With This System

- **[job-scout](https://github.com/8do-abehn/job-scout)** - A self-hosted job search tool that scrapes multiple job boards (Indeed, LinkedIn, Glassdoor, ZipRecruiter, USAJOBS), tracks applications via GitHub Issues, and includes an MCP server for searching directly from Claude. Note: this repo was recently anonymized by AI and the setup instructions have not yet been fully verified from scratch. If you run into issues, open an issue on the repo.
- **Claude Code Chrome extension** - Read job descriptions and company info directly from career pages during research and interview prep. AI can see the page you're looking at and work with it in context.
- **[changedetection.io](https://changedetection.io)** - Monitor career pages at companies you want to work for. Get notified when new roles appear so you're first in line instead of finding it weeks later on a job board.

## Filling Skills Gaps With AI-Guided Labs

When the skills gap analysis shows you're missing something that keeps coming up in job postings, you don't have to just hope it doesn't come up in interviews. You can close the gap yourself with AI as your instructor and a homelab (or cloud sandbox) as your classroom.

Here's the workflow:

1. **Create a separate AI project** for the topic. Don't mix it into your job search project.
2. **Tell AI what it is.** "You are an expert Kubernetes instructor" or "You are a Terraform course designer." Setting the role up front changes the quality of everything that follows.
3. **Ask it to build a structured course.** Lessons, exercises, checkpoints, and verification steps. AI can design a full curriculum from beginner to practical competence.
4. **Use your homelab as the lab environment.** VMs, containers, bare metal, whatever you have. If you don't have a homelab, a cloud free tier or local Docker setup works too. The point is hands-on practice, not just reading.
5. **Work through it with AI as your guide.** When something breaks (and it will), troubleshoot together in real time. AI can read error messages, suggest fixes, and explain what's happening. This is where you learn the most.
6. **Verify at each checkpoint.** Don't skip the verification steps. They catch misconfigurations early and build real confidence that you understand the material, not just copied commands.

The result: you walk into an interview and can talk about the technology from experience, not theory. "I set up a three-node Kubernetes cluster in my homelab and deployed a monitoring stack" is a fundamentally different answer than "I've read about Kubernetes."

Even better: if your homelab projects live in a public GitHub repo, the interview dynamic changes entirely. It stops being hard questions to prove yourself and turns into show and tell. Point interviewers to your repo, walk them through what you built, and let the work speak for itself. That's a much better conversation for everyone.

This approach was inspired by [Mischa van den Burg's KubeCraft](https://mischavandenburg.com/aboutme/) teachings on self-directed technical learning. Having a homelab to practice on made all the difference for refreshing skills and building confidence before interviews.

## Resources and Inspiration

- **[Farah Sharghi](https://www.farahsharghi.com/)** - Ex-Google recruiter who has reviewed 136,000+ resumes at Google, TikTok, Uber, Lyft, and The New York Times. Her YouTube channel is full of practical advice on how recruiters actually evaluate candidates. Her video [Ex-Google Recruiter Explains Why "Lying" Gets You Hired](https://www.youtube.com/watch?v=T__1QViXUxk) is a great one to watch before every interview.
- **[Mischa van den Burg / KubeCraft](https://mischavandenburg.com/aboutme/)** - DevOps engineer who advocates for career sovereignty and self-directed learning. His approach to building skills through real projects and public documentation is worth studying.

## A Note on AI-Generated Writing

AI has recognizable writing patterns, and recruiters are increasingly aware of them. If your resume reads like a chatbot wrote it, that undermines everything this system is trying to do. You want to have your flair. People want to hire you, not a robot. This is a tool to help with the heavy lifting, not to replace your voice.

The project instructions include specific rules to avoid common AI tells: inflated language, overused transitions, uniform sentence structure, and the kind of polished-but-generic tone that screams "I didn't write this." But instructions only go so far. You still need to read every output and make sure it sounds like you.

For a detailed reference on what to watch for, see [Wikipedia: Signs of AI Writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) (h/t Tim Braun for surfacing this). It's worth reading once and keeping in mind as you review AI output. The instructions in this project already incorporate the key points, but knowing what to look for yourself makes you a better editor of your own materials.

## Files in This Repo

| File | Purpose |
|------|---------|
| `README.md` | This guide |
| `instructions.md` | Claude project instructions (paste into your AI project) |
| `examples/resume-template.md` | Resume template (only if you don't have one yet) |
| `examples/cover-letter-template.md` | Cover letter template (only if you don't have one yet) |
| `examples/career-history-template.md` | Career history template with prompts to get you started |

---

One last thing: actually read the instructions before you use them. Remove stuff. Add stuff. See what it does. I built all of this iteratively as I went through my own job search, so I could see the impact of each change in real time. If you just copy-paste it blindly, you're trusting a stranger's workflow without understanding why any of it is there. Make it yours. Good luck.
