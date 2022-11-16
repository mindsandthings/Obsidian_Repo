---
created: 2022-11-14T09:17:54 (UTC -08:00)
tags: []
source: https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3
author: Jan Wright
---

# Looking for needles in a haystack: how do ebook reader applications handle active indexes? Part 4 – smartphones | Indexer (The)

> ## Excerpt
> Indexes in ebooks can be ‘active’, with hyperlinks into the text. Should these links go to the page, paragraph, line or word level? This is a complex question, but the main concern may be the user ...

---
Publication: The Indexer: The International Journal of Indexing

Volume 39, Number 1

## Abstract

Indexes in ebooks can be ‘active’, with hyperlinks into the text. Should these links go to the page, paragraph, line or word level? This is a complex question, but the main concern may be the user interface in ebook reader applications. In this last article of a four-part series, Mary Coe and Jan Wright report on their investigation of how active ebook indexes are handled by applications on smartphones. They conclude that smartphone applications perform reasonably well but do not handle all levels of locator specificity with precision and that small smartphone screens can lead to problems with index display and use. They also conclude the series with a summary of their findings across all ereading applications and devices. (See also the other articles in this series – the first part on Web-based browser ereader applications in _The Indexer_ 37(2), pp. 125–40; the second part on dedicated ereader devices in _The Indexer_ 38(1), pp. 29–44; and the third part on tablet devices in _The Indexer_ 38(3), pp. 271–89.)

## Introduction

Locators are fundamental components of indexes. In book indexes, they are usually page numbers, which means the reader must search a page’s worth of text to find the information; however, in ebooks, entries can be hyperlinked to the page, paragraph, line or word. When creating these active ebook indexes, what is the best practice for linking? Should we link entries to the page, paragraph, line, or word level? This is a complex question for many reasons.

•

_Index users_ Until we have usability studies, we really do not know which location users would prefer, or whether they will notice the differences between these levels of precision. And, as we will see, users may have trouble predicting where the index links lead to in the text.

•

_Publisher and author preferences_ Publishers may dictate where the entries may be placed and may not understand the differences. Authors and editors may prefer to have entries placed in front of a term, only to find during revisions that it is hard to work around the index entries. Translators may also find it hard to work around coding that is placed in the middle of sentences and would prefer paragraph-level entries. The software prescribed by the publisher for indexing the book and placing the codes may not give the indexer a choice of precision.

•

_Devices and ebook display software_ Perhaps most importantly, the devices and applications that we are using to read ebooks may not display our hyperlinked indexes in the most useful way for users.

Ebooks can be viewed on a stand-alone ebook reader, such as a Kindle or Nook, but they might also be displayed on another device, such as a personal computer (PC), tablet or smartphone.<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#fn1" role="doc-noteref" id="body-ref-fn1">1</a></sup> Some ebooks are in a reflowable format, such as EPUB, which means that they adjust to fit the size of the screen being used. This is a nifty feature, but it creates problems for the concept of a ‘page’. Obviously, a ‘page’ will not look the same on the small screen of a smartphone as it will on the large screen of a PC, nor will it have precisely the same amount of text as the print version. And, in order to read a book on any of these devices, the user will need an ebook reader application, which might display ‘pages’ differently. This might seem like a good argument for linking the index to a level other than the ‘page’ (such as to the paragraph, line or word) as long as ebook reader applications recognize these subtle differences.

To test how ebooks are displaying targeted information from hyperlinked indexes, we created an ebook in Adobe InDesign Creative Cloud (CC) 2018, and converted it to EPUB2 with Calibre 3.37. We then created an Amazon Kindle-compatible file (MOBI) by using Amazon’s KindleGen. The public-domain books both have a hyperlinked index that is linked to several levels (page, paragraph, word). The first third of the book has entries linked to the top of the page’s display in print format, the second third has index entries linked to the beginnings of paragraphs, and the third part of the book has entries linked to the terms directly. Thus the index locators, when clicked, will take readers to less targeted or more targeted views of the wanted text, at least in theory. The ebook is in a reflowable format, so the ‘page’ level was arbitrary and based on the presentation of the ebook in InDesign before it was converted to the EPUB and MOBI formats. We then tested the EPUB and MOBI files on several dedicated ereader devices to find out how they would handle the index links at various levels.

In the first article in this series ([Coe and Wright, 2019](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#core-R2)), we looked at the entries as they were in the files that created the ebook and at how they displayed in personal-computer ereader applications and in Web-browser-based applications. In the second article, we looked at dedicated ereader devices ([Coe and Wright, 2020a](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#core-R3)), and in the third part, we tackled tablet computer applications ([Coe and Wright, 2020b](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#core-R4)). In this last part of the series, we look at ereader applications on smartphones.

Focusing on smartphone applications for ereading led to as much variation in display as the browser- and tablet-reading applications discussed in previous articles. Due to the numbers of operating systems, devices and app versions, there are many variables that affect the performance of ereader apps on smartphones. For that reason, we comment more on how the index was displayed, how it can be accessed and general navigational issues (as done previously with the tablet apps in Part 3 of the series: Coe and Wright, 2020b). Here are some of the navigational tools and features available to users in ebook reading apps on smartphone devices (these are similar to the features considered with tablet devices):

•

_Index_ If the publisher includes a set of pages containing an index, it can be displayed in the ebook, and if the publisher hyperlinks the locators into the text, these can act as navigation. A specially coded alphabetical navigation bar may also be displayed within the index that allows the user to jump to other sections of the index quickly.

•

_Last-visited page display_ This feature allows the user to instantly return to the last page viewed, similar to Web browser ‘back’ buttons. This can potentially make it easier to navigate back to the index, particularly when following multiple hyperlinked locators into the text.

•

_Page scroll_ This may include buttons, swipe motions or taps that allow the user to move between screens.

•

_Progress bar_ This can be a quick way for a reader to navigate to not-very-specific areas of the ebook. It can also be a good way to move around the book and could be used to get to the index at the back of the book quickly.

•

_Search_ A full-text search function can be accessible by a special feature in the app, usually an icon. Some searches take the reader location by location through the text, but the most helpful search functions will display a screen with a snippet of text showing the context of the term at that location, allowing the reader to choose the most appropriate location.

•

Table of contents (ToC) This can be produced in two ways:

1.

As a reproduction of the book’s ToC pages, i.e. if the book’s designer included a set of ToC pages, these are often reproduced in the ebook, and sometimes hyperlinked.

2.

If the book’s designer built the metadata for a ToC file (a special file that ereader apps can display independently of the ebook’s normal pages), this can be displayed quickly by a special feature in the app, usually by touching an icon or selecting from a drop-down menu.

## Index entry locations

To get a good idea of exactly where the entries are in the original files for the book, Figures 1 to 3 show the exact location of the entry codes (or markers, as they are called in InDesign). Markers in InDesign look like small blue arrows, allowing one to identify their location.

### Page level

This index entry for Joseph Acosta was linked to the top of the print page, right after the word ‘Chocolate’ in the title ([Figure 1](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F1)). This is page 15 in the book’s file. We are not using the page 16 hyperlink in this test.

Acosta, Joseph, 15, 16

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.3/asset/7f299b61-ec65-4e4c-8770-7e88291d2fd5/assets/graphic/indexer_2021_3_fig1.jpg)

Figure 1. Page-level entry in InDesign text

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F1)

### Paragraph level

This index entry about the colour of roasted beans was linked to the beginning of the paragraph, in between the words ‘after’ and ‘roasting’ ([Figure 2](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F2)).

cacao beans, colour of, roasted, 118

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.3/asset/b0806424-6d8c-4ac4-a80d-c909b115eae4/assets/graphic/indexer_2021_3_fig2.jpg)

Figure 2. Paragraph-level entry in InDesign text

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F2)

### Term level

This cocoa tea index entry was linked directly to the words in the text, right after the words ‘cocoa tea’ ([Figure 3](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F3)).

cocoa tea, 147

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.3/asset/33228433-9493-4dec-bf87-2c40807783a2/assets/graphic/indexer_2021_3_fig3.jpg)

Figure 3. Term-level entry in InDesign text

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F3)

## Smartphones

A variety of ereader apps were tried on an iPhone SE and an Android device (Samsung Galaxy), including Apple Books, Aldiko Book Reader, FBReader, PocketBook Reader, and ReadEra. As with the tablet-based apps, we found several smartphone apps that did not work, displayed the index poorly, and had navigational issues that would severely impact the user. For example, on an Android device (Samsung Galaxy 7), we tried the Moon+ reader but it was so difficult to navigate that we gave up on it quickly and have not included it here. Rather than document all these apps, we focus on those that performed better. We also focus on free apps that are easily accessible, rather than on apps such as Kobo or Kindle that require the user to set up an account and sign in to use them.

### _Apple iPhone SE (running OS13.4.1)_

#### _Apple Books_

Apple Books provides full navigation and builds a table of contents from the metadata, and the index is displayed properly. No information about the version was available, but our best guess is that this was OS13.4.1. The search function displays snippets of text in a list of results, allowing the reader to choose the place they want to go to with an idea of what they will find. Those search-function snippets also show snippets from the index, allowing the reader to see what the index has to say about a topic, and allowing easy navigation to the index if the reader wants to look at more entries. There is a progress bar, and there is the equivalent of a back button, which displays the text ‘Back to page …’. allowing the reader to easily return to where they were. Swiping, tapping or scrolling moved to the next page.

The first locator in the Acosta index entry is linked to the _page level_, and the text as displayed on the iPhone is shown in [Figure 4](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F4). Remember that this entry was embedded in the heading and Acosta’s name is above the picture. With the small screen, embedding a link at the top of a print page means that the Acosta name is shown, but if the font size was larger, it would easily slip to the next screen.

Acosta, Joseph, 15, 16

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.3/asset/81a16c4d-befe-4a4f-814f-068a3216563f/assets/graphic/indexer_2021_3_fig4.jpg)

Figure 4. Page-level entry using Apple Books on iPhone

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F4)

The locator (118) in the following index entry is linked to the _paragraph level_, and the text as displayed on the iPhone is shown in [Figure 5](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F5). The entry is accurately shown about mid-page.

cacao beans, colour of, roasted, 118

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.3/asset/3f81c68a-160d-4cec-a115-23dff9cd2c40/assets/graphic/indexer_2021_3_fig5.jpg)

Figure 5. Paragraph-level entry using Apple Books on iPhone

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F5)

The locator (147) in the cocoa tea index entry is linked to the _term level_, and Apple Books displays the text in the middle of the screen, as shown in [Figure 6](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F6).

cocoa tea, 147

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.3/asset/e69e0ff8-939c-430b-8803-f93ac467a853/assets/graphic/indexer_2021_3_fig6.jpg)

Figure 6. Term-level entry using Apple Books on iPhone

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F6)

#### _Pocket Book_

PocketBook loads books by scanning the device for ebooks, but in our case it did not find the file. Loading the book was difficult, and relied on emailing it to the device and forcing it to open in PocketBook. Unlike its tablet counterpart, there was no navigation at the bottom of the screen, the app’s internal navigation devices did not show up consistently and locked the user in the book with no way out, and the index display was horrible. As shown in [Figure 7](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F7), the index is cut off on the left margin and hard to use. The search function does not show snippets. There was no progress bar. There was no table-of-contents icon. And there was no back-button functionality. Swiping, tapping or scrolling moved to the next page.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.3/asset/785a87cf-5b22-4760-9eb4-87227ec415bc/assets/graphic/indexer_2021_3_fig7.jpg)

Figure 7. Index display using PocketBook on iPhone

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F7)

The first locator in the Acosta index entry is linked to the _page level_, and the text as displayed on the iPhone is shown in [Figure 8](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F8). Remember that this entry was embedded in the heading. Acosta’s name is not on the screen due to being further down in the paragraph.

Acosta, Joseph, 15, 16

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.3/asset/1e528875-c143-4a42-9e70-152b8a268b42/assets/graphic/indexer_2021_3_fig8.jpg)

Figure 8. Page-level entry using PocketBook on iPhone

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F8)

The locator (118) in the following index entry is linked to the _paragraph level_, and the text as displayed on the iPhone is shown in [Figure 9](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F9). The entry is accurately shown about two-thirds of the way down the page.

cacao beans, colour of, roasted, 118

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.3/asset/0f5e4571-e736-400c-bbf9-636f93282932/assets/graphic/indexer_2021_3_fig9.jpg)

Figure 9. Paragraph-level entry using PocketBook on iPhone

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F9)

The locator (147) in the cocoa tea index entry is linked to the _term level_, and PocketBook displays the text near the middle of the screen, as shown in [Figure 10](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F10).

cocoa tea, 147

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.3/asset/0ed00679-9e68-48c4-8f83-39e6f8ece281/assets/graphic/indexer_2021_3_fig10.jpg)

Figure 10. Term-level entry using PocketBook on iPhone

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F10)

### _Android (Samsung Galaxy 7 running Android 8.0.0)_

We included the following four apps in this review because they were more user-friendly than others and offered most of the features we wished to review: Aldiko Book Reader, FBReader, PocketBook, ReadEra.

#### _Aldiko Book Reader (version 3.1.3)_

Aldiko Book Reader includes an icon on the toolbar that displays a drop-down menu leading to either the metadata ToC or to a ‘go to’ function for navigating within the book. The ToC and index locators are hyperlinked, and the alphabetical navigation bar is available in the index. The full-text search function gives snippets from the text. A progress bar is available as well as a back button. Readers can move between screens using a tap motion, which created a few issues when trying to navigate and use the index on a small screen. For example, unless the hyperlinked locator was tapped directly, the app would interpret the action as a request to move between screens or display the control bar, depending upon where on the screen the tap occurred.

The Aldiko Book Reader handled the more specific locators at paragraph and page level precisely as we expected; however, it did not perform as well with the page-level entry. The first _page-level_ locator (15) from the Acosta index entry was embedded in the heading ‘Derivation of Chocolate’. As shown in [Figure 11](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F11), in the Aldiko Book Reader, the heading was displayed in the middle of the screen. As we noted earlier with the Apple Books app, embedding a link at the top of a print page means that the Acosta name is shown, but if the font size was larger, it would easily slip to the next screen. As with the tablet-based ereader apps we reviewed in Part 3, the embedding of the index entry in the heading might have been an issue here.

Acosta, Joseph, 15, 16

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.3/asset/9b9d22d9-745a-4428-bce8-bbbeb140764c/assets/graphic/indexer_2021_3_fig11.jpg)

Figure 11. Page-level entry using Aldiko Book Reader on Samsung Galaxy

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F11)

The Aldiko Book Reader displayed the relevant text from the _paragraph-level_ locator (118) appropriately at the top of the screen, as shown in [Figure 12](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F12).

cacao beans, colour of, roasted, 118

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.3/asset/dd9d66dc-f3e4-4748-ad0a-ea51885229d5/assets/graphic/indexer_2021_3_fig12.jpg)

Figure 12. Paragraph-level entry using Aldiko Book Reader on Samsung Galaxy

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F12)

And the Aldiko Book Reader also displayed the relevant text from the _term-level_ locator (147) at the cocoa tea entry nicely at the top of the screen, as shown in [Figure 13](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F13).

cocoa tea, 147

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.3/asset/1dc26100-2b52-466d-a439-f69ea630cca8/assets/graphic/indexer_2021_3_fig13.jpg)

Figure 13. Term-level entry using Aldiko Book Reader on Samsung Galaxy

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F13)

#### _FBReader (version 3.0.23)_

The FBReader app displayed the metadata ToC, which could be accessed from a drop-down menu. The index was displayed with hyperlinked locators and an alphabetical navigation bar. While a progress bar was available, there was no obvious back button or last-page-visited option. The full-text search function takes the reader from location to location in the text, highlighting terms, and it requires the reader to use arrow buttons to move between the search results. As with the Aldiko Book Reader, a tap motion is required to move between screens, which can present a few issues with trying to navigate, access the control bar, and use the hyperlinked index locators on the small display.

The FBReader app handled the various locator link levels reasonably well. It displayed the text from page- and paragraph-level locators exactly as expected; however, it did not display the text from the term-level entry as precisely.

The first locator in the Acosta index entry is linked to the _page level_, and the text as displayed on the FBReader is shown in [Figure 14](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F14). Remember that the locator is embedded in the heading, so this is exactly how we hoped it would display the text.

Acosta, Joseph, 15, 16

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.3/asset/d636e09f-85bc-4b3f-8542-b87caf23af25/assets/graphic/indexer_2021_3_fig14.jpg)

Figure 14. Page-level entry using FBReader on Samsung Galaxy

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F14)

The locator (118) in the following index entry is linked to the _paragraph level_; [Figure 15](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F15) shows how the FBReader app displays the text. Again, this is exactly as expected as the locator is embedded at the beginning of the first paragraph shown on the screen.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.3/asset/fd54251a-c0d2-43b4-9cb3-0e6b8db5f43d/assets/graphic/indexer_2021_3_fig15.jpg)

Figure 15. Paragraph-level entry using FBReader on Samsung Galaxy

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F15)

However, the locator (147) from the cocoa tea, which is linked to the _term level_, was not as precise. As shown in [Figure 16](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F16), FBReader displays the text from the beginning of the paragraph rather than from the line where the locator was embedded.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.3/asset/9cbce873-fc61-4fe7-b91a-ff7cea09499b/assets/graphic/indexer_2021_3_fig16.jpg)

Figure 16. Term-level entry using FBReader on Samsung Galaxy

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F16)

#### _PocketBook Reader (version 4.21.17970)_

The PocketBook Reader (Android version) provided the metadata ToC from a drop-down menu, displayed a progress bar, and included a back button. Moving between screens required a swipe motion, which made it easier to navigate and use the hyperlinked index than the apps that used a tap motion. It is interesting to see that the Android version was more robust than the iOS version.

The PocketBook Reader displayed the text from the locators well enough but lacked precision. For example, the first locator (15) in the Acosta index entry is linked to the _page level_, and the text as displayed on the PocketBook Reader is shown in [Figure 17](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F17). The entry was embedded in the heading ‘Derivation of Chocolate’, which is displayed in the middle of the screen. The information about Joseph Acosta is displayed at the bottom of the screen.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.3/asset/960d0e10-7424-4722-93ff-1be2be0769d6/assets/graphic/indexer_2021_3_fig17.jpg)

Figure 17. Page-level entry using PocketBook Reader on Samsung Galaxy

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F17)

The locator (118) in the following index entry is linked to the _paragraph level_ and the text as displayed on the Pocketbook Reader app is shown in [Figure 18](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F18). The relevant paragraph is located at the bottom of the screen, rather than at the top as we expected.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.3/asset/e879c757-a379-4a58-8553-afaa725becab/assets/graphic/indexer_2021_3_fig18.jpg)

Figure 18. Paragraph-level entry using PocketBook Reader on Samsung Galaxy

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F18)

The locator (147) in the cocoa tea index entry is linked to the _term level_, and the PocketBook Reader displays the text in the second paragraph down, as shown in [Figure 19](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F19). While the reader would be able to find the relevant information on the screen, this is not displayed as precisely as we expected for a term-level entry.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.3/asset/fc912d15-4f16-4654-a825-e4438f11bee3/assets/graphic/indexer_2021_3_fig19.jpg)

Figure 19. Term-level entry using PocketBook Reader on Samsung Galaxy

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F19)

#### _ReadEra (version 20.03.26 + 1150)_

The ReadEra app offered many of the features we were interested in, such as the metadata ToC available via a ToC icon and a progress bar. It also provided a full-text search function that displayed snippets from the text. However, it had a few quirks, such as forward and back buttons that moved between the beginning of chapters. And while it offered a hyperlinked index, this was not displayed well as indents for subentries and line wrapping were lost, as shown in [Figure 20](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F20).

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.3/asset/122b379a-bbdb-43a8-9b1b-ffbd60d28541/assets/graphic/indexer_2021_3_fig20.jpg)

Figure 20. Index display using ReadEra on Samsung Galaxy

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F20)

The ReadEra app also displayed the text from the locators well enough but lacked precision. For example, the first locator (15) in the Acosta index entry is linked to the _page level_, and the text as displayed on the PocketBook Reader is shown in [Figure 21](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F21). The entry was embedded in the heading ‘Derivation of Chocolate’, which is displayed towards the top of the screen; however, the information about Joseph Acosta is displayed at the bottom.

Acosta, Joseph, 15, 16

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.3/asset/8e07128d-a648-4dda-9953-59440b7e4b39/assets/graphic/indexer_2021_3_fig21.jpg)

Figure 21. Page-level entry using ReadEra on Samsung Galaxy

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F21)

The locator (118) in the entry about the colour of roasted cacao beans is linked to the _paragraph level_ and the text is displayed towards the top of the screen using the ReadEra app, as shown in [Figure 22](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F22). While this is acceptable, we would have expected the relevant paragraph to be located at the very top of the screen, as we saw with the Aldiko Book Reader.

cacao beans, colour of, roasted, 118

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.3/asset/6ad232e5-edc5-44eb-ac2f-94fa916c5f32/assets/graphic/indexer_2021_3_fig22.jpg)

Figure 22. Paragraph-level entry using ReadEra on Samsung Galaxy

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F22)

The locator (147) in the cocoa tea index entry is linked to the _term level_. While the ReadEra app displays the relevant text in the first paragraph, as shown in [Figure 23](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F23), we would prefer to see it in the first line on the screen, as with the Aldiko Book Reader.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.3/asset/48f53086-4b78-49e1-9a63-94f587cf90d0/assets/graphic/indexer_2021_3_fig23.jpg)

Figure 23. Term-level entry using ReadEra on Samsung Galaxy

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#F23)

## Smartphones: conclusion

Smartphone apps for ereading led to as much variation in display as the tablet applications discussed in Coe and Wright (2020b). Several apps worked well but lacked precision in displaying the active links at particular levels. As with tablet applications, the variety of displays on smartphones means that indexers cannot always predict where on the screen their entry text will be displayed. We also found several apps that were difficult to use or displayed the index in odd ways, which means that we may not even be sure that an index will be rendered properly or be easily accessible to users. In some cases, these issues relate to the small screen on the smartphone and the actions that users must use to interact with the index, such as tapping or swiping the screen.

## Overall summary: implications for indexing

[Table 1](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#T1) summarizes our findings on how ereader applications handled active indexes linked to various levels of specificity. In this table, each application is rated more precisely than earlier in the series. The ● symbol indicates that the application displayed the text from the hyperlink at the index entry _exactly_ as intended for the embedded markers at the page level, paragraph level, and term level. The ○ symbol indicates that the text was not presented _exactly_ as intended. In our earlier evaluations, we accepted more variation in presentation than in the ratings in [Table 1](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#T1).

Table 1. Summary of findings for all ereader applications and devices

| Device | Product name | Page level | Paragraph level | Term level |
| --- | --- | --- | --- | --- |
| **Ereader software (Part 1)** | Adobe Digital Editions | ○ | ○ | ○ |
| FBReader | ● | ● | ● |
| EPUB File Reader | ● | ● | ● |
| Calibre | ● | ○ | ○ |
| **Web browser software (Part 1)** | Readium (Chrome) | ○ | ○ | ○ |
| Epubreader (Firefox) | ○ | ○ | ○ |
| **Dedicated ereader devices (Part 2)** | Kindle (older version) | ● | ● | ● |
| Kindle Paperwhite | ● | ● | ● |
| Kindle Oasis | ● | ● | ● |
| Nook | ○ | ○ | ○ |
| Kobo | ○ | ○ | ○ |
| **Tablet devices (Part 3)** |
| Apple iPad Mini | Kindle for iPad | ○ | ○ | ○ |
| Apple iPad Books | ○ | ○ | ○ |
| Amazon Fire | Kindle Fire 10 | ● | ● | ● |
| RCA Voyager Android | PocketBook | ● | ○ | ○ |
| eReader Prestigio | ● | ● | ○ |
| AIReader | ○ | ● | ○ |
| FullReader | ○ |   | ○ |
| **Smartphones (Part 4)** |
| Apple iPhone | Apple Books | ● | ○ | ○ |
| PocketBook | ○ | ○ | ○ |
| Android (Samsung Galaxy) | Aldiko Book Reader | ● | ● | ● |
| FBReader | ● | ● | ○ |
| PocketBook Reader | ○ | ○ | ○ |
| ReadEra | ○ | ○ | ○ |

Legend: ● = text displayed as intended; ○ = text not displayed as intended

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#T1)

Overall, Kindle devices were the standout performers, presenting the desired text at the top of the screen for all levels of locator specificity. Web browser software could not present the hyperlinks with any precision. And there was great variation amongst ereader software and applications for tablets and smartphones, with many using mid-screen as the default presentation.

When working with ebooks, we have to embed index entries that will work with the poorest feature set of the ereaders, not just the richest apps – in other words, index to the lowest common display denominator. As can be seen in [Table 1](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#T1), most of these applications are not displaying things the way we think they should. So best practice is to choose the locations to embed index entries so that hyperlinks are as close as they can be. Otherwise, there is the risk of the relevant text not being displayed.

Linear non-fiction, such as the ebook that was tested here, has been transported into a world with limited navigation and, consequently, readers may have a hard time finding ways to guidepost themselves and move around the book. Indexes that are presented linearly and meant to be scanned and dipped into may not be the best choice for ereader environments. They can be hard to navigate to and from, and it can be difficult to click the right locator. Trying to develop an index that will work in both a print book and an ebook version of the same text may be leaving indexers stuck with less usable ebook indexes. It is possible to restructure the index and make it more friendly in an ebook, but until indexers start doing that, users might give up on using indexes in ebooks due to the difficulties of the interface.

The goal is to make the user happy on their first hits, reducing their work. A rule of thumb might be to remember that ebooks are not print books (pbooks). Readers have to scan in pbooks, and they will still be doing that in ebooks. However, with unpredictable displays in ebooks, there is the danger of making the reader work harder to find what they want. As a participant in Coe’s (2019) study remarked, ‘I wish it would just leap out at me.’ Highlighting a term or section in the text would make it ‘leap out’, as this reader wants, but that is a software development the ereader and app manufacturers must implement. We might also help the ebook index user out by reproducing sections of the index rather than using cross-references and by using more subheadings to reduce the number of locators at a heading. But we also have to keep in mind the size of the screen, and try not to build very long sections with lots of subheadings that are difficult to scan and navigate. It is truly a dance of trying to manage details so that the index is easy to use as well as comprehensive. Ultimately, we need to know how users _want_ to use indexes in ebooks in order to improve them, but investigations into that have only just begun ([Coe, 2019](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#core-R1)).

Based on the exploration of ebook applications reported in this series of articles, we have the following recommendations for indexers creating active ebook indexes:

•

Place the entries directly in front of indexed phrases so that they are very close to the target material. This includes placing entries at the front of headings rather than the end. Consider what might happen if the view shown to the reader does not include a bolded heading describing the section of the text they see. If you need that heading for context, place the entry in the heading. If you do not, place it in the body of the text. Be aware that the niceties of page layout may completely disappear in the ebook, and headers may not be displayed with their body text.

•

Consider your indents: due to bugs, they may be lost. Run-in indexes were not tested here, but that may be a way to avoid the loss of indents. Reconsider third-level heads.

•

Remember the difficulties of clicking the link with a finger when there is a string of locators on a tiny smartphone display. Our testers often missed on the first try, and then had to navigate back, which could be difficult. Consider using more subheadings to reduce the number of locators at a heading (but remember that headings may not be displayed correctly if indents are lost, so rethink headings at the third level and below).

•

Work with the publisher to provide more intra-index navigation. A hyperlinked A|B|C|D|E navigation bar at the head of each index section provides more opportunities to help the reader get around in the index, especially if a back button is not available.

•

Add hyperlinks from cross-references to the target index headings, but also consider cross-references carefully. Double-posting small duplicate index sections might be easier for the reader than following a cross-reference across the index. If the book is only going to be electronic, and not print, make use of the absence of space constraints to duplicate sections, allowing immediate access: e.g., give page numbers both at ‘canines’ and at ‘dogs’.

•

Ask the publisher to include the metadata for a stand-alone ToC, as that navigational tool makes the index accessible.

This is the final part of this series; however, the EPUB and Kindle ebooks used in the research are still available for download.<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.3#fn2" role="doc-noteref" id="body-ref-fn2">2</a></sup>

## Acknowledgements

Thank you to Joshua Tallent for his help with troubleshooting the creation of the Kindle ebook. His knowledge of ebooks is unsurpassed, and we greatly appreciate his willingness to share his time and expertise with us. Thank you also to Glenda Browne for her thoughtful and helpful reviews of all the articles in this series.

## Footnotes

2

The EPUB ebook will continue to be available for download from [www.wrightinformation.com/Cocoa.epub](http://www.wrightinformation.com/Cocoa.epub) and the Kindle ebook from [www.wrightinformation.com/Cocoa.mobi](http://www.wrightinformation.com/Cocoa.mobi). The capital C in the word ‘Cocoa’ is critical to get the download. These are the levels at which index entry codes have been inserted into the book: page level: pages 1–62, paragraph level: pages 63–119, term level: pages 120–73.

## References

Coe, M. (2019) ‘Canaries in a coalmine: the index and the page in ebooks’, _Script & Print_ 43(2), 69–78.

Coe, M. and Wright, J. (2019) ‘Looking for needles in a haystack: how do ebook reader applications handle active indexes? Part 1 – ereader and Web browser software’, _The Indexer_ 37(2), 23–38.

Coe, M. and Wright, J. (2020a) ‘Looking for needles in a haystack: how do ebook reader applications handle active indexes? Part 2 – dedicated ereader devices’, _The Indexer_ 38(1), 29–44.

Coe, M. and Wright, J. (2020b) ‘Looking for needles in a haystack: how do ebook reader applications handle active indexes? Part 3 – tablet devices’, _The Indexer_ 38(3), 271–89.
