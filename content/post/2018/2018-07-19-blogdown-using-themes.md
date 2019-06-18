---
title: 'Using themes with blogdown: Lesson learned'
author: Peter Baumgartner
date: '2018-07-19'
categories:
  - reflection
tags:
  - blogdown
slug: blogdown-using-themes
draft: no
lastmod: '2019-06-07'
description: After almost one year of interruption, I started re-using blogdown again.  But
  instead of writing new content, I had to struggle once again with using the sophisticated
  machinery of  Hugo hidden in the functionality of its themes.  In this post, I will
  report on my Odyssean experience and --- more important --- I will suggest guidelines
  on how to start, explore, and use themes in blogdown.
---
After almost one year of interruption, I started re-using [blogdown](https://bookdown.org/yihui/blogdown/) again.  But instead of writing new content, I had to struggle once again using the sophisticated machinery of  [Hugo](https://gohugo.io/) and my [academic-theme](https://sourcethemes.com/academic/). With painful experiences, I learned that one has to be cautious with updates to prevent breaking changes. In this post, I will report on my Odyssean experience and --- more important --- I will suggest guidelines on how to start, explore, and use themes in blogdown.

Finally --- after almost one year of interruption --- I could reorganize my working responsibilities to spend more time working with `blogdown` and `Hugo`.

But (re-)starting blogging using these tools was not easy after such a long period. I did not only forget many procedures but also ran into compatibility problems with the necessary updates. It turned out for me that the [R Markdown](https://bookdown.org/yihui/rmarkdown/) ecosphere produces not only valuable and powerful tools but is a continuously changing complex still stricken with some fragilities.

After reporting on these difficulties, I will summarize the lessons I learned.

{{%expand "EXPAND to read the full story of my distress"  %}}

## Report from an Odyssean Journey

### Problems with my old theme

Last year I was intrigued by the potent [docdock theme](https://themes.gohugo.io/docdock/). It has many dynamic features (aka `shortcodes`) and is uniquely good suited for complex structured information. I have learned in my posting career with [WordPress](https://wordpress.org/) on [Gedankensplitter](http://peter.baumgartner.name) that over time, new subjects emerge and require a change of the content structure. I was especially delighted that `docdock` could produce dynamic HTML slides with the [reveal.js](https://revealjs.com/#/) framework, which I planned to use for [tutorials](https://notes.peter-baumgartner.net/slide/) and teaching.

After updating my software machinery (R, R packages, Hugo), I also installed a new release of the `docdock` theme. And here the odyssey started! I got many error messages which I could not solve. One problem was that I tweaked the theme (sacrificing several days of my summer holiday last year) without the necessary profound knowledge of the way `Hugo` works. Another problem was that after not using blogdown such a long time, I had forgotten many procedures of the interplay between `blogdown` and `Hugo`.

After several days of work, I did not manage to get a functional website. Worse! Meanwhile, I had destroyed my old (functioning) website as well. 😰 This disaster was for me an involuntary learning occasion to dive into [Git](https://git-scm.com/) and [GitHub](https://github.com/) to save my work and restore my repo. I had not worked on a sub-branch and had carelessly committed changes that destroyed my web presence.

To avoid similar issues, I started a clean installation of `blogdown` with the `docdock` theme. This time I did not get error messages, but experienced another surprise! The theme style I preferred had other (new) problems: The display of code snippets was not correct anymore and destroyed the page layout. I reported this issue to the theme author. Only now I noticed that the author does not respond to questions. On the issue page of the `docdock` repo, I found the following message from another user:

> Is this theme still maintained? Issues and PR's seem to indicate not. I'm looking to add a documentation theme, but I'm not interested in adding one that's been abandoned. ([Issue 151](https://github.com/vjeantet/hugo-theme-docdock/issues/151))

This question is now unanswered for more than 20 days. :angry: I do not blame the theme author. People have to work for a living; they donate their work and experiences to us whenever it is possible. But how could I be so naive only to judge my theme selection by the functionality of the theme? Not taking into account the sustainability of the theme, e.g., its complexity related with its life cycle (updates, bugs), the responsiveness of the author, the community of people using this theme and helping each other!

At that moment, I abandoned the `docdock` theme heavy-heatedly. I had put so much work into its adaption! And I like its functionality and design! Yes, I could still use my working version, but then I will lose future `Hugo` features. I didn't trust this theme anymore.

### Problems finding another suitable theme

Now I decided to choose a more simple theme and started with the [recommended theme list in the blogdown book](https://bookdown.org/yihui/blogdown/other-themes.html). The only theme I liked from its design was [ghostwriter](https://themes.gohugo.io/ghostwriter/). I installed it without problems and began using it. My first project was to learn the [Xaringan package](https://slides.yihui.name/xaringan/#1) in combination with `blogdown`. I stumbled about it reading the new [R Markdown book](https://bookdown.org/yihui/rmarkdown/). It could be a way to replace my beloved html5 slide functionality from the `docdock` theme. Instead of producing slides using  [reveal.js](https://revealjs.com/#/), I had now to learn with [remark.js](https://remarkjs.com/) another tool. But Yihui Xie --- the author behind all this fantastic stuff in the `R Markdown` ecosphere like [knitr](https://yihui.name/knitr/), `blogdown`, `bookdown`, `xaringan`, etc. --- explained convincingly why [remark is preferable to other slide frameworks](https://yihui.name/en/2017/08/why-xaringan-remark-js/) (e.g., [slidy](https://www.w3.org/Talks/Tools/Slidy2/#(1), [ioslides](https://bookdown.org/yihui/rmarkdown/ioslides-presentation.html) or [beamer](https://www.overleaf.com/learn/latex/Beamer)).

To shorten a long story: After several hours trying to bring `Xaringan` to work --- I followed the simple synopsis by [Tim Mastny](https://timmastny.rbind.io/)  in his blog entry [Embed Slides in Your Blog](https://timmastny.rbind.io/blog/embed-slides-knitr-blogdown/) --- it turned out that in the `ghostwriter` theme files in the static folder are not rendered and uploaded. This insight came as a big surprise for me! I thought that it is a standard procedure that all [files under the `static/` directory](https://bookdown.org/yihui/blogdown/static-files.html) are copied to `public/` when Hugo renders a website. Only when I found an entry by [Amber Thomas on Stack Overflow](https://stackoverflow.com/questions/41176194/hugo-not-reading-rmd-files-after-using-blogdown) --- one of the co-authors of the blogdown book --- I learned that this could be possible.

The problem was --- at least for me --- a tricky one. The website worked locally but not when I deployed it with [Netlify](https://www.netlify.com/). Even when I noticed that there were no static files uploaded in my repository, I still thought it was me, who did something wrong. As a novice user, I always believe that the problem is on my side. But after many fruitless trials, I came up with the idea to try it out with another theme. So I installed the [Xmin theme](https://themes.gohugo.io/hugo-xmin/) and learned that everything I did was done correctly.

I abandoned the `ghostwriter` theme much more relaxed than before the `docdock` theme. I was not yet emotionally linked to the theme and had (thankfully) not started with adaption work. I learned from this experience that it is an excellent strategy to test things out with the two minimal themes `Xmin` or [Lithium](https://themes.gohugo.io/theme/hugo-lithium-theme/), which provides a stable reference point. 

But how to proceed now? Should I stick with `Xmin` to be on the secure side? But I do not like this theme from its appearance. Also, my CSS knowledge is feeble, and I do not want to spend much learning and working time to adapt its design. 

So my next choice was the [academic theme](https://themes.gohugo.io/academic/). Last year I had already experimented with it, and it is one of the (more complex) recommendations in the `blogdown` book. It is a very elaborated theme with fantastic features designed for academic usage. But precisely or targeting the academic community, was the reason why I decided last year against this theme.

I am looking forward to my retirement, and I am fed up from all the administrative university business: The thought of (re)presenting all details of my scientific work and especially to transfer more than 120 publications from my `WordPress` blog to the blogdown academic framework made me furious. All I was looking for was a decent blog framework open for all the helpful tools from the [R Markdown](https://rmarkdown.rstudio.com/) ecosphere.

But incidentally, just at the same time, I noticed problems with some of the `WordPress` plugins dynamically serving my list of publications. Besides, I understood that I am not forced to use all sections of the academic framework: I could focus on the posts section --- and maybe add later on some other parts.

So I returned to my abandoned experiments with the `academic-theme` as I already did some configuration and had even written some content. First of all, I updated it to the new version and … --- Yes, again I ran into troubles! After some trials, I noticed a wired problem: It took me two days to narrow down the error. It turned out that with one of the last update, the `academic theme` was not compatible with blogdown anymore! I reported this issue to the [RStudio community](https://community.rstudio.com/t/serve-site-creates-index-of-site-rather-than-site-preview-blogdown/11120), to [George Cushen](https://github.com/gcushen/hugo-academic/issues/594) and [Yihui Xie](https://github.com/rstudio/blogdown/issues/315).

Can you imagine my emotional state? I changed between desperation and depression. All in all, it took me already two weeks with the result that I had accomplished nothing!

After taking a short nap to calm down, I reconsidered my situation: Yes, it took me much time, but at the same time, I learned a lot. I am not referring primarily to my speed generating a new `blogdown` website from scratch with a `GitHub` repo and deployed by `Netlify` (It takes my now only 60 seconds 🚀). But hopefully, I will not need this skill so frequently in the future. 😊 In addition to being more comfortable with `Git` and `Github`, I had learned general strategies to avoid similar problems in the future!

And there also came some encouraging signals from the community: Both --- Georg Cushen and Yihui Xie --- responded almost immediately to my posts. Even the problem was not solved at that time; I decided to stick with the `academic-theme`. From some other interactions (issues and questions to the theme), I had built up trust to the theme author. George is committed to his theme and very busy to deliver the best product possible. So after a roll back to an older version, I began with this article. As it stands now, this was the right decision. George and Yihui solved the issue together within two days.

{{% /expand%}}

{{%expand "EXPAND to read my conclusion and guidelines" %}}
## <a name="guidelines"></a>Lesson learned from my own experience

The following list is an attempt to turn my Odyssean experience into constructive advises for other users. I am sure it is not complete and maybe in some points faulty. If you disagree or have other, better tips: please comment on this post!

I am not going into details, and I take for granted some basic knowledge/experience with `RStudio / blogdown / Git / Github and Netlify`. To have read the [blogdown book](https://bookdown.org/yihui/blogdown/) is another requirement.

### How to choose a theme?

{{% notice tip %}}
Most important: In choosing a theme do not <b>only</b> focus on functionality and pleasing design.
{{% /notice %}}

Additionally: 

+ Look if the theme author is currently active. If there are no updates for several months or later, reconsider to choose this theme.
+ Look at the repo to decide if the author is responsive to reported issues or pull requests.
+ Look if the author provides releases from time to time. Unexperienced users like me are still not comfortable with `Git/Github`. Instead of forking and synchronizing repositories, I prefer to install updates via ZIP files.
+ Look into the documentation to see if the explanations are comprehensive and up-to-date
+ Investigate if the popularity of the theme. This check is not easily done but improves the changes for support through other users. Look not only at the number of stars and forks in the repo because that could be misleading for your purpose and community. 
+ Recherche also if people often write in blogs and forums about the theme and what kind of community is using this theme.

> … keep in mind that a more complicated and fancier theme may require you to learn more about all the underlying technologies like the Hugo templating language, HTML, CSS, and JavaScript. ([Blogdown Book](https://bookdown.org/yihui/blogdown/a-quick-example.html))

### How to start working with a theme?

{{% notice tip %}}
Most important: Do not <b>begin</b> with adapting the design of the theme. 
{{% /notice %}}


Instead:

+ Start a test site with a test repository and test deployment with `Netlify`.
+  Copy the content of `themes/<your-theme-name>/exampleSite` to your project directory. Not the folder itself, but just the content inside (e.g., the folders `static`, `content` and the `config.toml`). Overwrite these files in your project directory --- it is only a site for testing.
3. Read accompanying instructions and go line by line through the `config.toml`.  Adapt this configuration file to your needs. Make notes not only how but also why you did which setting. Documenting these changes could be helpful later when you have already forgotten you initially considerations and the procedures to follow.
4. Now start writing text in your test site. I recommend working on real posts you want to publish. Choose predominantly use cases which will be typical for your everyday work. This advice seems strange as you are working still on a test site. It is important to test the theme under real working conditions. Besides, writing real posts are not lost work: You are producing standard text files which you can transfer to other sites or themes if the need arises.
5. Establish a common workflow and get used to it. I use the following workflow:
  - I start my daily routine with `blogdown::serve_site()` using the `RStudio` addins plugin (CTRL-S on my machine) provided by the `blogdown` package. 
  - Then I start writing. After saving the file (which automatically updates the local website), I look over the result locally in my browser. (I prefer my `Google Chrome` browser for detailed inspection and use the `RStudio` viewer pane only for a general overview or to look up a specific change.)
  - From time to time --- or whenever something seems wrong or not updated --- I use `Build -> More -> Clean All` followed by restarting `R`. And again `blogdown::serve_site()` to update locally.
  - After I have finished my work, I commit and pull the changes to my repo, and after some seconds, when `Netlify` has deployed the site, I inspect the live result. 
6. After some time with your daily working routine, you get accustomed to all the other features of the theme. Even if there are functions you will not need to use: It is nice to have an overview of what could be possible and what not. This knowledge is also important to understand future updates of the theme.
7. Not until you feel comfortable with the functionality of the theme and your working habit, you should start to adopt the theme. Here it is important to do all your work on your side of the project; meaning **not** under the themes directory. Copy those files you are going to change or add under the same structure in your home folder of the `RStudio` project. Changes on these files will overwrite the virgin theme. One the one hand,  your changes are all collected in one place and separated from the original theme. On the other hand, new versions of the theme will not override your changes. 
8. Only when you have finally arrived at a status where you work could be publicly launched, change to the real website. Prepare a fresh installation with your theme, with a new repo and a new deployment by `Netlify`. 
9. Before you copy your work into a new `RStudio` project, create a new `Git` branch and check it out (= change to it). If anything goes irreparably wrong (and believe me: eventually in the long term this will be the case!) you have not destroyed your current web presence. After my odyssey, I worked with two branches besides master: `config` for bigger changes (new version of the theme, changing the configuration or the structure of my site) and `blog` for my daily (writing) work. If you decide to merge your branch with `master` you will have an additional security level: `Netlify` will check if anything went smoothly **before** your branch is merged with master. If something went wrong, you would abstain from merging your branch.  

### Problem-solving strategies 

{{% notice tip %}}
Most important: Keep calm <b>and</b> RTFM!
{{% /notice %}}



1. Use `Google` (or other search engines) to see if other users experienced the same problem. Start your search inquiry with `blogdown <name of your theme> <error message>` or different appropriate combination of content. Most of the time, you will get results linked to questions in [Stack Overflow](https://stackoverflow.com/) or blog posts where other users reported about the same or similar problems.
2. If you cannot find appropriate problem/solution pairs, I would now --- after my Odyssean experience --- not yet starting to bother people at discussion fora. Start instead of a new reference (test) site with the `XMin` theme and try to reproduce the problem. If it works there, then the problem has to do with your theme or the changes you have made. 
3. If the problem persists in your theme, then there are still two possibilities: Either you did something wrong, or it really is a bug in one of the pieces in the R Markdown machinery. Produce a [reproducible example](https://stackoverflow.com/help/minimal-reproducible-example) ( aka `repex`,) and [report the problem at Stack Overflow](https://stackoverflow.com/questions/5963269/how-to-make-a-great-r-reproducible-example). Your replication on the otherwise empty reference site will help you to focus on the essential question and will also provide an excellent reproducible example.

{{% /expand %}}


<p id="from-docdock-to-academic"></p>
{{% panel theme="primary" header="From docdock to academic theme and back again" %}}

**Update (2019-06-03):** As you can see from the footer, this website is using the `docdock`- and not the `academic` theme I wrote above. I started with the `docdock` and abandoned it for reasons I mentioned above. After another year of creative abstinence of blog writing, in May 2019, I fired up the `blogdown` machinery again. But because of a combination of many updates of `Hugo` (from 0.27 to 0.55.6!) and the `academic` theme (from 2.4 to 4.3), I not only ran into a bunch of error messages, but I have also lost track of different breaking changes and couldn't recover. ---😳  

So I changed to `docdock` back, but this time with somewhat more knowledge. Hopefully, my activities were not a circle but a helix movement where I managed some advances. Thinking positively, hopefully, I can stick with this theme in the future. I do not want writing another complaining article next year, addressing the same problems again.

**Update (2019-06-07):** The reason for my problems mentioned above was an old version of [pandoc](https://pandoc.org/). I had installed "pandoc-1.19.2-29-jan-2017", but the latest release of the date of this writing is "pandoc-2.7.2-5-april-2019". Now I could successfully update [Hugo](https://gohugo.io/) to "v0.55.6" By this occasion I also updated [jQuery](https://jquery.com/) v2.2.3 to v.3.4.1.

Now there wouldn't be any reason not to return to the `academic` theme. But I had worked hard the last week and learned so much about my `docdock` theme, that I am feeling now very comfortable and will stick with it.
{{% /panel %}}

