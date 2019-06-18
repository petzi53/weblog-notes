---
title: Blogdown tutorial (Part 4)
author: Peter Baumgartner
date: '2017-09-09'
categories:
  - how-to
tags:
  - blogdown
  - netlify
  - github
slug: blogdown-tutorial-part-4
draft: no
description: In this fourth part of the tutorial I will explain a method how to bring
  your website online. My preferred method is to transfer the files via GitHub to
  Netlify, a service specialized for quickly rolling out static websites.
---

#### Bring your website online: From blogdown via GitHub to Netlify

We start this last part of the tutorial where we have finished last time  ([picture 10 of part 3]({{% relref "2017-09-08-blogdown-tutorial-part-3.md" %}})).

1. **Ignore public folder**: One benefit of using Netlify is that that there is no need to upload your large public folder to get your website. Netlify will compile the source files and build by its own the Hugo site. You should take advantage of this feature by telling RStudio that the `public`-folder does not need version control, committed and uploaded. Select the public folder under the Git tab on the right upper pane and select from the configuration menu `ignore…`. {{< figure src="/img/blogdown-tutorial/ignore-public-folder.png" title="Ignore public folder" >}}

2. **Confirm git ignore**: This will bring up a window where you can specify which files are to be ignored. Confirm the inclusion of the public folder with clicking 'Save'. {{< figure src="/img/blogdown-tutorial/git-ignore-public-folder.png" title="Confirm the exclusion of the public folder." >}} This saved file (`.gitignore`) will be added as modified to the version control. {{< figure src="/img/blogdown-tutorial/gitignore-modified.png"  >}} 

3. **Clean up**: Before we are going to rebuild the complete site, I recommend to take some precaution. To rebuild from a clean slate I restart R (Under the RStudio menu 'Session' or CMD-Shift-F10 on MacOS.) and clean up all unnecessary files ('Clean All’ in the 'Build' tab under the 'More' menu in the upper right pane.) {{< figure src="/img/blogdown-tutorial/clean-all.png" title="Rebuild website from a clean status." >}}

4. **Build website**: Now you can safely (re-)build the website by clicking into 'Build Website'. You get a message of all the activities done, the time necessary for the build and were the output was created. [Personal comment: Frankly I do not know if the last two steps are really necessary when Netlify is running its own scripts.] {{< figure src="/img/blogdown-tutorial/build-website.png" title="Rebuild website from a clean status." >}}

5. **Commit changes**: The next step is to select all changed files under the Git tab and to choose "Commit", write a commit message and to confirm these changes. {{< figure src="/img/blogdown-tutorial/commit-changes.png"  >}} {{< figure src="/img/blogdown-tutorial/reviewed-changes.png" title="Bring all changes under version control and check if everything went smoothly.">}}

6. **Push changes**: Now you can transfer all your committed changes to GitHub. After clicking on the push button a window opens and you can see if the changed files are transferred successfully. {{< figure src="/img/blogdown-tutorial/push-changes.png" title="Push the committed files to GitHub.">}}

7. **Inspect repo**: If you don't trust this process, you can direct your browser to your GitHub repository and check if really the last commit "First post" has safely arrived. {{< figure src="/img/blogdown-tutorial/inspect-repo.png" title="Inspect your repo on GitHub to confirm the procedure.">}}

8. **Get Netlify account:** The last task we are going to solve is the connection the GitHub repository to the Netlifly service. Go to [https://www.netlify.com/](https://www.netlify.com/) and create a free new account ("Get started for free"). {{< figure src="/img/blogdown-tutorial/create-account-on-netlify.png" title="Inspect your repo on GitHub to confirm the procedure.">}}

9. **Let Netlify access your repo**: After the registration procedure you get page where you can choose 'New Site from Git'.  {{< figure src="/img/blogdown-tutorial/netlify-empty.png">}} There are essential three step to create the new website: (A) Choose GitHub as your Git repository. This will bring up a window where you have to confirm that you will allow Netlify access to your GitHub account.  {{< figure src="/img/blogdown-tutorial/netlify-authorization.png">}} (B) Then you have to specify to which repository Netlify should connect. {{< figure src="/img/blogdown-tutorial/netlify-choose-repo.png" title="Authorize Netlify to access your website repository.">}} 

10. **Deploy settings**: In the third and last step (C in my former notation) on Netlify to create your website you have to specify the details (parameters) to let Netlify know which type of website it has to build. In the example in the screenshot I said that Netlify should watch my master branch, build a Hugo website from the public repository with the newest version of Hugo at the time of writing this tutorial (version 0.26). {{< figure src="/img/blogdown-tutorial/netlify-deploy-settings.png" title="Specify the deploy settings." >}}

11. **Deploy website**: After clicking "Deploy website" you can lean back and watch Netlify busy working on building the website. This may take for this initial step some time but later on Netlify will finish work almost immediately as it only builds the new/changed files incrementally. When the rolling down of the messages stops you should see as last line: "Site is live"! {{< figure src="/img/blogdown-tutorial/netlify-site-is-live.png" title="Watch Netlify working until it is finished." >}}

12. **Preview deploy**: Scroll back to the beginning of the log messages. You will see that Netlify has giving you a random URL but you can change this later on to your liking. Click "Preview deploy" to go to the URL of your new website. {{< figure src="/img/blogdown-tutorial/netlify-preview-deploy.png" title="Watch Netlify working until it is finished." >}}

13. **Website is online!:** Congratulations! Your website is now online. {{< figure src="/img/blogdown-tutorial/website-is-online.png" title="Your website is online." >}}


## Final comments

This was a very quick tour where I have covered just the things I believed to be essential. If you are (like me) new to static website generators then the different steps together seem overwhelmingly complex. But with patience and some trial and errors you should succeed --- as I have. There are many other (better) tutorials and How-Tos around. You should definitely read carefully the book [blogdown: Creating websites with R Markdown](https://bookdown.org/yihui/blogdown/) and the reports of different experiences from the new [rbind community](https://support.rbind.io/). 




