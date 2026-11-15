---
layout: post
title: "How to use AI to apply for jobs in 2026 (without becoming spam)"
description: "A practical way to use ChatGPT, Claude or Gemini in a job search: find fresh roles at the source, rank them against your CV, tailor honestly, and apply early. With prompts you can copy."
---
{% assign s = site.data.stats %}
AI can apply to a hundred jobs for you overnight. That is exactly why it stopped working. Recruiters now get
hundreds of near-identical applications per role, and the ones that read like a template get skipped in seconds.

The people getting interviews use AI for the slow parts of a job search (finding the right openings, judging fit,
tailoring a CV) and keep the judgment for themselves. Here is a workflow that does that, with prompts you can copy.

## 1. Find jobs where they are first posted, while they are new

Timing beats volume. Of the jobs that came down from company career pages recently, {{ s.closed.within14Pct }}%
were gone within two weeks of going up, and half within {{ s.closed.medianDaysOpen }} days. An application in the
first few days is read by someone who is still looking; one in week four often lands after the shortlist is made.

Job boards copy postings from company career pages, sometimes days later. Going to the source is faster:

- Most tech companies and funded startups post on Greenhouse, Lever or Ashby (their careers page links to
  boards.greenhouse.io, jobs.lever.co or jobs.ashbyhq.com).
- [ATS Jobs Search](https://apify.com/redomic/ats-jobs-search) searches all {{ s.openJobs }} open jobs on
  {{ s.companies }} of those career pages at once. Filter by title words, country, remote, minimum salary, and
  "first seen within days" set to 1 or 2 to get only new openings. Export the results as a spreadsheet or CSV.

You now have a list of 20 to 50 fresh roles instead of a feed of 2,000.

## 2. Let AI rank the list against your CV

Paste your CV and the list into ChatGPT, Claude or Gemini. Keep the job rows short (title, company, location,
salary, link) so the model can compare them.

> Here is my CV, then a list of job openings. Score each opening from 1 to 10 for how well my experience matches
> it, based only on what is in my CV. For each, give one line on the strongest match and one on the biggest gap.
> Sort by score. Do not reward jobs just for being senior or well paid.

Then open the top ten yourself and read them. The model is good at spotting obvious mismatches; it is bad at
knowing which team you would actually enjoy.

## 3. Tailor your CV honestly

For each job you pick, give the model the full posting and your CV:

> Rewrite the bullet points in my CV so the most relevant experience for this job comes first and uses the same
> words the posting uses where they are true for me. Do not add skills, tools or results I don't have. Keep my
> numbers exactly as they are. Show me what you changed.

The "show me what you changed" line matters. Read every change. If the model turned "helped with" into "led", put it
back. Interviewers ask about the things on your CV.

## 4. Write three sentences, not a cover letter

Many hiring managers skim cover letters. A short note does more:

> Write a 3-sentence note to the hiring manager for this role. Sentence 1: the specific thing in the posting that
> made me apply. Sentence 2: the one piece of my experience that proves I can do it, with the number. Sentence 3: a
> plain ask for a conversation. No flattery, no "I am excited to".

Edit it so it sounds like you. If you would not say it out loud, cut it.

## 5. Apply on the company's site

Use the "Apply" button on the company's own careers page rather than a quick-apply button on a job board. Your
application goes straight into the system the recruiter works in, with your tailored CV, instead of a generic
profile.

## 6. Track it

A simple sheet with company, role, date applied, link and status is enough. If you run the search from step 1 on a
schedule, the new jobs can land in that sheet every morning on their own.

## What about tools that apply automatically?

They exist: browser agents and auto-apply services that fill in forms for you. They save time per application but
send the same generic CV everywhere, answer screening questions with guesses, and can apply you to jobs you would
never take. Recruiters also notice when twenty applications in a week read the same. If you use one, point it
only at a short list you have already checked, and read what it submits.

## The short version

Fewer, earlier, better-matched applications beat a hundred automated ones. Use AI to find new roles at the source,
rank them, and tailor your CV without inventing anything. Then apply yourself in the first week.

## Sources

Timing figures come from our daily check of {{ s.companies }} company job boards on Greenhouse, Lever and Ashby
({{ s.openJobs }} open jobs; closures recorded since {{ s.closed.since }}). They refresh monthly, last on
{{ s.asOf }}. More numbers: [the best time to apply for jobs]({{ site.baseurl }}/best-time-to-apply-for-jobs/) and
[ghost jobs in 2026]({{ site.baseurl }}/ghost-jobs-2026/).
