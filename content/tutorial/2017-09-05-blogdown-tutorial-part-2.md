---
title: Blogdown tutorial (Part 2)
author: Peter Baumgartner
date: '2017-09-05'
categories:
  - how-to
tags:
  - github
  - installation
slug: blogdown-tutorial-part-2
description: In part 2 we will create a GitHub repository and link it to our local
  repository, which we have created in part 1 of this tutorial.
---

#### Creating a Github repository

In part 1 we have installed the hugo-academic theme on top of R, RStudio and blogdown. We will continue the installation process with creating a remote GitHub repository.


1. In case you do not have a GitHub account, sign up for it. When you have finished the registration process click the button "Start a project". If you already have an account click at "New repository". {{< figure src="/img/blogdown-tutorial/new-repo.png" title="Creating a new GitHub repository. " >}}

2. Both actions ("Start a project" and "New repository") opens up a window where you can name your new repository. Leave all the other options empty resp. as they are and click the green button "Create repository". {{< figure src="/img/blogdown-tutorial/create-github-repo.png" title="Name your new GitHub repository. " >}}

3. The last click brings you to a "Quick setup" page with several options. As there already exist a repository with our hugo-academic files, we copy the two lines in the third option: "push an existing repository from the command line". {{< figure src="/img/blogdown-tutorial/quick-repo-setup.png" title="Quick setup: push an exiting repository from the command line. " >}}

4. But before we can paste these two lines into the terminal in order to link our local with the remote GitHub repository we need to [download Git](https://git-scm.com/downloads) and install it. The best description I know of the installation procedure and its integration with RStudio is by Hadley Wickham in chapter 13 of his book about R Packages. There is a online version available. Read the two sections [Initial set up and Create a local Git repository](http://r-pkgs.had.co.nz/git.html#git-init). For the mentioned shell commands you can use the Terminal tab of RStudio in the left lower pane. {{< figure src="/img/blogdown-tutorial/terminal-without-commands.png" title="Use for the shell command the new terminal tab of RStudio. " >}}

5. After the shell command `git init` the local repository is under version control. After you have restarted RStudio you will now see new tabs in the RStudio panes. Click in the Git tab in the upper right pane. This reveals a bunch of folder and some files. The yellow boxes with the question marks under the status column indicate that these file are not yet under version control. {{< figure src="/img/blogdown-tutorial/git-folders-and-files.png" title="Folders and files which are not under version control. " >}}

6. To bring these folders and files under version control you have to select all of them and click in one of the check boxes under the column "Staged". You will see now a lot more files as all the files under the still untracked folders are explicitly shown. The `A` indicates that these files are new (are just added) to the repository. {{< figure src="/img/blogdown-tutorial/git-added-files.png" title="New (Added) files  to be set under version control. " >}}

7. A click in the Commit tab opens up a new window where you must write a message. This is necessary so that all collaborators (including the future-you!) remembers what was the change about. This first  (e.g.initial) commit will bring all the files under version control. {{< figure src="/img/blogdown-tutorial/initial-commit.png" title="The initial commit brings many files under version control. " >}}

8. After sending your message by clicking the `Commit` button you will see a list of all the committed files which are now in the local repository under version control. You can close this window and we can finally add our two lines copied from the GitHub page. {{< figure src="/img/blogdown-tutorial/git-committed-files.png" title="Files are successfully committed. " >}}

9. Insert the two copied lines from the GitHub repository into the Terminal tab (red arrow). The first line will establish the connection between the local and the remote repository. The second line will push all the committed local files to the GitHub repository.Depending of you internet connection and how many data has to be transferred this can take a couple of seconds (blue arrow). {{< figure src="/img/blogdown-tutorial/connect-git-with-github.png" title="Connecting local Git with remote GitHub repository and pushing the initial commit. " >}}
