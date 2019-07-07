---
title: How to install Disqus on Hugo?
author: Peter Baumgartner
date: '2017-09-10'
categories:
  - how-to
tags:
  - blogdown
  - disqus
  - hugo
  - installation
slug: how-to-install-disqus-on-hugo
draft: no
description: This post explains how to integrate Disqus as a discussion forum for
  your website. It is not a thing you can do directly applying the Hugo documentation
  because there is a faulty template to change.
---

### Steps to intgrate Disqus into your Hugo website

1. **Sign up**: First of all you have to sign up for [Disqus](https://disqus.com/). {{< figure src="/img/disqus/sign-up.png" title="Create an account on Disqus." >}}

2. **Install Disqus**: You are offered two choices after the registration process. Select 'I want to install Disqus on my site'. {{< figure src="/img/disqus/two-choices.png" class="small" title="Choose 'Install Disqus'" >}}

3. **Fill in the form**: Disqus needs some information for adding a forum to your website. I will add just two remarks as the form is mostly self-explaining. Firstly, the website name is a text snippet that will appear in the head of every forum section. It does not have to be related to you website name. Secondly, make a note of your Disqus short name as you are going to use it in step 5 and 6. {{< figure src="/img/disqus/fill-in-form.png" title="Configure Disqus for your site" >}}

4. **Find discussion template**: With the next two steps we are going to fix the problem of a faulty Hugo template. Look for the file 'single.html' and open it in the editor to inspect the content. `single.html` should be under `/themes/<your-theme-nam>/layouts/_default`.  At the end of the file -- just before the footer --, you should find the name of the partial template for your discussion forum (= 'comments-html' in my case). {{< figure src="/img/disqus/find-discussion-template.png" title="Configure Disqus for your site." >}}

5. **Replace content**: Now go and edit this file, which should be found under `/themes/<your-theme-nam>/layouts/partials`. You have to replace the whole content with the [code snippet provided by Yihui Xie](https://github.com/rstudio/blogdown/issues/52#issuecomment-288407836) (Thanks a lot by the way!!). To help you, you can [compare my changes at GitHub](https://github.com/petzi53/weblog/commit/b7993533e501e2f1668375e22fe05e1ceb7d87ae?diff=split). But don't forget to change the URL to your Disqus account [as I did :blush:]! {{< figure src="/img/disqus/my-github-changes.png" title="Replace content of your partial template as explained" >}}

6. **Add shortname**: To finish the installation you have finally to add the line `disqusShortname = "<your-disqus-shortname>"` to your config.toml. {{< figure src="/img/disqus/add-disqus-shortname.png" title="Add your Disqus short name into the config.toml" >}}

7. **Congratulation!** You have integrated Disqus into your static website. Go to one of your posts and check it. Your end of the page should look similar as in the following graphic. {{< figure src="/img/disqus/disqus-integrated.png" title="Disqus forum successfully integrated" >}}

## Critical remark to Disqus

I should mention that there is growing skepticism in the community about Disqus. People are not only criticizing slowness (load-time behavior) but above all they are concerned about data integrity. It seems that there are lots of [irrelevant requests](http://donw.io/post/github-comments/) to track the data traffic for whatever purpose nobody knows. 




<span class='Z3988' title='url_ver=Z39.88-2004&amp;ctx_ver=Z39.88-2004&amp;rfr_id=info%3Asid%2Fzotero.org%3A2&amp;rft_val_fmt=info%3Aofi%2Ffmt%3Akev%3Amtx%3Adc&amp;rft.type=blogPost&amp;rft.title=How%20to%20install%20Disqus%20on%20Hugo?%20::%20Open%20Science%20Education&amp;rft.source=How%20to%20install%20Disqus%20on%20Hugo?&amp;rft.rights=CC%20BY-SA%204.0&amp;rft.description=This%20post%20explains%20how%20to%20integrate%20Disqus%20as%20a%20discussion%20forum%20for%20your%20website.%20It%20is%20not%20a%20thing%20you%20can%20do%20directly%20applying%20the%20Hugo%20documentation%20because%20there%20is%20a%20faulty%20template%20to%20change.&amp;rft.identifier=https%3A%2F%2Fnotes.peter-baumgartner.net%2Ftutorial%2Fhow-to-install-disqus-on-hugo&amp;rft.aufirst=Peter&amp;rft.aulast=Baumgartner&amp;rft.au=Peter%20Baumgartner&amp;rft.date=&amp;rft.language=en'></span>