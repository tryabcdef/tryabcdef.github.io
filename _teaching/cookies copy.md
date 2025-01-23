---
title: "From Cache Confusion to Clear Solutions "
collection: testing-musings
type: "Cache"
permalink: /testing-musings/an-unforgettable-cookie
venue: "Deployment"
date: 2024-10-10
location: "City"
---

**The Importance of Cache Management Learned from a Missing Search Bar**

Introduction:
=====
Last year, as a tester on an IoT project, I was tasked with testing the implementation of a new search feature on an existing page. After completing testing on the test environment, we moved to the UAT environment and, after successful sanity testing, deployed the feature to production. However, an issue with the search bar appeared that night, and I learned some valuable lessons from troubleshooting the problem.


Sanity Testing on UAT:
======
After deploying the new search functionality on the UAT environment, sanity testing was completed without any major issues. The search feature worked as expected, and the team gave the sign-off for deployment to production.


Deployment on Production:
=====
After deployment to production, it was quite late, so I decided to skip sanity testing, assuming no issues would arise with the search bar, which seemed straightforward. However, late that night, my PM reported that the search bar was not visible in production.

Identifying the Cache Issue:
=====
I logged into the production application and saw the search bar was visible on my laptop. Upon further investigation, I realized I was logged in via incognito mode, which doesn't use the cache. Switching to a normal browser mode, I confirmed the issue: the search bar was invisible due to a caching problem. We instructed the client to clear their cache, which resolved the issue.

Lessons Learned:
=====
This incident even though appeared as a normal cache issue ,actually gave many valuable insights:

* Always perform smoke testing: A thorough smoke test could have flagged this cache issue early.
* Ensure developers implement cache-busting techniques: Developers should ensure that code changes do not require users to manually clear their cache or use incognito mode.
* Debugging at your level is crucial: Before drawing conclusions, it's important to investigate potential causes on your own, which helps avoid unnecessary escalation. 
