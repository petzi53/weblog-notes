---
title: How to produce bibliographic metadata for your web page?
author: Peter Baumgartner
date: '2019-06-19'
categories:
  - how-to
tags:
  - zotero
slug: how-to-produce-bibliographic-metadata-for-you-web-page
description: 'The tutorial explains how to use Zotero to produce and embed bibliographic metadata into your web page. An annotated screenshot illustrates each of the 14 simple steps.'
disable_comments: no
draft: no
---

## Requirements

In this tutorial, I will show how to produce and embed bibliographic metadata into your web page. To follow this guide, I assume that 

1. you have installed the standalone version of [Zotero](https://www.zotero.org/).
2. you have installed the appropriate [Zotero connector](https://www.zotero.org/download/) (plugin) for your browser.
3. you have a working knowledge how to use Zotero (There are many (video) instructions on the internet, see for instance the 'official' [Zotero Quick Start Guide](https://www.zotero.org/support/quick_start_guide) or the [introduction by the Idaho State University](https://isu.libguides.com/zotero)).

## Bibliographic metadata in 14 small steps

1. Start Zotero and your browser. Go to the page where you want to embed the metadata. You see the Zotero icon for web pages in the place where your web browsers shows the symbols for its installed extensions.
<img class="border shadow" src="/tutorial/2019-06-19-coins.files/zotero-coins-01-min.png" alt="Screenshot of the target web page for embedding bibliographi metadata." width="60%" />
<figcaption><h4>**Figure 01:** Target web page for embedding bibliographi metadata.</h4></figcaption>

2. Click on the icon and download the rudimentary bibliographic information for the web page.
<img class="border shadow" src="/tutorial/2019-06-19-coins.files/zotero-coins-02-min.png" alt="Screenshot shows the menu to download the rudimentary bibliographic information with Zotero" width="60%" />
<figcaption><h4>**Figure 02:** Download the rudimentary bibliographic information with Zotero</h4></figcaption>

3. Change to Zotero and inspect the new downloaded entry. You will notice that many details are still missing.
<img class="border shadow" src="/tutorial/2019-06-19-coins.files/zotero-coins-03-min.png" alt="Sreenshot of the Zotero bilbiograpy with the new downloaed biobliographic entry." width="60%" />
<figcaption><h4>**Figure 03:** Zotero bilbiograpy with the new downloaed biobliographic entry. </h4></figcaption>

4. Change the item type to an appropriate value: in my case "Blog Post". You will see that the Zotero icon changes to reflect the new value.
<img class="border shadow" src="/tutorial/2019-06-19-coins.files/zotero-coins-04-min.png" alt="Annoted screenshot explains missing bibliographic information." width="60%" />
<figcaption><h4>**Figure 04:** The standard web page entry misses many information in its bilbiographic record.</h4></figcaption>

5. Add the relevant information as shown on the screenshot.
<img class="border shadow" src="/tutorial/2019-06-19-coins.files/zotero-coins-05-min.png" alt="Screenshot shows the information added." width="60%" />
<figcaption><h4>**Figure 05:** Adding information into the bibliographic record.</h4></figcaption>

6. When you bibliographic entry is complete you can start the conversion and export procedure. Open the context menu (on MacOS is it a right mouse click).
<img class="border shadow" src="/tutorial/2019-06-19-coins.files/zotero-coins-06-min.png" alt="Screenshot show opening of the context menu of the bibliography entry to start the export" width="60%" />
<figcaption><h4>**Figure 06:** Opening the context menu of the bibliography entry to start the export.</h4></figcaption>

6. From the appearing drop down menu choose the "COinS" translator.
<img class="border shadow" src="/tutorial/2019-06-19-coins.files/zotero-coins-06a-min.png" alt="Screenshot shows choosing COinS as export translator." width="60%" />
<figcaption><h4>**Figure 07:** Choose COinS as export translator.</h4></figcaption>

7. Save the converted data in a file on your hard disk. The place is not essential as we only need the text inside the file. After we have copied the COinS data into our web site, we will delete our intermediary file.
<img class="border shadow" src="/tutorial/2019-06-19-coins.files/zotero-coins-07-min.png" alt="Screenshot shows preparation of saving the converted information." width="60%" />
<figcaption><h4>**Figure 08:** Prepare to save the converted information.</h4></figcaption>

8. File name and file extension are also irrelevant. Just check if your export format is "COinS".
<img class="border shadow" src="/tutorial/2019-06-19-coins.files/zotero-coins-08-min.png" alt="Screenshot shows MacOS Save File dialog window with export mode 'COinS'." width="60%" />
<figcaption><h4>**Figure 09:** MacOS Save File dialog window with export mode "COinS".</h4></figcaption>

9. Open the exported file with your text editor and select the COinS HTML code.
<img class="border shadow" src="/tutorial/2019-06-19-coins.files/zotero-coins-09-min.png" alt="Screenshot shows exported COinS code in a text editor." width="60%" />
<figcaption><h4>**Figure 10:** Exported COinS code as it is seen after opening the file with a text editor.</h4></figcaption>

10. Copy and paste the code in the source code of your web page. Again, the place does not matter. On a life web page visitor do not see these code but only the result -- the particular Zotero icon.
<img class="border shadow" src="/tutorial/2019-06-19-coins.files/zotero-coins-10-min.png" alt="Screenshot shows how the exported COinS code is inserted into the HTML source code of the web page." width="60%" />
<figcaption><h4>**Figure 11:** Embed the exported COinS code into the HTML source code of the web page.</h4></figcaption>

11. Now inspect you life web page. You will see that the Zotero icon has changed from "Web Page" to "Block Post". Congratulation you made it! 
<img class="border shadow" src="/tutorial/2019-06-19-coins.files/zotero-coins-11-min.png" alt="Screenshot of life inspection of the modified web page." width="60%" />
<figcaption><h4>**Figure 12:** Inspection the modified web page.</h4></figcaption>

12. We need to check if everything works as intended. Save the new generated bibliographic metadata into your zotero database.
<img class="border shadow" src="/tutorial/2019-06-19-coins.files/zotero-coins-12-min.png" alt="Screenshot shows download of the new generated metadata." width="60%" />
<figcaption><h4>**Figure 13:** Download of the new generated metadata to test if everything works as intended. </h4></figcaption>

13. Check if all the bibliographic metadata are imported correcty.
<img class="border shadow" src="/tutorial/2019-06-19-coins.files/zotero-coins-13-min.png" alt="Screenshot shows how the modified bibliographic entry is inspected in Zotero." width="60%" />
<figcaption><h4>**Figure 14:** Inspection of the modified bibliographic record in Zotero</h4></figcaption>

## Wrapping up and additional information 
<img class="floatright" src="/tutorial/2019-06-19-coins.files/zotero-menu-item-type-min.png" alt="Zotero drop down menu of different types of bibliographic entries." />

You have learned to create, embed, and download bibliographic metadata from those web pages where you have access to the source code. There are further options in addition to what I have demonstrated in the tutorial:

+ _You are not limited to the item type "Block Post":_ You can choose from all the 34 different types of bibliographic entries. But watch out: Every item type has its (slightly) different input form and Zotero icon. You need to know what kind of information each bibliographic record type needs. 
+ _You are not limited to one COinS entry:_ You can generate and embed as many bibliographic entries you want. If your web page has a list of references, you can offer visitors of your web page to download the bibliographic information for the full bibliography. The Zotero icon changes to a folder if there is more than one bibliographic entry to download.
+ _You do not need to generate a COinS entry by yourself if the bibliographic entry has a DOI:_ I do not know how this works, but Zotero evidently recognizes DOI entries. See as an example, my [blog post about data science education](https://notes.peter-baumgartner.net/2019/06/18/data-science-education-with-coursera/).
