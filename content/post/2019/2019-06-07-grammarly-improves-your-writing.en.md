---
title: Grammarly improves your writing
author: Peter Baumgartner
description: 'The article reports on my experiences with the premium version of Grammarly, an AI-powered web service for grammar and spell checking. As this is going to be a very positive review, I want to disclose that I am not affiliated in any way with Grammarly Inc., the enterprise behind this product.'
date: '2019-06-07'
lastmod: '2019-06-08'
categories:
  - review
  - report
  - webService
  - app
tags:
  - grammarly
slug: grammarly-improves-your-writing
toc: no
disable_comments: no
draft: no
---
## My story with Grammarly

This article reports on my experiences with the premium version of Grammarly, an AI-powered web service for grammar and spell checking. As this is going to be a very positive review, I feel the obligation to publicly disclose that I am not in any way affiliated with Grammarly Inc., the enterprise behind this product. 

It was almost exactly one year ago in June 2018 when I learned the first time about Grammarly. I cannot remember anymore, why I stumbled over Grammarly. At first, I used it only with the free plan experimentally for some of my English writing on the web. I have to confess that I was very skeptical about the practical usefulness of this kind of app. 

But after some tests, I was surprised about the quality of the suggestions. Grammarly was quite helpful as it gave me not only corrections for words spelled wrongly but also tips and ideas for a better style in English writing. At the same time, Grammarly told me not only how many improvements it has already suggested to me for a specific text passage, but also how many more suggestions would be in the premium version. Clearly enough, this was a sales gimmick, but a well-done one! I became curious about these other recommendations and signed finally up in August 2018 for the Premium version. At that time, it was still  `US$ 62,98` for a year, but in the meantime, the price has more than doubled (`US$ 139,95`) for the yearly subscription. I didn't regret it! 

## Use cases illustrated by screenshots

Besides spell and grammar, Grammarly also helped me with style issues and even to find the right tone to address a particular audience. As a non-native speaker, it is difficult for me to judge any English improvements. But from reading much English literature, I've got the feeling that my English writing has improved tremendously.

I do not intend to write a tutorial for Grammarly, but I will give you some examples of use cases, illustrated by screenshots.

### Use case 1: An already published article

I took a [lengthy article](/2017/10/17/what-is-obvious-and-for-whom/) (about 2.500 words), which I had published two years ago. I copied the markdown formatted text directly into the web interface of Grammarly. This article has a somewhat philosophical flavor so that technical concepts, which Grammarly has not in its dictionary, didn't play a role. I had the text already cleaned up form spelling errors using RStudio's spell checker. Nevertheless, Grammarly came up with more than 125 suggestions for improvements. I didn't think that my English is so bad. How embarrassing!  

When I inspected the text in detail, it turned out, that 19 suggested "improvements" weren't useful, as they addressed quotes from English books by famous people like [Michael Polanyi](https://www.newworldencyclopedia.org/entry/Michael_Polanyi) or [Ludwig Wittgenstein](https://www.iep.utm.edu/wittgens/). Another four recommendations related to markdown formatted text, where corrections would have resulted in syntax errors. But still there remained about 100 helpful tips! Statistically, Grammarly advised me about possible improvements every 25 words. I was shocked, and even a little depressed!

<img class="border shadow" src="/post/2019/2019-06-07-grammarly/screenshot01-min.png" alt="Screenshot how Grammarly suggests a writing improvement"  width="60%"/>
<figcaption><h4>**Figure 1:** Grammarly suggests and explains a possible improvement</h4></figcaption>

You see on the right top of the screenshot the number of alerts or warnings (= 120). Grammarly suggests finding a more common synonym for "emphatically" and explains with examples why it is maybe not the best choice.  As all recommendations didn't quite fit for my writing intention, I decided to delete this "overly complex" word without a substitution.


### Use case 2: German text translated via Google Translate


I transcribed a [German interview with Michael Rundel](/2019/06/05/physik-libre-a-bookdown-project/) and ran the text through [Google Translate](https://translate.google.com/). I believe, `Google Translate` has already overcome its start-up difficulties. Nowadays, I think, its translation is pretty good. But the writing must still be reviewed by a human.

As you can see in the image below, Grammarly recommended after an _unpolished_ Google Translation from German to English a slightly better rate of improvements per word: 1892 words (bottom-left) with 104 tips (top-right) which accounts for one suggestion every 18 words. 

<img class="border shadow" src="/post/2019/2019-06-07-grammarly/screenshot02-min.png" alt="Screenshot how Grammarly improves a machine-translated text"  width="60%"/>
<figcaption><h4>**Figure 2:** Grammarly alerts in a machine-translated text</h4></figcaption>


If you subtract the high number of 37 tips for punctuation issues (third line in the alerts list) – which partly are markdown formatting requirements and partly are differences between American and English punctuation rules – then the ratio improves to 1 tip for every 28 words.  Admittedly this calculation is done under the caveat that after Google Translate, one has more sentences to restructure or to reformulate completely. But you can use Grammarly to implement these changes fairly quickly.


This calculation startles. Instead of struggling to formulate an English text from scratch and then to polish it with Grammarly, it appears to be more efficient – at least for me – to use another workflow: Writing my thoughts in a German paper -> than to translate it with Google Translate -> and finally using Grammarly to polish it. 

> 1. Write the text in German<br />
> 2. Translate it with Google Translate<br />
> 3. Polish it with Grammarly<br />
> 4. Publish it with Bookdown /Blogdown 

But this reasoning is not entirely correct: The first version of the English text could already be done with Grammarly and would save one complete phase of the mentioned workflows. At least, I believe, this is valid for technical writing, where writing in English is not so complicated grammatically and therefore faster. But for publications in the Humanities, the workflow with Google Translate would be perhaps the better choice.
 
### Use case 3: Writing English directly with Grammarly

To write text "live" in Grammarly has several advantages:

+ Grammarly gives you immediately a short explanation for every alert so that you can reformulate or restructure your document instantly.


<img class="border shadow" src="/post/2019/2019-06-07-grammarly/screenshot03-min.png" alt="Screenshot of an alert by Grammarly"  width="60%"/>
<figcaption><h4>**Figure 3:** Grammarly explains every current alert briefly and succinctly </h4></figcaption>

+ Grammarly offers on-demand also longer clarifications and examples. So you can learn better writing _during_ writing.

<img class="border shadow" src="/post/2019/2019-06-07-grammarly/screenshot04-min.png" alt="Screenshot of an alter explanation by Grammarly"  width="60%"/>
<figcaption><h4>**Figure 4:** If required you can get form Grammarly a more profound explication with examples </h4></figcaption>


+ Grammarly tutors you about the English language. This educational approach comes in handy when you notice that Grammarly often complains in similar situations. For instance, I didn't know that there are different punctuation rules in American and British English. As I had written the lengthy text outside of Grammarly, I had to go through the whole article and change all occurrences of wrong punctuations one by one. If I had known these different rules, I would have to use the correct rules already in writing the draft version.

<img class="border shadow" src="/post/2019/2019-06-07-grammarly/screenshot05-min.png" alt="Screenshot of a short tutorial presented by Grammarly"  width="60%"/>
<figcaption><h4>**Figure 5:** Grammarly offers on some subjects short tutorials</h4></figcaption>

+ Grammarly supports different kinds of workflows: In the default configuration, Grammarly jumps automatically from one suggestion to the next. It is a good strategy for papers already written in English. But if you are writing directly within Grammarly, it is better to turn off this feature as it destroys the writing flow. Then you can select the recommendation you want to look at individually, and Grammarly jumps to the related text passage. A third option is to work on all tips concerning a specific category (e.g., spelling, grammar, punctuation, clarity, etc.) As you don't have to jump from one type of problem to another one, the focus of one category of alerts speeds up the correction.

<img class="border shadow" src="/post/2019/2019-06-07-grammarly/screenshot12-min.png" alt="Screenshot of alerts from type 'Punctuation'"  width="60%"/>
<figcaption><h4>**Figure 6:** Working with Grammarly on alerts type "Punctuation"</h4></figcaption>





+ Grammarly opens a window with synonyms when you double click on a word in your text.

<img class="border shadow" src="/post/2019/2019-06-07-grammarly/screenshot10-min.png" alt="Screenshot of a window in Grammarly for choosing a suggested synonym"  width="45%"/>
<figcaption><h4>**Figure 7:** Grammarly window to choose from a suggested synonym</h4></figcaption>




+ Grammarly also offers recommendations to improve your writing style. The following screenshot presents my first try to begin this article. Grammarly analyzed it as a tedious text passage. This example demonstrates that Grammarly is far more than just a garden-variety of a spell or grammatic checker.

<img class="border shadow" src="/post/2019/2019-06-07-grammarly/screenshot09-min.png" alt="Screenshot of a Grammarly window with alert about a boring text passage"  width="80%"/>
<figcaption><h4>**Figure 8:** Screenshot of a Grammarly window with alert about a boring text passage</h4></figcaption>

+ Grammarly varies its suggestions according to your writing goals. You can choose your intention, subject domain, target audience, your writing intention, your style (formal/informal), and even about the emotional flavor of your writing.  Some of these features are still experimental, and I have to confess that I did not know when to choose what. I assume that my English is not good enough to use these advanced configurations.

<img class="border shadow" src="/post/2019/2019-06-07-grammarly/screenshot11-min.png" alt="Screenshot to your chosen writing style in Grammarly"  width="40%"/>
<figcaption><h4>**Figure 9:** Grammarly varies its alerts according to your chosen writing style</h4></figcaption>

+ Grammarly can seamlessly be integrated via a browser plugin into types of web content (e.g., fora, web editing). But it seems to me that these possibilities are sparse. Yes, there is an add-in for Microsoft Word, but [only for Windows](https://www.grammarly.com/office-addin/mac). In WordPress, Grammarly does not work with the visual editor, you have instead to use the code editor. Likewise, you can't use Grammarly with markdown files in RStudio or other text editors. But these shortages are not limitations as you can always write your book or article in the Grammarly cloud and then copy the text into your editor of choice. Grammarly stores your document in short time intervals, so you don't have to worry to loose parts of your work. You can go back to unfinished articles at a later time and finish it for publication. 

<img src="/post/2019/2019-06-07-grammarly/screenshot07-min.png" alt="Screenshort of my personal desktop in Grammarly"  width="80%"/>
<figcaption><h4>**Figure 10:** My personal desktop in Grammarly</h4></figcaption>

I prefer to work with the browser extension, as it always presents the same user interface. Besides, it unleashes the full power of Grammarly. All screenshots in this post show the Grammarly editor in the browser, Google Chrome, in my case. But there are also plugins for Firefox, Safari, and Edge. All these browser extensions are free, and you can use Grammarly with limited functionality at no charge as well.



## Other similar products

Finally, I should add that during the research of this article, I noticed that there are a couple of web services with related functionality available. The high number of recent articles about grammar apps insinuates a big market for this kind of service:

+ [The 5 Best Spelling and Grammar Check Apps of 2019](https://www.lifewire.com/best-spelling-and-grammar-check-apps-4176088) 
+ [The 13 Best Free Grammar Check And Grammar Corrector Apps](https://justpublishingadvice.com/the-best-12-free-grammar-check-and-grammar-corrector-apps/)
+ [Spell and Grammar checker apps like Grammarly 2019](https://www.triveditech.com/spelling-and-grammar-checker-apps/)
+ [20 Best Grammar Checker Software Solutions for 2019](https://financesonline.com/top-20-grammar-checker-software-solutions/)
+ [7 Best Spelling And Grammar Check Apps Of 2019](https://medium.com/@samjh715/7-best-spelling-and-grammar-check-apps-of-2019-b93465f2b567)
+ [What are the best grammar and spelling autocorrecting apps?](https://en.softonic.com/solutions/what-are-the-best-grammar-and-spelling-autocorrecting-apps)
+ [7 Best Online Grammar and Punctuation Checker Tools For Error-Free Writing](https://masterblogging.com/online-grammar-checker-tools/)
+ [The Best Online Grammar Check Websites of 2019](https://www.toptenreviews.com/best-online-grammar-checker)

## Wrapping up

All in all, I'm delighted with Grammarly. In my opinion, it is a beneficial tool for the non-native writer. It improves your writing for the web (e.g., posting in blogs or commenting in fora) but also for printed papers and books. It has many cute and even some outstanding features. Even with Grammarly, I am still not wholly comfortable to write in English, but at least I am stressed about it anymore.  

I do not claim that Grammarly is the best product, as I do not know the other apps and have therefore no comparison. But in most of the reviews mentioned above, Grammarly is top ranked. It is undoubtedly the app with the biggest user base (over 10 Mio.).

Last, but not least, I would like to add that Grammarly is not idiot-proof. You have to make your choices, looking up other dictionaries to find better wording. (I am happy using all the time [dict.cc](https://www.dict.cc/)). You have to be aware that even if Grammarly is AI driven, it does not understand your writing in the human sense. If you are writing a dumb and meaningless article, Grammarly cannot improve your reasoning and arguments. I noticed, for instance, that Grammarly sometimes had overlooked a missing word, an error a human would immediately see. And sometimes Grammarly is wrong with its suggestions as the last screenshot demonstrates. But these rare cases are easy to judge and correct.

<img class="border shadow" src="/post/2019/2019-06-07-grammarly/screenshot08-min.png" alt="Screenshot of a wrong recommendation by Grammarly"  width="100%"/>
<figcaption><h4>**Figure 11:** Grammarly is not idiot-proof. Your own intelligent judgement is still required.</h4></figcaption>
