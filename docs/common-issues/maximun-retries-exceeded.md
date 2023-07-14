---
title: Maximun retries exceeded
description: Fix Github-Readme-Stats showing error "Maximun retries exceeded".
---

![](/assets/images/docs/common-issues/maximun-retries-exceeded/pat.svg)

This is due to public Vercel instance reaching Github's GraphQL limits. Even with Multiple PAT tokens used to overcome these limits but sometimes they still run out. 

The best solution is to [deploy your own Vercel instance](/getting-started/deploy-your-own/) or use an alternative one provided by the community.
