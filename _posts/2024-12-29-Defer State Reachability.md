---
title: "Tip: Defer State Reachability"
date: 2024-12-29
categories: [creativity, speed_boost, finding_bugs]

---

The idea is in this tweet: https://x.com/BowTiedDravee/status/1872741659164983656

> Tip: defer state reachability.
> Treating state reads and read-only external calls as input parameters can uncover bad paths early (and is easy on Fuzzers/FV tools).
> By doing this on sensitive functions, you can quickly understand what's needed for a vulnerability to actually exist

However, a tweet being short, it was a bit confusing and a follow-up description was given: https://x.com/BowTiedDravee/status/1873097615883288719

> You find a weakness ("if this is possible => rekt") before exploring existing paths potentially leading to the exploit fr
> A bit like the Certora Prover (over-approximating initial states / ext calls are "havoks" i.e can do anything (revert, edit states, return unexpected values))

However, the most amazing description came from Antonio Viggiano's ChatGPT prompt which did an amazing job at explaining what I tried to explain: https://chatgpt.com/share/67706907-399c-8012-8075-8c983895bb1f

