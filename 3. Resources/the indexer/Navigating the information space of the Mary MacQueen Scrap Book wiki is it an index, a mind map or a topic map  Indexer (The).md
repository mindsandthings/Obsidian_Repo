---
created: 2022-11-14T09:12:27 (UTC -08:00)
tags: []
source: https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38
author: Glenda Browne
---

# Navigating the information space of the Mary MacQueen Scrap Book wiki: is it an index, a mind map or a topic map? | Indexer (The)

> ## Excerpt
> This paper discusses the use of wiki technology to provide a navigation structure for the online version of the Mary MacQueen Scrap Book, which contains newspaper clippings about the Victorian arti...

---
Publication: The Indexer: The International Journal of Indexing

Volume 39, Number 4

## Abstract

This paper discusses the use of wiki technology to provide a navigation structure for the online version of the _Mary MacQueen Scrap Book_, which contains newspaper clippings about the Victorian artist. After outlining the architecture of the wiki, the navigation structure is discussed and several questions are posed: is the navigation structure an index? If so, what type? Or is it just a linkage structure or topic map? Does such a distinction really matter? Are these definitions in reality function-based?

## Introduction

In 2020, the Cultural Conversations project<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#fn1" role="doc-noteref" id="body-ref-fn1">1</a></sup> published an interview with Victorian artist Mary MacQueen (The MacQueen Conversation<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#fn2" role="doc-noteref" id="body-ref-fn2">2</a></sup>), who is renowned for her drawing, printmaking and mixed media works on paper. She exhibited regularly between 1944 and 1996. MacQueen clipped any articles (or part thereof) mentioning her name and pasted them into a scrapbook. This scrapbook provides a fascinating insight into the history of the visual arts in Victoria, Australia, since the 1940s, highlighting the development of careers through exhibitions, as seen through MacQueen’s eyes.

This article discusses the development of the navigation structure and its attributes, facilitating access to the online version of the scrapbook (The Mary MacQueen Scrap Book<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#fn3" role="doc-noteref" id="body-ref-fn3">3</a></sup>) for the following items of interest: people’s names, place names, organisation names, exhibition names and years. This digital version was created as an accompaniment to the conversation mentioned above.

We discuss the architecture of the navigation structure and the development of a specific tool to assist in the capturing of this structure and minimising the development workload. We conclude by posing the following question: is this structure just a navigation structure or topic map, or a cross-reference, or can it be classed as an index in its formal meaning?<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#fn4" role="doc-noteref" id="body-ref-fn4">4</a></sup>

## Wiki architecture

The development of the wiki commenced with the scanning of each scrapbook page into a JPEG file.<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#fn5" role="doc-noteref" id="body-ref-fn5">5</a></sup> This 173-image collection was then imported into a wiki developed using TiddlyWiki software.<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#fn6" role="doc-noteref" id="body-ref-fn6">6</a></sup> TiddlyWiki is an early example of a web application, one built entirely of web technologies running in an online environment. It is unique in that it is built to run from the user’s computer’s local disc drive, allowing the saving of changes but, as a web application, it can also be hosted on a web server (with the limitation that changes cannot be easily saved).<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#fn7" role="doc-noteref" id="body-ref-fn7">7</a></sup> TiddlyWiki has extended beyond its initial vision and now has an extensive and active international development group.

The wiki architecture is simply a single html page consisting of many content elements, called ‘tiddlers’, which are implemented as HTML Div elements. Their content and visibility are manipulated by the wiki software. From a technology perspective, TiddlyWiki is built from the international standards HTML, CSS and Javascript, and some external Javascript libraries.

There are several tiddler types: Scrapbook Page tiddlers, People tiddlers, Places tiddlers, Organisations tiddlers, Exhibitions tiddlers, Years tiddlers and Information tiddlers. There is also a set of system tiddlers as part of the TiddlyWiki software, but these are not discussed here.

### Scrapbook Page tiddlers

Each Scrapbook Page tiddler has the following elements (as illustrated in [Figure 1](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F1)):

•

a page number as provided by MacQueen

•

a title, e.g. Page 147, being the representation of the physical page numbered 147

•

a set of ‘tags’ (discussed below)

•

the JPEG image of the physical page

•

a hyperlinked alphabetical list of names of people, places, organisations and exhibitions mentioned in any clipping on the page, and the year the clippings refer to (scrapbook pages can have clippings from multiple years, as discussed below).

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.38/asset/3a392cd1-79ad-4b4a-b25f-961d342e2351/assets/graphic/indexer_2021_38_fig1.jpg)

Figure 1. A Scrapbook Page tiddler <sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#fn8" role="doc-noteref" id="body-ref-fn8">8</a></sup>

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F1)

### Tags

Tags are information elements that create categories of tiddlers based on their content. For example, each scrapbook tiddler has a Pages tag which collects all tiddlers sharing this tag into a category set. The category set is also displayed in the table of contents (discussed below and shown in [Figure 6](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F6)).

The wiki development identified the following tags: Pages, People, Places, Organisations, Exhibitions and Years, corresponding to the content types found. These category names are also listed as part of the wiki’s table of contents (see [Figure 6](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F6) below), allowing the user to click a category name to see its content in total or expand the category list inside the table of contents to directly access a single tiddler. Tags are identified by the grey-coloured buttons near the top of a tiddler display (in the live wiki, tags are coloured orange and hyperlinks are blue and underlined).

The source text linking to a tiddler may be different in multiple Scrapbook Page tiddlers. For example, the link to Eric Thake’s tiddler (see [Figure 2](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F2)) could just be using his surname, Thake, E. Thake, Eric Thake or his full name, and so on. This is also true for the other tiddlers.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.38/asset/eb3d5c1b-5e69-40b2-a2f8-88c72cf49445/assets/graphic/indexer_2021_38_fig2.jpg)

Figure 2. An example of a People tiddler<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#fn9" role="doc-noteref" id="body-ref-fn9">9</a></sup>

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F2)

Tiddler titles have been standardised to allow resolving of various source texts to the correct target tiddler. One might consider the target tiddler titles to form a type of ‘controlled vocabulary’ or name authority. For example, the People tiddler title is in the form Surname Given Names Date of Birth–Date of Death, and these values are taken from the Australia Art Sales Digest, or the Centre for Australian Art if the Digest has no entry. The remaining tiddler types’ titles are essentially the name of the real-world object: for example, Flinders Street, Art Gallery of New South Wales and so on.

There are also links to external sources of information. The three sources supported are the Australia Art Sales Digest, the National Gallery of Australia’s Centre for Australian Art and the Dictionary of Australian Artists Online. For those persons having a published conversation via the Cultural Conversations project, there is also a link to their published conversation.

### People tiddlers

[Figure 2](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F2) shows an example of a People tiddler, with its title giving the person’s surname, given names and dates of birth and death. For those entries where the specific details are ambiguous, such as the People tiddler in [Figure 3](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F3), we try to provide links to more detailed tiddlers based on the surname. It is not possible to determine whether any of these are valid, hence the statement ‘could also possibly be’. As can be seen in this example, there are two entries to Campbell, on pages 028 and 110, but no further information is available to specifically identify the Campbell concerned. So links are provided to other persons sharing the surname. This cross-referencing is done automatically by software we have written.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.38/asset/dea65dbe-8ea2-4ede-b49a-2a7079ff0a86/assets/graphic/indexer_2021_38_fig3.jpg)

Figure 3. An ambiguous People tiddler<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#fn10" role="doc-noteref" id="body-ref-fn10">10</a></sup>

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F3)

### Places/Organisations/Exhibitions tiddlers

The wiki uses separate tiddlers for cross-referencing the names of places, organisations and exhibitions. As detailed in [Figure 4](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F4), showing an example of a Places tiddler, such information is minimal, just listing tiddlers mentioning the subject, with no links to external content except for exhibitions (if any such links are discoverable). The only difference between these tiddlers is that they have a different tag allocating them to the appropriate category, i.e. Places, Organisations or Exhibitions.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.38/asset/54362d36-a226-48b8-ba0e-c69c38332f9b/assets/graphic/indexer_2021_38_fig4.jpg)

Figure 4. An example of a Place tiddler<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#fn11" role="doc-noteref" id="body-ref-fn11">11</a></sup>

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F4)

### Years tiddlers

Similarly to a Places tiddler, a Years tiddler ([Figure 5](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F5)) provides details of all clippings from that particular year. There is no tag for the year, as this would duplicate the Years tiddler itself, and thus present needless complexity.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.38/asset/af022166-6b77-4a68-b3dd-6767a929b9d6/assets/graphic/indexer_2021_38_fig5.jpg)

Figure 5. An example of a Year tiddler<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#fn12" role="doc-noteref" id="body-ref-fn12">12</a></sup>

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F5)

### Table of Contents tiddler

TiddlyWiki provides a special facility to develop a table of contents. Adding the tag _Index_ to any tiddler lists that tag in the table-of-contents area of the display (accessed via the _Contents_ tab). As illustrated in [Figure 6](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F6), the arrows on the left of an entry signify that the entry consists of a list of sub-elements. Clicking the arrow, so that it turns into a down-facing arrow, expands the list and an individual entry can be accessed by clicking on its name in the sub-list. In the example shown, the Information entry has been expanded, as has the People entry.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.38/asset/26c35076-b493-419f-8ce8-f021cb71881a/assets/graphic/indexer_2021_38_fig6.jpg)

Figure 6. Table of Contents tiddler<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#fn13" role="doc-noteref" id="body-ref-fn13">13</a></sup>

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F6)

## The development tool

When development of this wiki began, it was soon recognised that individual links might be duplicated many times and this would be a time-consuming activity to manage manually. To assist, a tool was developed in Filemaker Pro.<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#fn14" role="doc-noteref" id="body-ref-fn14">14</a></sup> The architecture is very simple: two main tables, one listing all entries made to date, and one listing entries for the current scrapbook page being processed (see [Figure 7](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F7)). The second table is emptied on completion of the page being processed. There are additional tables to detect duplicate entries from the current scrapbook page, duplicate tag names and link contents.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.38/asset/7879198e-f246-447c-bf70-908e432fdc88/assets/graphic/indexer_2021_38_fig7.jpg)

Figure 7. The tool architecture

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F7)

### Names List table

The Names List table, which lists all entries made to date, is displayed in [Figure 8](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F8). The table allows for different entries in scrapbook clippings to be mapped onto identical details tiddlers. For example, clipping entries such as _Flinders Street_ and _Flinders St_ would resolve to the tiddler _Flinders Street._ This accommodates the writing styles of the various authors. This was seen most often with names of places and people. With names of people, the name of the person might be misspelled, or only listed as a surname. In each case, detection of such matters would allow mapping to the same People tiddler.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.38/asset/3b525cd7-5f35-44d5-9c24-cb5642bd5a65/assets/graphic/indexer_2021_38_fig8.jpg)

Figure 8. Names List table

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F8)

[Figure 9](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F9) shows in more detail how a name item is entered into the tool. The user would do the following:

•

copy the link from the Australia Art Sales Digest, the Centre for Australian Art and the Dictionary of Australian Artists Online.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.38/asset/b29acfa1-27ab-4fb7-9b0c-fa62dd64a18b/assets/graphic/indexer_2021_38_fig9.jpg)

Figure 9. Entering a name item into the development tool

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F9)

The tool automatically generates the code to link to the detail tiddler as well as identifying any duplicates, either on the current page or on those provided previously. For duplicates, the appropriate link code would be inserted with the external links left empty, as they would have already been defined on the detail tiddler. As mentioned above, target tiddler titles implement a type of ‘controlled vocabulary’. This tool highlights such control by recording the various formats of source labels and their resolution to target titles and highlighting potential target tiddlers based on source tiddler labels. This has been shown to reduce the time for establishing the navigation structure considerably.

### Links list

The tool also supports the automatic creation of the links list found below the page image of a page tiddler ([Figure 10](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F10)). This is merely an alphabetical list of entries found in clippings on that page. This list is merely copied and pasted into the page tiddler source. The format for a link is ‘source text|target title’, enclosed in double square brackets. These values are inserted by the tool automatically from entered data. The double asterisk displays as an indented list.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.38/asset/77f3ffa2-4fd8-49fb-9615-b7903f8847a2/assets/graphic/indexer_2021_38_fig10.jpg)

Figure 10. Links list generated by the tool

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F10)

Once the current page has been processed, the tool enables the code for each new detail tiddler to be copied and pasted into the wiki as a new tiddler. The content of this new tiddler can be seen in the ‘Tiddler text’ field in [Figure 11](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F11). The tag to be inserted into the current page tiddler is also automatically generated from the Name Type field, in [Figure 11](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F11), and simply copied into the Tags area of the page tiddler.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.38/asset/5c879903-d770-4aef-a4ef-724235610659/assets/graphic/indexer_2021_38_fig11.jpg)

Figure 11. Generated tiddler code

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F11)

## The navigation structure

The discussion so far has focused on the creation of the appropriate content elements and links to support navigation through the scrapbook. We will now discuss the characteristics of this navigation architecture, which is illustrated in [Figure 12](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F12). Can it be considered an index, a mind map or a topic map?

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.38/asset/899fc957-1ae9-4d29-bb52-4f0525f76683/assets/graphic/indexer_2021_38_fig12.jpg)

Figure 12. Navigation structure of the wiki

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F12)

Each scrapbook tiddler has a ‘previous’ and ‘next’ button (as shown in the top right corner of the scrapbook tiddler in [Figure 1](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F1) above), identified by << and >> signs. Clicking on these will change the tiddler display to the previous/next sequential scrapbook page, much like turning the page in a physical book. Similarly, the table of contents (see [Figure 6](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F6) above) facilitates sequential navigation through the various tiddler categories. It looks very similar to a back-of-the-book index, with five main entries and multiple subentries.

Non-sequential access is supported by the various tiddler category sets (People, Places, Organisations, Exhibitions and Years), by the alphabetic listing below the scanned image of each scrapbook page and by the table of contents, as well as by a general searching capability, which allows use of any combination of words in a tiddler.

Each of the tiddler types depicted in [Figure 12](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F12), with the exception of the Scrapbook Page tiddlers, is essentially part of the navigation structure. So each tiddler type serves as an ‘index’ element as well as a content element. The Scrapbook Page tiddler is excluded from this categorisation as these tiddlers are the start/end of navigation actions. The four grey-coloured elements are the actual pages on the Internet provided by the Internet services so named and thus are end nodes of the structure (or doorways into further details from the Internet).

Information retrieval has over many years developed many ever-more-sophisticated techniques for allowing a reader to find the information they are after in increasingly larger and more complex information spaces. One of the earliest techniques was page numbering. [Manguel (1996](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#core-R10): 48) describes how early Roman ‘rolls’ were folded into pages which could be numbered to allow the reader easier access to various sections:

> Paul’s Epistles, as read by Augustine, were not a scroll but a codex, a bound papyrus manuscript in continuous writing, in the new uncial or semi-uncial hand which had appeared in Roman documents in the last years of the third century. The codex was a pagan invention; according to Suetonius, Julius Caesar was the first to fold a roll into pages, for dispatches to his troops. The early Christians adopted the codex because they found it highly practical for carrying around, hidden away in their clothes, texts that were forbidden by the Roman authorities. The pages could be numbered, which allowed the reader easier access to the sections, and separate texts, such as Paul’s Epistles, could be easily bound in one convenient package.

[Baron (2015)](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#core-R2) describes how page numbering in printed books initially came about as an aid to printers to assist in the collation of the physical, individual pages. Page numbers were a requirement for the development of indexes and tables of contents. More recently, increasingly sophisticated techniques have been employed to make non-sequential access easier as the size and complexity of information spaces increased. These techniques have included indexes, cognitive maps, mind maps, concept maps, thesauri, taxonomies and, more recently, topic maps, as well as various techniques developed in library science. Cognitive maps, concept maps, taxonomies and thesauri are not discussed here, as it is doubtful that this wiki could be said to implement any one of these according to their formal definitions. It is more likely that some part of the navigation structure could resolve onto one or other of these technologies.

### Index

An index is defined as:

•

a list (as of bibliographical information or citations to a body of literature) arranged usually in alphabetical order of some specified datum (such as author, subject, or keyword) (Merriam-Webster, 2021)

•

an alphabetical list, such as one printed at the back of a book showing which page a subject, name, etc. is on or a collection of information stored on a computer or on a set of cards, in alphabetical order (Cambridge Dictionary, n.d.)

•

a systematic guide to facilitate retrieval of content (ANSI/NISO, 2021).

The term ‘index’ is also commonly employed to describe the technology used in computerised text retrieval through the building of content elements and pointers to their source in the object being searched. In this scenario, an index could be a list of terms, possibly configured into digraphs – any pair of adjacent letters. The STATUS software<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#fn15" role="doc-noteref" id="body-ref-fn15">15</a></sup> ([Coleman, 1976](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#core-R6); [Niblett and Price, 1969](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#core-R12)) implemented a three-level digraph index to identify the location of any word in a document collection.<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#fn16" role="doc-noteref" id="body-ref-fn16">16</a></sup>

The navigation structure of the _Mary MacQueen Scrap Book_ could be said to be an index according to these definitions, but should more likely be considered as a multiple-index object. The tag-based categories each make up an index, as does the table of contents. These indexes work separately from each other and also in unison to facilitate various mechanisms of navigation. Each index is essentially a flat structure ignoring the capabilities available through TiddlyWiki in linking through different elements, and the fact that, in a traditional index, linkages are one-way, whereas the TiddlyWiki capability is for multi-way navigation.

### Mind maps

A mind map is the simplest and most straightforward type of cognitive map, a tree that represents a central topic and its subtopics. As discussed by [Gibbons (2019)](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#core-R9), mind maps are characterised by the following:

•

a clear organisation and structure, with clear directed flows from the central node to leaf nodes

•

one central topic, thus limiting the scope of the map

•

no definition of the relationships between nodes.

It is our belief that a mind map is a construct that represents the structure or orientation of the central topic. [Winchester (2021](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#core-R14): 39) describes a mind map in this way: ‘And he \[a hunter–gatherer\] also had to come to know, if only for his own survival, some details of his orientation – of where he was, in relation to everywhere else around him … If only in his mind, he had to have a map.’ The important detail here is that of orientation. The map does not focus on topics or subjects, but on the lie of the land – the orientation, or the structure of the space. In a similar way, the mind map of this wiki provides details as to its structure, its orientation. The central theme is not the details tiddlers, the subjects or topics, but on which page to find a clipping, or to follow a link to a details tiddler and from there to perhaps another page (clipping) and/or an external web page.

The whole scrapbook could be said to be a mind map, one small part of MacQueen’s mind map covering her entire professional career, as it represents one central topic, namely MacQueen’s interest in comments about her (through the clippings), with directed links to each clipping via pages and directed links to the various levels of sub-elements, names and so on. This structure is clear and simple. In the case of this wiki, relationships are implicitly labelled by the source text, and the directed flow characteristic is disobeyed because of TiddlyWiki multi-way capabilities. The mind map does not detail attributes of a relationship, such as what the comment about Eric Thake was on the clipping found on page 002 (see [Figure 13](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F13)). That, in our mind, would elevate the mind map more into a type of topic map (see the discussion of topic maps below).

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.38/asset/42fc3f9f-a395-4e4e-91d6-14c051233591/assets/graphic/indexer_2021_38_fig13.jpg)

Figure 13. A small part of the mind map for Thake Eric Prentice Anchor 1904–?

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F13)

It should be recognised, though, that the external links to the Australian Art Sales Digest, and the other sources, have been added _after_ MacQueen detailed her clippings book and so are not strictly part of her mind map, as these elements would not have existed during her lifetime. These elements have been added as an aid to current and future researchers/students to provide more information about people, exhibitions and so on.

### Topic maps

[Garshol (2004)](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#core-R8) describes topic maps as having

> originated in work on the merging of electronic indexes and so are very much a subject-based classification technique. In fact, topic maps are organised around topics, and each topic is used to represent some real-world thing … topics represent concepts, the same way terms in an indexing language refer to concepts. In topic maps the concepts are called subjects, and the standard emphatically states that a subject can be ‘anything whatsoever’.

Unlike mind maps, a topic map focuses not on the orientation of the elements within the information space but on the semantics of the elements and their relationships, providing an aid to finding a specific element based on its semantics or content.

[Garshol (2004)](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#core-R8) states that ‘topic maps are organised around _topics_, and each topic is used to represent some real-world thing’. Taking this point of view, the real-world things represented by topic map(s) of this wiki would be the details tiddlers, occurrences of People, Places, Names, Exhibitions and Years (see [Figure 14](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F14), noting the altered orientation of the map from its equivalent mind map in [Figure 13](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F13)).

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.38/asset/36f82ed9-7a8e-4969-a59c-572f132c23e9/assets/graphic/indexer_2021_38_fig14.jpg)

Figure 14. A topic map for Eric Thake

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#F14)

It is envisaged that someone coming to this wiki would most likely be interested in finding out what information is available about a person, place, exhibition or organisation, or what clippings are available for any year. So their initial entry point will be the details tiddlers. These are not orientation queries; they are content-based queries. To determine what MacQueen thought about this time of her professional career is not something easily determined through a topic map or a mind map, but through the exploration and in-depth research through the complete clippings set.

Occurrences (i.e. the details tiddlers) relate topics to the information relevant to them. They indicate what clippings and information resources contain information about them. The topic map specification allows for the typing (categorisation) of relationships between elements. This typing can be used to document the semantics of a relationship. This allows many kinds of relationships to be represented. With the exception of the external linkages, linkages/relationships are not typed; in fact, no relationships are specifically named. The shallow structure implies the relationship details: Page contains Clippings; Clippings mention People, Places, Organisations and Exhibitions; Clippings relate to a specific year.

### An indexer’s viewpoint on the wiki

To a carpenter, everything looks like a nail, and to an indexer, every A-to-Z navigational tool looks like an index. There are, however, many types of index, and different technical and conceptual approaches that are taken in their creation. As discussed above, analysis of the MacQueen Scrapbook index suggests that it has elements of mind maps and topic maps, supported by the use of a controlled vocabulary/name authority.

[Biezunski (2018)](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#core-R3) points out that the topic maps model was invented to incorporate indexes with emerging technologies, and drills to the core of indexing. [Provo (2019)](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#core-R13) describes the use of topic map concepts in the Enhanced Networked Monographs experimental project, in which topics were extracted from indexes, and tools were built to create a platform for reading.

Web-based indexes have been created over the last two decades for both websites and web-mounted documents ([Browne and Jermey, 2004](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#core-R4)). The success of the indexes depends on the commitment of the organisation/content owner, and the availability and commitment of the indexer(s). The index to the American Society for Indexing website is an example of a useful website index.<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#fn17" role="doc-noteref" id="body-ref-fn17">17</a></sup> It has been maintained for over two decades. It uses HTML Indexer software to embed the index terms within the website. Embedding has advantages for updating as the whole index does not have to be re-created each time the content changes.

The indexes to the periodicals _Native Plants for NSW_<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#fn18" role="doc-noteref" id="body-ref-fn18">18</a></sup> and _Garden Design Study Group Newsletter_,<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#fn19" role="doc-noteref" id="body-ref-fn19">19</a></sup> on the other hand, use a dedicated indexing software package to create the index, which is then output as an HTML version for the Web. As _Native Plants for NSW_ is no longer published, its index can remain static. The index to the _Garden Design Study Group Newsletter_, on the other hand, has to be output, manipulated and reloaded each year. This process has been refined over the years so it is not a great burden. As the MacQueen Scrapbook is complete, it will not have to be updated, unless, perhaps, further information comes to light on some of the incomplete names or missing links identified to external sources. Updating such would be straightforward.

Putting information on the Web is one step, but without quality navigation the content is likely to be missed or at least underused. The MacQueen Scrapbook navigation structure/index adds value to the content because it helps users to navigate through the material, and to find information on topics of interest, such as all mentions of a person. As the content is in image rather than text form, this access is even more crucial.

The index is logically constructed, with thought given to the nature of the content, and the needs of potential users, who can use, search or browse through the content, either by name or by category. Searching provides a list of possible results, refining the results list as more characters are added to the search. This means that users can find content without knowing the exact spelling of a name, for example.

The tools chosen (TiddlyWiki and Filemaker Pro database) provide technical support to the intellectual process of selecting terms of interest and creating the index, thus making it easier to create and keep consistent.

The use of external authorities for names (both spelling variations and earlier/later names) saves work and keeps the wiki index consistent with other resources. The only problem with this is that the names are retrieved without commas and look as if they could be in direct order (i.e. given name first). For example, it is not immediately clear in the tag ‘Abraham Trevor ?-?’ whether ‘Abraham’ is a first or last name. There is often a price to pay for maintaining consistency.<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#fn20" role="doc-noteref" id="body-ref-fn20">20</a></sup>

One challenge in indexing is dealing with the metatopic (the main topic of the work). Here there is no entry for Mary MacQueen. As she is mentioned on every page, it would be meaningless to add references for each occurrence. Instead, the home page provides brief information about her and her work and linkages to appropriate external sources for more detailed information.

The wiki is easy to use, and the site provides both brief and detailed hints to help users. One initial frustration is that the browser back arrow takes one out of the wiki, rather than to the last screen seen. This is an attribute of the TiddlyWiki software because its design is hinged on a single HTML page implementation for the whole wiki content, so previous searches are retained on the page (and can be found by scrolling up/down) rather than on a separate page. This requires some familiarisation on the part of the user.<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#fn21" role="doc-noteref" id="body-ref-fn21">21</a></sup>

## Conclusion

This wiki-based ‘index’ started with a need, and a practical approach was developed to provide appropriate access in the most efficient way possible. [Dettori and Gianetti (2004)](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.38#core-R7) report that

> The literature reports evidence that developing problem solving abilities strongly depends on developing problem representation abilities. This, in turn, appears to be connected with students’ ability to understand not only the problem’s explicit information, but also the implicit one, and to connect both to their previous knowledge. Different roles in problem solving appear to be played by representations which are given with the text of problems and representations which the solvers build by themselves to support their activity during problem solution. Representations play a crucial role in problem solving in particular when abstract concepts are handled …

The wiki, as discussed above, supports appropriate access via multiple strategies to support problem solving. The aim of this wiki was to provide access to the various clippings in a variety of ways. So finding the correct clipping is one of the major reasons for using it. Other reasons coexist, many in the mind of the user, but their resolutions are supported by the index(es).

Indexes, mind maps and topic maps are essentially different perspectives on the same elements, facilitating solution(s) to different problems. Like our minds, the wiki can and does accommodate all three. The topic map as implemented is very basic, essentially only a two-level map with, as discussed above, no explicit labelling of relationships. The obvious enhancement is to label those relationships as appropriate; however, it must be recognised that two elements may be related through multiple, differing relationships, as well as through intermediate elements. This complexity makes any such enhancement not a trivial exercise, and difficult, if not impossible, to automate. Also, it is not clear that such effort would be beneficial.

## Acknowledgements

The authors acknowledge the MacQueen family, especially her son, Duncan MacQueen, and the estate of Mary MacQueen in approving and providing access to the clippings book and the conversation recorded with her family. We also acknowledge the assistance of Adele Boag, artist, curator and gallery director, who provided feedback on the use cases and quality of this wiki from an artist’s perspective, and Dr Richard Jones, adjunct professor, Research School of Computer Science, Australian National University, and consulting scientist, Encompass Corporation, for his review of the paper.

## Footnotes

4

Dr Bob Jansen, founding director and chief scientist of the Cultural Conversations project, was the designer and developer of the wiki and primary author of the technical sections, including the navigation structure discussion. Freelance indexer Glenda Browne provided advice and guidance in relation to the architecture and the linkage structure and was the primary author of the indexer feedback section. She also provided input into the use cases, along with Adele Boag, artist, curator and gallery director, who contributed from an artist’s perspective and reviewed the quality of the wiki. Both authored the conclusion, and the paper was reviewed and tightened up in entirety by both authors.

7

There are plugins that facilitate the saving of changes when running from a web server (not discussed any further here).

15

Bob Jansen was International Computers Limited’s STATUS specialist in Australia during the 1970s and 1980s.

16

‘A digraph is any pair of adjacent letters (a digram in Miriam Webster) … We used a three-level digraph index because the mean word length in English is 6 and the analysis showed that there was a reasonable balance of an English vocabulary across the letter pairs’. Dr Richard Jones, personal communication.

20

It should be noted, though, that the entry text for a person lays out their name in the correct format. So the tiddler for Thake Eric Prentice Anchor 1904–82, starts, ‘You can find more references to Eric Prentice Anchor Thake …’.

21

The wiki does provide a ‘Previous’ and ‘Next’ facility through two separate buttons on the top right-hand side of each Scrapbook Page tiddler. This allows for conventional ‘page turning’ through the scrapbook.

## References

Biezunski, M. (2018) ‘Topic maps and the essence of indexing’, _The Indexer_ 36(4), 157–61.

Coleman, C. F. (1976) _A word and digraph-frequence analysis of fine legal texts_. Harwell: Atomic Energy Research Establishment.

Manguel, A. (1996) _A history of reading_. London: HarperCollins.

Niblett, G. B. F. and Price, N. H. (1969) _The STATUS Project: searching atomic energy law by computer_ (research report). Harwell: Atomic Energy Research Establishment.

Provo, A. (2019) ‘From index to network: topic maps in the Enhanced Networked Monographs project’, _The Indexer_ 37(1), 13–35.

Winchester, S. (2021) _Land: how the hunger for ownership shaped the modern world_. New York: HarperCollins.
