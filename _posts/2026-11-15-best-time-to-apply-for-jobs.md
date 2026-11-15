---
layout: post
title: "The best time to apply for jobs, from 300,000 real job postings"
description: "Which days companies post jobs, how long postings stay up, and why the first week matters more than the day of the week. Data from 10,000+ company career pages."
---
{% assign s = site.data.stats %}
Short answer: apply in the first week a job is up, ideally in the first few days. The day of the week matters much
less than that, but if you want to know when new jobs appear, it is {{ s.weekdays.top }} and
{{ s.weekdays.second }}.

This comes from the {{ s.openJobs }} open jobs we track on the careers pages of {{ s.companies }} companies that
use Greenhouse, Lever or Ashby, checked every day.

## Which days companies post jobs

Of the {{ s.weekdays.jobs }} jobs posted in the last six months:

| Day | Share of new postings |
|---|---|
{% for d in s.weekdays.shares %}| {{ d.day }} | {{ d.pct }}% |
{% endfor %}

Recruiters post in the middle of the week. Monday is quieter, probably because it goes to meetings and reviewing
the applications that came in over the weekend. Weekends are almost empty: {{ s.weekdays.weekendPct }}% of postings.

So if you check for new jobs once a week, Thursday or Friday catches most of that week's postings while they are
still fresh. If you check every day, you will see most new jobs on Tuesday, Wednesday and Thursday.

## How long a job stays up

This is the number that matters more. We looked at every job that came down since
{{ s.closed.since | date: "%-d %B" }} and measured how long it had been up:

- half of them were gone within **{{ s.closed.medianDaysOpen }} days**
- **{{ s.closed.within14Pct }}%** closed within two weeks
- **{{ s.closed.within30Pct }}%** closed within a month
- {{ s.closed.over90Pct }}% stayed up for more than three months

A posting coming down does not always mean the job was filled, but it does mean the company stopped taking
applications for it. A third of jobs give you less than two weeks. Recruiters also tend to start screening the first
applicants while the ad is still collecting more, so a strong application on day three is read with more attention
than the same application on day twenty.

## Time of day

We don't publish an hour-by-hour chart because the posting times we see are in UTC and the companies span many
time zones, so any "post your application at 9:14 am" advice from this data would be made up. What we can say is
that sending an application on a Sunday night is fine: it will be in the pile on Monday morning either way.

## How to be early without refreshing job boards all day

Big job boards pick up a company's posting hours or days after it appears on the company's own site, and often show
it as "reposted" later. Going to the source is faster.

- [ATS Jobs Search](https://apify.com/redomic/ats-jobs-search) searches all {{ s.openJobs }} open jobs straight
  from company career pages. Set "first seen within days" to 1 and run it every morning to get only the jobs that
  appeared since yesterday, filtered by title, country, salary or remote.
- If you would rather have them in a spreadsheet automatically, schedule the same search daily and send the rows to
  Google Sheets; the Actor page shows how.

## How we counted

"Posted" is the date the employer published the job (Greenhouse's first-published date, Lever's creation date,
Ashby's published date). Weekdays are counted in UTC for jobs posted in the last 180 days. A job counts as closed
when it disappears from its board; we have recorded closures since {{ s.closed.since }}. Numbers refresh monthly,
last on {{ s.asOf }}. A free monthly sample of the data is on
[Kaggle](https://www.kaggle.com/datasets/redomic/job-postings-salaries).
