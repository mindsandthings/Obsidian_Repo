---
created: 2022-11-14T09:13:58 (UTC -08:00)
tags: []
source: https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18
author: Walter Greulich
---

# Embedded indexing with Word. Part 5 – locators other than page numbers | Indexer (The)

> ## Excerpt
> The focus of the fourth part of this series was on the generation of annotations to page references and of functional indexes for ebooks. In the context of ebook indexes, it described how other fie...

---
Publication: The Indexer: The International Journal of Indexing

Volume 39, Number 2

## Abstract

The focus of the fourth part of this series was on the generation of annotations to page references and of functional indexes for ebooks. In the context of ebook indexes, it described how other fields besides the PAGE field can be incorporated into the XE field. This article follows on from that, showing how, by using the STYLEREF field, it is possible to bring other locators into an index as substitutes for page numbers. The decisive factor here is again the shifting method. Only with this method can the locators be integrated into an overall workflow from Word to ebook or from Word to Index-Manager and back. The first four articles in the series can be found in the June, September and December 2020 issues and in the March 2021 issue of _The Indexer_ (38(2), 38(3), 38(4), 39(1)).

## Why use locators other than page references?

In most publications that are to be indexed, page numbers serve as references to the places where the index terms are found. But there are also cases where other locators are useful, or even better, as references. For example, the contributions to a handbook on a technical, medical, or legal topic might be highly structured, possibly with subheadings up to five or six levels. The structure or outline property is usually conveyed with appropriate numbers. In such a case, heading numbers may be better locators than page numbers, because they possibly increase granularity and lead the reader more directly to the reference. Moreover, such heading numbers provide additional information about the environment in which the index term is found: one can see how it is embedded in a hierarchical system.

In some works, additional numbers are used to form a bracket around passages of text in which a particular aspect is discussed. That is, they indicate a self-contained block of information. This can be a single paragraph or a collection of several consecutive paragraphs. Probably the best-known example of this type of numbering is the _Chicago Manual of Style_ (University of Chicago Press, 2017). In this reference work, these numbers are in the margin. However, it is also conceivable to have information block numbers before paragraphs or as bolded headings at the beginning of paragraphs.

Whether page numbers or other locators are used in an index also depends on which indexing tools are used and how familiar the client, indexer and typesetter are with document templates and styles and other functions of the word-processing or layout program on which the document is based. After all, it is not only stand-alone indexing programs that are able to handle locators other than page numbers. With appropriate formatting and when using the shifting method (see [Greulich, 2020d](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#core-r5)), other types of locators can also be inserted into Word’s XE fields and then integrated into the overall workflow from Word document to layout program to PDF (and thus to print output) or ebook.

## Dealing with heading and information block numbers in Word: a brief overview

Heading and information block numbers differ from other numbers in that they are structured. There are four main ways to arrive at a consistent system of structured numbers (often called _outline numbers_):

Manual numbering is very time-consuming, especially if numbers are added or deleted in the middle of the document and all subsequent numbers have to be adjusted. Multilevel list styles offer a great and largely reliable help in creating outline numbers. Some multilevel list styles have been permanently integrated into Word by Microsoft. They work together with Word’s built-in heading styles _Heading 1_, _Heading 2_, and so on. However, multilevel list styles can also be defined by the user. We cannot go into the details of multilevel list styles here.

The third and fourth way of numbering, using SEQ and LISTNUM fields respectively, can only be mentioned here in principle, but not described in detail. More detailed information on the use of multilevel list styles, SEQ and LISTNUM fields can be found in good Word manuals (e.g. [Tyson 2010](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#core-r7)), on the Microsoft Most Valuable Professionals page (WordMVP site),<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#fn1" role="doc-noteref" id="body-ref-fn1">1</a></sup> in Greulich ([2017](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#core-r1)) and on one of the author’s websites.<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#fn2" role="doc-noteref" id="body-ref-fn2">2</a></sup>

## How do the outline numbers get into the index?

Since we are in Word, everything that should appear in the index is controlled by the XE fields. This means that we have to find a way to get the outline numbers into the XE fields. Fortunately Word provides a way to automatically read these numbers and insert them as locators in the XE fields. Only if they are in the XE field can they be processed further. To bring outline numbers into an XE field, special fields can be used: the STYLEREF field and the SEQ field. This article only discusses the STYLEREF field, because it is a little more comfortable as it ‘extracts’ or ‘pulls’ information of any kind (including numbers) based on formatting alone.

### Use of the STYLEREF field

The STYLEREF field is generally used to read and reproduce the contents of text passages that have been marked with a paragraph or character style. It is mainly used to create so-called running or ‘living’ headers in the header area: for example, to reproduce the contents of the chapter heading on all pages of a chapter. When a new chapter starts, the header is automatically filled with the content of the new chapter heading. So the running header changes automatically from chapter to chapter – it ‘lives’. In order for the STYLEREF field to do its job, the chapter headings must have been marked with a suitable style, such as _Heading 1_. The STYLEREF field then can refer to this style.

The syntax of the field is

{ STYLEREF "Name" \\switch }

The name of the style to be referenced must be entered for ‘Name’. If chapter headings are numbered, it is possible to read and reproduce this number only. To do this, the \\n switch in the STYLEREF field must be used. Let us look, for example, at a chapter heading in a physics handbook marked with the style _Heading 1_. It may read:

## 2 Mechanics

With the STYLEREF field

{ STYLEREF "Heading 1" \\n }

only the number would be pulled. That is, where the STYLEREF field is located in the text (for example, in the header), once the field view was turned off, the 2 would be displayed.

If a subchapter of the same handbook is marked with the style _Heading 2_, it could read, for example:

### 2.1 Motion in one dimension

The number of this heading could be pulled with the following STYLEREF field:

{ STYLEREF "Heading 2" \\n }

After turning off the field view, 2.1 would be displayed. When referring to headings of other levels, the corresponding numbers are displayed, such as 2.1.2 or 2.1.2.1, etc. Since these outline numbers are controlled, so to speak, by multilevel list styles in the background, they can be read out with the STYLEREF field using the \\n switch, always reflecting the entire outline number according to the heading level.

The principle of using the STYLEREF field should now have become clear. For indexing this means:

•

If the STYLEREF field is included in an XE field, the XE field will contain the outline number from the associated heading. Whether the number is single- or multi-part depends on which name of a heading style is referenced and which level the heading is.

•

The number of a heading that _precedes_ the XE field is always pulled.

•

There can be several headings of different levels preceding an XE field; only the number of the heading whose name is specified in the STYLEREF field is fetched.

### Insertion of the STYLEREF field

The first question that arises is: _when_ should the STYLEREF field be incorporated into the XE field?

Answer: preferably immediately after the XE field of an index term has been created.

The second question is: _where_ within the XE field should it be incorporated?

Answer: there are several reasonable placement locations. Since the page reference is to be replaced, it is obvious that the \\t switch should be used in the XE field, which is also used for cross-references. It causes the display of the page number to be suppressed. The STYLEREF field can then be inserted after this switch. This will automatically result in only the outline chapter and subchapter numbers being displayed. Here is an example for the reference to a second-level heading:

{ XE "mechanics" \\t "{ STYLEREF "Heading 2" \\n }" }

The complete STYLEREF field must be enclosed in quotes to allow the \\t switch to do its job.

Another possible placement location will be considered later.

The third question we have: _how_ is the STYLEREF field inserted?

You could insert it via

> Menu \[Insert - Building blocks - Field, then select the STYLEREF field in the field list - OK\]

Once that is done, the field can be copied and pasted from the clipboard into the next XE field. However, a slightly different way is recommended: once the field has been created, it is marked together with the \\t switch and the quotation marks, then

> Menu \[Insert - Building Blocks - Save Selection to Quick Parts Gallery\]

is selected. The dialog box for creating a new Bulding Block opens. Remember that Quick Parts are a subset of Building Blocks (as shown in [Figure 1](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#F1)).

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.18/asset/6b2e2fc4-b4e0-4ea5-83ea-6bc849cdf1d6/assets/graphic/indexer_2021_18_fig1.jpg)

Figure 1. Building Block window of Word. _Katalog_ and _Schnellbausteine_ mean ‘Gallery’ and ‘Quick Parts’

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#F1)

Here only the name needs to be assigned; everything else can remain as it is. The name should be as short a string as possible, for example _sr_. Finally click OK and the new Quick Part has been created. Quick Parts have taken over the role of Autotexts in older Word versions. They behave like a permanent accessible clipboard. In the next XE field, the cursor is placed directly behind the closing quotation mark of the index term, then _sr_ is typed in and the F3 key is pressed immediately afterwards. This inserts the content of the Quick Part, i.e. the STYLEREF field, at the desired position. This is the way to proceed, index term by index term, thus XE field by XE field. If necessary, the name of the style to which the field refers can be changed immediately after insertion (e.g. _Heading 2_ becomes _Heading 3_, etc). It would be even more practical if there were two or three different Quick Parts – _sr1_, _sr2_ and _sr3_ – which already contain the name of the correct reference style. Then _sr1_, _sr2_ or _sr3_ is typed in and the complete field is inserted by pressing F3.

If required, it is possible to look at the field result (i.e. the parsed number), at any time by pressing <Alt-F9>. Pressing <Alt-F9> again switches back to the field syntax view.

### Examples for the insertion of the STYLEREF field behind the \\t switch

For illustration, some examples are given here. Starting from the two headings already mentioned (‘Mechanics’ and ‘Motion in one dimension’), further headings could be added and included in an index (the page numbers are arbitrarily chosen for demonstration purposes), as shown in [Figure 2](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#F2). We usually proceed page by page to create index entries. For this reason, the XE fields in the table are ordered by page number.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.18/asset/9bfa84d9-931c-44a9-8b74-3b78463cbae9/assets/graphic/indexer_2021_18_fig2.jpg)

Figure 2. Inserting the STYLEREF behind the \\t switch

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#F2)

In the index, it would look like this:

> acceleration, 2.1.3
> 
> average velocity, 2.1.1
> 
> instantaneous velocity, 2.1.2
> 
> mechanics, 2
> 
> motion
> 
> in one dimension, 2.1
> 
> in two and three dimensions, 2.2
> 
> Newton’s axioms, 2.3
> 
> work, 2.4

The index should again be in a separate file so that its growth can be permanently monitored (cf [Greulich, 2020a](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#core-r2)). It is also important to keep the cross-references in a separate file (as explained in [Greulich, 2020a](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#core-r2)).

However, the procedure has a few catches. Two things can happen if a term has several references:

•

the order of the references may not be correct

•

Word lists the same reference as multiple occurences.

The order problem will not be considered here, but in principle, it is solved similarly to the _problem of multiple occurrences_, as described here. For example, the following entries could occur:

> acceleration, 2.1.3, 2.2, 2.3, 2.3
> 
> average velocity, 2.1.1, 2.2
> 
> instantaneous velocity, 2.1.2, 2.1.3
> 
> mechanics, 2
> 
> motion
> 
> in one dimension, 2.1
> 
> in two and three dimensions, 2.2
> 
> Newton’s axioms, 2.3, 2.4, 2.4
> 
> work, 2.3, 2.4

Here the numbers 2.3 at ‘acceleration’ and 2.4 at ‘Newton’s axioms’ appear twice.

The reason for multiple occurrences is that Word is programmed in such a way that references are always included in the index page by page. If the text belonging to a certain chapter or subchapter heading runs over several pages and there are XE fields with the same index term on several pages, their occurrences are listed individually. If page numbers were used as locators, we would get the usual picture of comma-separated page references, such as

> acceleration, 20, 25, 32, 35

Word also applies this standard behavior to the STYLEREF field locators: the page numbers running in the background determine the rate at which the STYLEREF field locators are listed:

> acceleration, 2.1.3, 2.2, 2.3, 2.3

With a small index (up to a thousand entries), it is not a great effort to manually clean up such duplicate or multiple occurrences of locators. Since the index is constantly monitored during the generation of XE fields, multiple occurrences of the same locations are noticed immediately. To clean up, the superfluous XE fields in the affected page area are deleted.

One could even wait until the end to clean up and reduce the multiple locators in the overall index to one each. As emphasized in the other articles in the series, the overall index must be converted to normal text before editing: click into it, then press <Ctrl-6> or <Ctrl-Shift-F9>. For example, the pattern for removing multiple-occurring third-order locators (such as 2.1.4) from the index might look like this:

<table><tbody><tr data-xml-align="left"><td><b>search for (pattern search)</b></td><td><b>replace with</b></td></tr><tr data-xml-align="left"><td>(&lt;[0-9]{1;2}.[0-9]{1;2}.[0-9]{1;2}.&gt;), \1</td><td>\1</td></tr></tbody></table>

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#tabular-1)

Here it is assumed that each part of the structured total number can consist of up to two digits. This should cover the numbering of most projects that exist in practice.

The total number forms a ‘word’, which is expressed by the angle brackets. Also, this word is declared to be a group by putting within round brackets. It is the only group that occurs, so it has the group number 1 within the program. Two consecutive locators are separated by a comma, and the search is only for cases where the first total number (group 1) is repeated after the comma, which is expressed by \\1. Double occurrences of a locator are found by this procedure. The double locator is replaced by the single locator: i.e. by \\1. In the case that some locators in the index occur not only twice, but several times, the search/replace procedure would have to be repeated correspondingly often, but this can be done quickly. Second-order (like 2.3) or first-order (like 2) locators that occur more than once are cleaned up analogously.

### Examples for the insertion of the STYLEREF field in the lowest entry level: application of the shifting method

Instead of inserting the STYLEREF field behind the \\t switch, it can be inserted in the lowest level of the XE field. That is, the shifting method (see [Greulich, 2020d](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#core-r5)) is applied. Here are the main arguments for using the shifting method:

•

While writing an index, it is beneficial to always see the page numbers in the index to be able to quickly go to a found location. This is done by using the go-to function (see [Greulich, 2020a](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#core-r2)). This is less cumbersome than using the search function.

•

Also when using locators from heading or information block numbers, it may be necessary to make range specifications: for example 1.2.3–1.2 4. The shifting method is very helpful for range specifications as described by Greulich ([2020d](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#core-r5)).

•

The further processing of the index with a layout program or for an ebook should be possible without problems. Only if the locator is in the lowest level can an automatic linking be achieved via InDesign or Jutoh (see [Greulich, 2021](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#core-r6)).

•

_Index-Manager_ should be able to take over the data and process it correctly.

[Figure 3](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#F3) shows the application of the shifting method to the XE fields of the entries shown in the last index example. The colons in the XE field open the next sub-level of an entry.

In the overall index, it then looks like this:

> acceleration
> 
> **2.1.3** 20
> 
> **2.2** 25
> 
> **2.3** 32, 36
> 
> average velocity
> 
> **2.1.1** 14
> 
> **2.2** 24

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.18/asset/a9588755-e7c1-474f-9760-90813c9d4da7/assets/graphic/indexer_2021_18_fig3.jpg)

Figure 3. Applying the shifting method to the XE entries from [Figure 2](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#F2)

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#F3)

> instantaneous velocity
> 
> **2.1.2** 17
> 
> **2.1.3** 21
> 
> mechanics
> 
> **2** 12
> 
> motion
> 
> in one dimension
> 
> **2.1** 13
> 
> in two and three dimensions
> 
> **2.2** 24
> 
> Newton’s axioms
> 
> **2.3** 30
> 
> **2.4** 42, 45
> 
> work
> 
> **2.3** 36
> 
> **2.4** 40

The new locators are listed alphabetically as subentries or sub-subentries. They do not behave like numbers, but like usual entry text (because they are alphanumerical strings). They are written here in bold so that they stand out from the page numbers. Also, a double space has been used as a separator between entry text (i.e. outline number) and page reference. As is appropriate for subentries and sub-subentries, Word lists all references (in the form of the page numbers) one after the other: the new locators 2.3 at ‘Acceleration’ and 2.4 at ‘Newton’s Axioms’ have two occurrences each, on pages 32, 36 and 42, 45 respectively. The two locators 2.3 and 2.4 themselves occur only once. This means that the problem of multiple occurrences has solved itself.

If the document, and thus the index, is to be published directly from Word, the page number references must be removed, and the new locators must no longer be presented as subentries or sub-subentries, but must be placed directly after the respective index term.

The goal is the following presentation:

> acceleration, 2.1.3, 2.2, 2.3
> 
> average velocity, 2.1.1, 2.2
> 
> instantaneous velocity, 2.1.2, 2.1.3
> 
> motion
> 
> in one dimension, 2.1
> 
> in two and three dimensions, 2.2
> 
> mechanics, 2
> 
> Newton’s axioms, 2.3, 2.4
> 
> work, 2.3, 2.4

To achieve this goal, the index field must first be converted to normal text after all other editing has been completed. The easiest way to do this is to click into the index and execute the key combination <Ctrl-6>. Now the page numbers can be removed. The pattern search is used again for this:

<table><tbody><tr data-xml-align="left"><td><b>search for (pattern search)</b></td><td><b>replace with</b></td></tr><tr data-xml-align="left"><td>((double space))&lt;[0-9]{1;3}&gt;*^013</td><td>^p</td></tr></tbody></table>

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#tabular-2)

There is a double space before the page number references. The page number itself can consist of one to three digits (this should apply to most projects). The asterisk means that any letters, numbers or special characters will be found, up to the end of the line, marked with ^013. This means that the complete character string from the first page number to the end of the line will be marked during the search and replaced by the paragraph marker. When replacing, the code for the paragraph marker is ^p.

After this search/replace run, we have the following situation:

> acceleration
> 
> 2.1.3
> 
> 2.2
> 
> 2.3
> 
> average velocity
> 
> 2.1.1
> 
> 2.2
> 
> instantaneous velocity
> 
> 2.1.2
> 
> 2.1.3
> 
> mechanics
> 
> 2
> 
> motion
> 
> in one dimension
> 
> 2.1
> 
> in two and three dimensions
> 
> 2.2
> 
> Newton’s axioms
> 
> 2.3
> 
> 2.4
> 
> work
> 
> 2.3
> 
> 2.4

Now the locators must be dragged upwards to the associated term. To do this, the same methods as described for page range specifications (in [Greulich, 2020d](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#core-r5)) have to be applied. After that, the index has reached its final form.

## Further processing of a Word document with InDesign and Jutoh

What happens when a document containing XE fields with outline numbers is transferred to InDesign or Jutoh? Before the transfer, all STYLEREF fields that are in the XE fields must first be fixed. That is, the STYLEREF fields lose their field property, and in their place are now the outline numbers, which consist of common characters, namely digits and dots. For fixing, the whole document is marked by <Ctrl-a> and then <Ctrl-6> or <Ctrl-Shift-F9> is pressed.

### InDesign

In the case of using the \\t switch, the outline numbers end up in the cross-reference field of the index entry window, as shown in [Figure 4](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#F4). (The examples here are drawn from a German handbook of ‘Toxikologie’.)

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.18/asset/a1951bdd-d0f3-49b9-a137-70660106966f/assets/graphic/indexer_2021_18_fig4.jpg)

Figure 4. InDesign index entry window Note: when a cross-reference is handled, the index entry window automatically turns into the cross-reference mode (_Themenstufen_ means ‘Topic levels’).

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#F4)

If the index is generated, only the outline numbers are visible, but no page numbers. This is exactly what was desired ([Figure 5](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#F5)).

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.18/asset/51fa725d-69bf-4b52-934c-30b0f18f2d74/assets/graphic/indexer_2021_18_fig5.jpg)

Figure 5 InDesign index with special locators

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#F5)

The index looks good in principle (although the orphaned subentries would still have to be pulled up to the main entries) and it could be printed. However, if an EPUB file is to be exported from InDesign, an error message comes up saying that InDesign is not able to make links. The index to be found in the ebook looks like the printed one: as locators, the outline numbers are presented, but they lack function. That is, this index is basically useless.

When the shifting method is used, the outline number is kept as an ordinary subentry or sub-subentry (in the present example as a sub-subentry) ([Figure 6](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#F6)).

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.18/asset/7f82e4ab-d8bf-4eff-97e7-5420d8855b67/assets/graphic/indexer_2021_18_fig6.jpg)

Figure 6. InDesign index entry window, now in page-reference mode

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#F6)

In the index, the page numbers are displayed in addition to the outline numbers ([Figure 7](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#F7)).

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.18/asset/f2030b91-edc1-4406-9314-c687b6695e11/assets/graphic/indexer_2021_18_fig7.jpg)

Figure 7. InDesign index with special locators and page references

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#F7)

For print publication, the page numbers would have to be removed, but this is done in a few minutes with regular expressions (GREP).

If an export as EPUB is made from InDesign, the page numbers appear again, in addition to the outline numbers in the ebook index, but now they are linked. With the help of the ebook program Sigil, the page numbers can be removed and the linking moved to the outline numbers. For this purpose, Sigil uses regular expressions in the HTML source code.

### Jutoh

As shown in Greulich ([2021](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#core-r6)), the ebook program Jutoh takes the XE fields from Word, converts them, and uses them to create its own index. In the Jutoh index, the lowest levels of the entries are always linked automatically. In the case of using the \\t switch, not the outline number, but the entry text is on the lowest level in each case. This causes Jutoh to link the text itself. The outline number will be discarded (as in [Figure 8](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#F8)). With the shifting method, the outline numbers are linked – as they should be (as in [Figure 9](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#F9)).

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.18/asset/e9693b94-929f-42c9-9e2f-6da20ed9ff25/assets/graphic/indexer_2021_18_fig8.jpg)

Figure 8. Jutoh index with term links

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#F8)

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.18/asset/679af64d-859d-4e95-a9e5-5ef6db17a6df/assets/graphic/indexer_2021_18_fig9.jpg)

Figure 9. Jutoh index with linked locators

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#F9)

In this form the index is almost ready. The numbers only have to be pulled up to the entry texts. But this is done quickly with Sigil via regular expressions.

## Use of Index-Manager

Another interesting question is whether the Index-Manager program can also be used for outline numbers. The answer is yes, but only if the shifting method is used. Index-Manager interprets content after the switch \\t as cross-references. That means that, using the switch \\t, all entries are treated as cross-references. Meaningful editing is therefore not possible.

The situation is different with the shifting method. Here all outline numbers stand as ‘usual’ entry text on the respective lowest level of an XE field. If the Word file is loaded into Index-Manager, the numbers are to be seen in the index window, as in [Figure 10](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#F10).

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.18/asset/c540c692-501d-45ec-9b20-a4ba90d4b1d7/assets/graphic/indexer_2021_18_fig10.jpg)

Figure 10. Index-Manager with index window (left) and text window (right)

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#F10)

But how, for example, does the creation of a new entry happen? Index-Manager is not able to create the STYLEREF field, but can work with placeholders. This means that when a new entry is created, a code is entered at the lowest level. The code should be so unique that Word can ‘make’ the appropriate STYLEREF field from it by search/replace. The best codes are those that stand for the name of the style to which the future STYLEREF field should refer: for example, _h1_ for the style _Heading 1_, _h2_ for the style _Heading 2_, and so on. In Index-Manager, the indexer sees which heading or information block a new entry belongs to. The information for the applicable code is therefore available and only needs to be entered.

After the data has been transferred from Index-Manager to Word (using the Export function), only two or three search/replace operations need to be performed in Word to incorporate the STYLEREF fields. Temporarily, three STYLEREF fields are first created somewhere in the document:

{ STYLEREF "Heading 1" \\n }

{ STYLEREF "Heading 2" \\n }

{ STYLEREF "Heading 3" \\n }

Now the first field is marked and copied. This puts it on the clipboard. With this, the first search/replace run can be executed. The same is done with the other two fields. The three find/replace runs look like this (where ^c stands for the contents of the clipboard):

<table><tbody><tr data-xml-align="left"><td><b>search for</b></td><td><b>replace by</b></td></tr><tr data-xml-align="left"><td>:h1"</td><td>:^c"</td></tr><tr data-xml-align="left"><td>:h2"</td><td>:^c"</td></tr><tr data-xml-align="left"><td>:h2"</td><td>:^c"</td></tr></tbody></table>

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#tabular-3)

In all three cases, _Replace All_ can be chosen. This means that the conversion to STYLEREF fields is done in a few minutes. It is important not to forget that before reloading into Index-Manager, all STYLEREF fields must be fixed again.

With this procedure it is also possible to create the complete index from scratch with Index-Manager. After exporting the index and updating the Word file (or even several Word files), only the search/replace runs mentioned above need to be executed and an index with outline numbers as locators is obtained.

## Conclusion and outlook

We have now seen how, in a Word index, the page numbers can be replaced with other locators. In the case of structured headings or information block numbers as locators, the STYLEREF field is used, which is inserted into the XE field. As was shown in Greulich ([2020d](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.18#core-r5)), the shifting method again offers many advantages. If the goal is the output of a print index, the switch \\t method can also be used. If the output is intended to be a functional ebook index, there is no alternative to using the shifting method. It is also the necessary prerequisite for Index-Manager to be able to process outline numbers and pass them back to Word. The next and final article in this series will focus on two closely related topics: sorting and exporting index entries. Among other things, we will examine whether and how it is possible to output an index in such a way that the entries are arranged in the order of the pages or other locators. If this is successful, the entries can be exported in a simple way and then further processed, in a stand-alone indexing program, for example. Another interesting point is the switching from word-by-word to letter-by-letter sorting. It will be seen that even this is possible in Word.

## Footnotes

## References

Greulich, W. (2017) Dokument- und Formatvorlagen für Word 2016, 2013 und 2010. Hamburg: Tredition.

Greulich, W. (2020a) ‘Embedded indexing with Word: new light on an old topic. Part 1: how to monitor creation of an index’, _The Indexer_ 38(2), 207–18.

Greulich, W. (2020b) ‘Embedded indexing with Word. Part 2: editing entries and making work easier by using macros’, _The Indexer_ 38(3), 291–306.

Greulich, W. (2020c) Indexing mit Word. Hamburg: tredition.

Greulich, W. (2020d) ‘Embedded indexing with Word. Part 3: shifting method and field codes for cross-references and page ranges’, _The Indexer_ 38(4), 381–98.

Greulich, W. (2021) ‘Embedded indexing with Word. Part 4: page reference annotations and functional ebook indexes’, _The Indexer_ 39(1), 85–100.

Tyson, H. (2010) Microsoft Word 2010 Bible. Chichester: Wiley.

The University of Chicago Press (2017) Chicago Manual of Style, 17th edn. Chicago: The University of Chicago Press.
