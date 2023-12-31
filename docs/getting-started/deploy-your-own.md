---
title: Deploy your own GRS Vercel instance
description: Step to step guide for Deploying your own Github-Readme-Stats Vercel instance.
---

Deploying your own GRS Vercel instance has multiple benefits, including:
- No more PAT Limits
- Include private commits counts

Video Guide
<iframe width="854" height="480" src="https://www.youtube.com/embed/n6d4KHSKqGk" title="UPDATE: Next Level GitHub Profile README (NEW) | GitHub Actions | Vercel" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

1.  Go to [vercel.com](https://vercel.com/).
2.  Click on `Log in`.
    ![](/assets/images/docs/getting-started/deploy-your-own/pcxk33.png)
3.  Sign in with GitHub by pressing `Continue with GitHub`.
    ![](/assets/images/docs/getting-started/deploy-your-own/b9oxey.png)
4.  Sign in to GitHub and allow access to all repositories if prompted.
5.  Fork this repo.
6.  Go back to your [Vercel dashboard](https://vercel.com/dashboard).
7.  To import a project, click the `Add New...` button and select the `Project` option.
    ![](/assets/images/docs/getting-started/deploy-your-own/3n76fh.png)
8.  Click the `Continue with GitHub` button, search for the required Git Repository and import it by clicking the `Import` button. Alternatively, you can import a Third-Party Git Repository using the `Import Third-Party Git Repository ->` link at the bottom of the page.
    ![](/assets/images/docs/getting-started/deploy-your-own/mg5p04.png)
9.  Create a personal access token (PAT) [here](https://github.com/settings/tokens/new) and enable the `repo` and `user` permissions (this allows access to see private repo and user stats).
10. Add the PAT as an environment variable named `PAT_1` (as shown).
    ![](/assets/images/docs/getting-started/deploy-your-own/0yclio.png)
11. Click deploy, and you're good to go. See your domains to use the API!
