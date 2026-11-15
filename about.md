---
layout: page
title: About
permalink: /about/
---
{% assign s = site.data.stats %}
We collect the public job boards that companies run for applicants on Greenhouse, Lever and Ashby: {{ s.companies }}
companies and {{ s.openJobs }} open jobs at the last count ({{ s.asOf }}). Every board is checked once a day, so we see
when a job goes up, when it comes down and what it pays when the employer says.

The posts here are written by us; every number in them comes from that collection and refreshes monthly.

The data is also available to use:

- [ATS Jobs Search](https://apify.com/redomic/ats-jobs-search): search every open job by title, country, salary,
  company or date.
- [Salary Data](https://apify.com/redomic/salary-data): pay percentiles by role and country from posted ranges.
- [Closed Jobs Tracker](https://apify.com/redomic/closed-jobs-tracker): which jobs came down and how long they were up.
- [Job Postings Dataset](https://apify.com/redomic/job-postings-dataset): bulk exports.
- A free monthly sample on [Kaggle](https://www.kaggle.com/datasets/redomic/job-postings-salaries) and
  [Hugging Face](https://huggingface.co/datasets/Redomic/job-postings-salaries).
