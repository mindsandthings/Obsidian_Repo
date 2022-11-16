---
created: 2022-11-14T09:17:39 (UTC -08:00)
tags: []
source: https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8
author: Walter Greulich
---

# Embedded indexing with Word. Part 4 – page reference annotations and functional ebook indexes | Indexer (The)

> ## Excerpt
> In this fourth article in a series on the under-exploited potential for using Microsoft Word as a tool for embedded indexing, the focus is on creating page-reference annotations and the automatic l...

---
Publication: The Indexer: The International Journal of Indexing

Volume 39, Number 1

## Abstract

In this fourth article in a series on the under-exploited potential for using Microsoft Word as a tool for embedded indexing, the focus is on creating page-reference annotations and the automatic linking of index entries when producing an ebook from the Word document. Also described is the transfer from Word to ebook by using the ebook programs Jutoh and Sigil. The first three articles in the series can be found in the June, September and December 2020 issues of _The Indexer_ (38(2), 38(3) and 38(4)).

The third part of this series of articles focused on the creation of page-range specifications using the shifting method and the PAGE field. The arrangement of _see also_ cross-references can also be controlled with this. However, as previously mentioned (see [Greulich, 2020c](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#core-R5)), the shifting method and the inclusion of the PAGE field can even be used to create page-number annotations and functional ebook indexes. This is described here.

## Page numbers with annotations (labels, decorations)

Sometimes, when referring to a page, one would like to point out that the reference is taken from a footnote, a figure, a caption, or a table, by adding appropriate identifiers – one can also speak of these as annotations, labels or decorations.

The goal is, for example, to have the following display appear in the index:

> InDesign 61–65
> 
> Fenster für Spezialsortierung 64b
> 
> Indexeintragsfenster 63b
> 
> RTF 62t
> 
> Zwischenablage 65t

The letters b and t stand for _Bild_ and _Tabelle_ respectively (in English indexes corresponding to f for ‘figure’ and t for ‘table’). This means that the references for ‘Fenster für Spezialsortierung’ and ‘Indexeintragsfenster’ belong to locations in an image (or in a caption) and the references ‘RTF’ on page 62 and ‘Zwischenablage’ on page 65 are located in a table (or table heading). Of course, it would help if the page numbers concerned were written in italics; this would make them stand out from the usual page references in normal font. A short explanatory text at the beginning of the index could explain to the readers the meaning of italics and italics could be easily activated with the switch \\i in the XE field (see e.g. [Greulich 2020b](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#core-R4)). But the annotations b and t allow a finer distinction than italics. In general, annotations, including others in addition to b and t, would be helpful in any case. In principle, text strings consisting of several letters (such as ‘figure’ or ‘table’) can also be used as annotations.

Using the index features integrated within Word, such annotations cannot be brought into an index, at least not without causing sorting problems. You can, e.g., use the PAGE field behind the \\t switch, but such an entry would not be sorted correctly.

However, there is a simple way to solve this task.

The previous article in this series ([Greulich, 2020c](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#core-R5)) explained that even the codes ‘<’ and ‘>’ for the start and end of a page range are basically nothing more than annotations. Therefore all statements made there can be transferred to other annotations. This present article, which is on annotations in general, gives an overview only, but no technical details. Again, it is important to work in two stages: the writing stage and the technical stage.

In stage 1 (writing stage) the entries are created and edited. To decorate an entry, the label (e.g. b or t) is entered in the XE field in a new level (i.e. after a colon), as shown in [Figure 1](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#F1).

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.8/asset/b7f37f50-c3ae-4670-8ba4-99cd16133264/assets/graphic/indexer_2021_8_fig1.jpg)

Figure 1. Stage 1: the writing stage – adding the labels

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#F1)

In this way, all entries with annotations are created. Once the document has been equipped with all XE fields and the content has been finished, the work steps of stage 2 can be carried out – either by the indexer or by another person who may be more familiar with the technical aspects of Word. The goal of stage 2 is to output the fully formatted index.

The first step in stage 2 is to create a PAGE field ([Figure 2](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#F2)a) in a new index level at the end of each XE field using search/replace (see Greulich 2020c). Then the PAGE field is moved in front of the annotation (again via search/replace) and the second colon is deleted ([Figure 2](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#F2)b). All PAGE fields should then be updated (<Ctrl-A>, then <F9>) in order to show the correct page numbers. After that the page numbers are fixed (the easiest way is to use <Ctrl-6>). In a further step, leading zeros are inserted (e.g. 61→ 061, [Figure 2](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#F2)c); these are important for correct sorting.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.8/asset/b7c6d7d4-0f92-4e27-a312-ab262ecfb364/assets/graphic/indexer_2021_8_fig2.jpg)

Figure 2. The three work steps of stage 2 for creating the fully formatted index

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#F2)

In this way everything is prepared to convert the index into its final form. The index section for the above example currently looks like this:

> InDesign
> 
> 061< 61
> 
> 065> 65
> 
> Fenster für Spezialsortierung
> 
> 064b 64
> 
> Indexeintragsfenster
> 
> 063b 63
> 
> RTF
> 
> 062t 62
> 
> Zwischenablage
> 
> 065t 65

At this stage the page numbers occur twice, which is the ‘natural’ result of this process, as described in part 3 of this series (Greulich, 2020c). Now only the search/replace runs described in that article have to be performed to remove the repeated page numbers and correctly display page ranges and annotations (as shown in the first index example on page 86).

## Ebook indexes with active page references

It is permissible to ask, why do we need page numbers in an ebook index? This is not the place to begin a discussion about this. We, as professional indexers, know the answer. In an article by [Cary Wenzel (2008)](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#core-R9) on a keynote address given by Jeff Duntemann on the ‘changing of books’, there are some remarkable statements relevant to the subject discussed here: ‘At least for the foreseeable future, book pages are here to stay. They are fundamental. They are understandable. As Jeff said at the end of his presentation, “Don’t give them up without a fight!”’

If we want to keep page numbers, we must seek and hopefully find ways to pass them from indexes designed for print books to those for ebooks. Looking at Word, one way (not the only one, but a good one) is to use the combination of the PAGE field and the shifting method (see Greulich, 2020c) in order to prepare the transfer. Here I describe a transfer method on the basis of the Jutoh program.<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#fn1" role="doc-noteref" id="body-ref-fn1">1</a></sup> Jutoh is an ebook layout program which, as the developers say, allows ‘digital publishing for everyone’. With Jutoh, an active ebook index can be created in which the index terms themselves are linked. By default, these links start from the lowest existing index level (see Appendix for a detailed description). This knowledge can be used to bring the page number information already in Word to the lowest existing index level by appropriate preparation. It would then be passed via Jutoh on to the ebook index.

All content-related work on the XE fields in Word should be completed first. Preparations for the transfer of the Word data to Jutoh will begin with stage 2a (see Greulich, 2020c). As described in the above section on page number annotations, in Word the PAGE field can be inserted into the lowest index level within all XE fields. Only a rather simple find/replace run (with REPLACE ALL) is needed for this action. We will first consider here the simple case of not using any annotation in addition to the PAGE field, for example:

> Seite 64: { XE "InDesign:RTF:{ PAGE }" }
> 
> Seite 78: { XE "InDesign:Zwischenablage:{ PAGE }" }

The two most important further preparation steps are fixing the PAGE fields and inserting leading zeros in the page numbers (for correct sorting). The two sample XE fields then look like this:

> Seite 64: { XE "InDesign:RTF:064" }
> 
> Seite 78: { XE "InDesign:Zwischenablage:078" }

This completes stage 2a; all page information is in the lowest level of the XE fields. Now the data can be transferred to Jutoh.

### _Transfer of data to Jutoh and creation of the ebook index_

Since Jutoh ‘understands’ the information contained in the XE fields, its own index function can be used to create the index at the touch of a button. This index can be viewed immediately in Jutoh. Or the ebook can be exported and the result can be viewed with an EPUB or MOBI viewing program or immediately on an ebook reader. In all cases the resulting index looks like this (where the underlining marks the linking):<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#fn2" role="doc-noteref" id="body-ref-fn2">2</a></sup>

> InDesign
> 
> RTF
> 
> 064
> 
> Zwischenablage
> 
> 078

If there are several locations where a term is found, and possibly also page ranges or locations with annotations, the corresponding page numbers are sorted like other sub-entries. It is worth remembering what was explained in the third part of this series (Greulich, 2020c): the page-number information generated with the PAGE field is not in a number format, but is an alphanumeric string. These page references are therefore sorted like characters (i.e. alphabetically). And that is the reason why leading zeros are needed. Finally, the index looks like this:

> InDesign
> 
> RTF
> 
> 023–024
> 
> 064
> 
> Zwischenablage
> 
> 078
> 
> 105b

This could be left as it is, since on an ebook reader the space requirement of an index is not critical. In fact, this arrangement of page references gives a better overview than separating page numbers with commas, as is usual with indexes for printed works. But if the task is to make the appearance of the ebook index as close as possible to that of the printed version, a quick solution can be found by search/replace. However, this is not possible in Jutoh directly, because these changes have to be made in the HTML source code, which Jutoh does not allow. Ideal for this is the EPUB editing program Sigil (see Heiland, 2019),<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#fn3" role="doc-noteref" id="body-ref-fn3">3</a></sup> which is relatively easy to use (see Appendix for details). Sigil offers powerful search/replace options based on regular expressions (pattern searches). The result of Sigil processing will look like this:

> InDesign
> 
> RTF 023–024, 064
> 
> Zwischenablage 078, 105b
> 
> If the leading zeros are annoying, they can be deleted with another simple search/replace run.

### _Percentage specifications_

Since no fixed pages are displayed on an ereader (we will not consider the case of fixed-layout ebooks here), one idea would be not to present the page numbers of the print version in the index, but to give percentage specifications. For example, if a work has 180 pages in the print version and the location of an entry is on page 70 of the print version, the percentage would be: 38.89 per cent (since 70/180 = 0.38888). Even such an indication would give the readers an impression of where the entry is located within the book – at the beginning, in the middle or at the end. This is consistent with the fact that most ereaders display the ‘reading progress’ as a percentage below each screen page. With the field-in-field method described in Greulich (2020c), percentage specifications can be achieved in Word indexes and passed on to the ebook using the method decribed here.

Instead of simply inserting the PAGE field into the XE field, a formula is inserted in which the quotient of the current page number and the total page number is calculated. The result is multiplied by 100. Such an XE field would look like this:

> { XE "index term:{ = { PAGE }/{ NUMPAGES }\*100}" }

This formula can also be brought into all XE fields by regular expressions in a single search/replace run. The formula should first be created and copied somewhere in the normal text or a new empty Word file so that it is in the clipboard. When replacing, \\1:^c” can be used, where ^c stands for the content of the clipboard (see Greulich, 2020c).

The formula field has the general syntax { = formula }. The best way to create it is as follows. First, an empty field is created and then its contents are entered. It is important that this is done _outside_ any XE field and the format must be normal text (not hidden text). The command for an empty field is <Ctrl-F9>, which gives { }. Now the equals sign is entered between the curly field brackets and the actual formula is built behind it. First comes the PAGE field, which is obtained most easily by pressing <Ctrl-F9> again. Again, this produces an empty field, in which the word PAGE is entered. The intermediate result looks like this: { = { PAGE } } (please note that all brackets are field brackets). The slash is typed after the PAGE field and after that again the key combination <Ctrl-F9>. In the new empty field NUMPAGES is entered and then \* 100 is typed (\* 100 means: times 100). This produces the desired formula:

> { = { PAGE }/{ NUMPAGES }\*100}

The result of the calculation is by default a decimal number with two decimal digits. The formula can now be inserted into the XE fields.

This is a nice example of what field-in-field means. Here we have a double nesting: the PAGE and NUMPAGES fields are inside the calculation field and the calculation field is inside the XE field. In principle, further nesting is possible. For example, one could continue to work with the ROUND function, which allows the number of decimal digits to be controlled. The formula for rounding to one decimal digit would be:

> { = Round { { PAGE }/{ NUMPAGES }\*100};1 }

Like the PAGE field alone, the result of this calculation can be fixed. It can then be transferred to the ebook program in the same way as a page reference. If the above index section belongs to a book of 180 printed pages, it would look like this in the ebook:

> InDesign
> 
> RTF 12.78–13.33, 35.56
> 
> Zwischenablage 43.33, 56.67b

These percentages with two decimal digits are harder to read than pure page numbers, but the number of decimal digits could be reduced to 1 or even 0. This would improve readability, but at the same time reduce accuracy. The larger the book, the more important it would be to work with two decimal digits for accuracy reasons (with the ROUND function one could even create three or more decimal digits). Percentage specifications are relative values, and this is something that fits much better to a reflowable text (see Appendix) than the absolute page numbers we know from print. Since such relative references are not yet standard in indexes, an introductory note preceding the index could perhaps help readers to understand these references. However, something else is more important than such an introductory text: the reader must end up exactly at the place in the text that the reference promises (see [Coe and Wright, 2019](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#core-R1); [2020](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#core-R2)).

It is worth pointing out that with the normal indexing function in Word, or with the indexing functions in other word processing programs (like LibreOffice) or layout programs (like InDesign), it is not possible to create relative values instead of absolute page references. Even stand-alone indexing programs are not capable of this (except by manual input). This only works if calculations can be performed within the respective program. And Word has exactly this ability because it works with fields and these can be nested in one another. This makes Word stand out from all these programs in a positive respect.

## Conclusion and outlook

We have seen how page references can be ‘decorated’ in an embedded Word index, how an ebook can be created from Word and how to link the page references automatically during conversion with the Jutoh program. There are many more surprising aspects of embedded indexing with Word. Not all of them can be described in this series of articles. More detailed information can be found in Greulich ([2020d](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#core-R6)), an English-language edition of which will be published in the near future. In the meantime, there are plans to conclude this series with two further short articles. These will cover a deeper insight into the field-in-field technique (where fields other than the PAGE field come into play), sorting the index by page numbers and exporting the index data, and what the shifting method means for InDesign and how it is applied there.

## Footnotes

2

The settings in Jutoh for the generation of hyperlinks are described in the Appendix.

## Appendix: functional ebook indexes from Word files – a detailed description

Here I provide the background information on how page references can be passed from Word to an ebook, beginning with how an ebook can be created on the basis of Word data.

It is important to make it clear that PDF is a digital publication format, but not a real ebook format. The linking of index entries in PDFs is not dicussed here. An ebook is generally understood to be a document that is optimized for reading on an ereader. Typical ebook formats are EPUB and MOBI. They give digital books the property of being reflowable, i.e. they can be adapted to the size of the screen. EPUB is an open format developed by the International Digital Publishing Forum (IDPF, 2020);<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#fn4" role="doc-noteref" id="body-ref-fn4">4</a></sup> MOBI is Amazon’s own format, which allows digital books to be read on Amazon’s Kindle ereaders.

### _Creation of ebooks with Jutoh and Sigil_

There are several different ways to create an ebook from a Word document. The most popular and technically uncomplicated way is via InDesign: a Word document is loaded into InDesign, designed, and then exported as an ebook in EPUB format. However, as always, when something is simple, there are disadvantages. EPUBs from InDesign, for example, contain much unnecessary code, which makes it difficult to convert them to MOBI or to post-process them with an XML program. Ebooks that are generated with special ebook programs such as Jutoh and Sigil are significantly leaner and easier to process. The biggest advantages of this second route are good quality, flexibility, speed and, last but not least, low cost. Here I concentrate on the Jutoh–Sigil path.

On the way from Word document to ebook, Jutoh takes on the role of a moderator. It cushions the immense technical challenges. Without such a moderator, it would be necessary to work entirely in HTML or XML. This is reserved for technical professionals. The goal here is to show methods that can be followed by any indexer, editor or author and still lead to high-quality results.

Apart from technical aspects, there is an important content-related feature which makes the HTML/XML route less attractive: all index information contained in the Word document would be lost and could only be partially brought back into the ebook at great effort and expense. Jutoh, on the other hand, understands the XE fields from Word and processes them further.

Using the Jutoh–Sigil way the Word file can be imported directly (without the detour via HTML) into Jutoh. All formating of the document and also the contents of the XE fields are transferred to Jutoh. After importing, the content can be designed with the tools provided by Jutoh, and finally EPUB is output. An ebook created with Jutoh receives the final touches when it is loaded into the EPUB processing program Sigil and finished there; this is important if a functional index is embedded. Finally, a check program (included in Jutoh and Sigil) is used to check whether the data are technically correct. The process is shown in [Figures A1](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#AF1) to [A4](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#AF4).

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.8/asset/bbba203d-3008-46be-bc38-122f41803d37/assets/graphic/indexer_2021_8_afig1.jpg)

Figure A1. Jutoh user interface

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#AF1)

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.8/asset/4ade7e52-5522-4209-a926-0d707522c6b4/assets/graphic/indexer_2021_8_afig2.jpg)

Figure A2. Influencing CSS in Jutoh

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#AF2)

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.8/asset/74d98488-3842-4788-b808-527b32eb52bf/assets/graphic/indexer_2021_8_afig3.jpg)

Figure A3. Sigil user interface

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#AF3)

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.8/asset/66e7ce21-e0ad-4ca2-b39a-dbf27b2ff1a3/assets/graphic/indexer_2021_8_afig4.jpg)

Figure A4. Section of the content shown in [Figure A3](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#AF3), but now in HTML source code view

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#AF4)

[Figure A1](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#AF1) shows the Jutoh user interface. When a Word document is loaded, a new ‘project’ is created in Jutoh. On the left is the structure of the project, which is divided into several sections. In the middle, the text of a section is displayed, in rendered form. The floating ‘palette’ on the right gives access to various windows that can help with editing: tools, formats, etc.

[Figure A2](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#AF2) shows how the cascading style sheet (CSS) can be altered in Jutoh to influence the design of the ebook. This example shows how to change the settings of a paragraph style (named ‘Vfll\_fliess’) that came over from Word.

[Figure A3](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#AF3) shows the Sigil user interface. If an EPUB file from Jutoh is loaded into Sigil, it is managed here as a ‘book’. On the left is the structure of the book, which is divided into several sections. In the middle is the text of a section, in rendered form. On the right is the functional table of contents, which either was transferred from Jutoh to Sigil or can be generated in Sigil by pressing a button. Below the text window, the search/replace window is displayed, where complex searches based on regular expressions can be entered. At the very bottom, small custom ‘clips’ are listed, which combine several formatting commands and execute them by clicking on them.

[Figure A4](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#AF4) gives an insight into the HTML source code as it is presented in Sigil. Particularly noticeable are the so-called class attributes, which correspond to the format styles in Word. Find/Replace commands must be executed in this view. That this is only possible with regular expressions should be clear.

The best way to get a MOBI version is to convert the finished EPUB file with KindleGen (included in the so-called KindlePreviewer<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#fn5" role="doc-noteref" id="body-ref-fn5">5</a></sup>). So the complete path actually consists of Jutoh, Sigil and KindlePreviewer. [Figure A5](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#AF5) shows a section of the KindlePreviewer interface. The result should then be checked visually in an ebook viewing program (Apple iBooks, Adobe Digital Editions and Kindle Previewer) and on various ebook readers. If everything is in perfect order, the ebook can be published.

Here is an overview of the steps that lead from Word to ebook:

1

loading the Word file into Jutoh

3

outputting in EPUB format

4

possible post-processing with Sigil

5

technical verification and clean-up (in Jutoh and/or Sigil)

6

conversion with KindleGen to the MOBI format

7

control in EPUB or MOBI viewing programs and on ebook readers

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.8/asset/03b73a93-ac1b-4e96-9870-ee0ad962a2a8/assets/graphic/indexer_2021_8_afig5.jpg)

Figure A5. Detail of the KindlePreviewer interface

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#AF5)

The current (2020) purchase price of Jutoh is a relatively modest €30 (simple version) or €80 (professional edition). To learn how to use Jutoh, it is advisable to watch the introductory video on the Jutoh site, consult the user manual ([Smart, 2020](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#core-R8)) and gain experience through sample projects – in other words, Jutoh is self-teaching.

Sigil is a shareware program. It can also be learnt by reading the good manual ([Heiland, 2019](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#core-R7)). Although it is technically quite demanding, because one is dealing with HTML and CSS, there are numerous online aids, such as w3schools<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#fn6" role="doc-noteref" id="body-ref-fn6">6</a></sup> or the German-language site selfhtml.<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#fn7" role="doc-noteref" id="body-ref-fn7">7</a></sup>

KindlePreviewer can be downloaded for free and is intuitive to use. The conversion from EPUB to MOBI is fully automated. An export from KindlePreviewer delivers the publication-ready MOBI file, which can be uploaded to the platform of the distribution service provider (i.e. also directly to Amazon).

### Functional ebook indexes with Jutoh and Sigil

When Word data are transferred to Jutoh, the XE fields are converted into Jutoh’s own index elements; in addition, Jutoh automatically sets a target anchor for each index element. If an index is now created using Jutoh’s own index function, all references from the index are immediately linked to the target anchor. This is exactly the function that makes the heart of all indexers beat faster.

Of course, there are also limitations to the Jutoh method, which one must be aware of when following this path:

•

Jutoh allows only three index levels. With regard to the code-shifting procedure and the use of the PAGE field, this means that only two index levels are available in Word for content purposes, because the third level is needed for the code and the PAGE field. This is a disadvantage compared to the InDesign method, where in Word there are three content-related index levels and a fourth level can be used for code and PAGE field.

•

Formatting that has been done in the XE fields is lost, and it cannot be manually rebuilt in Jutoh; Sigil would have to be used for this.

•

In addition, Jutoh completely detaches itself from the page numbers generated by the Word indexing function. This means that indexers must also get rid of these page numbers and replace them with others. Fortunately, there is the PAGE field, with which we can get the problem under control.

What Jutoh _is_ able to do:

•

In the index, which is created with Jutoh’s own index function, either the terms themselves are linked to the found locations (this is the default setting; see [Figure A6](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#AF6)) or all found locations of an entry are numbered consecutively and the numbers carry the hyperlinks. It is important to note that it is always the lowest level containing information that is linked. It is not possible to specify ranges with Jutoh’s own tools, therefore it is important to prepare range specifications already in Word by using code shifting and the PAGE field (see above).

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.8/asset/1aeab701-a334-4db3-a59d-aa1604b1374e/assets/graphic/indexer_2021_8_afig6.jpg)

Figure A6. Settings options for an index generated by Jutoh

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#AF6)

•

Some formatting is done by Jutoh itself: the sub- and sub-sub-entries have indents against the next-higher level, and all levels also have a hanging indent, so that text that runs over more than one line is indented accordingly in the following lines. The program also automatically creates alphabet-area headings.

•

As with the Word–InDesign path, all cross-references are preserved and displayed correctly in the Jutoh index.

The index settings in Jutoh are shown in [Figure A6](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#AF6). By default, the check mark for ‘Only use linked numbers’ is _not_ set. This means that the terms themselves are linked.

An excerpt from a typical index generated in Jutoh is shown in [Figure A7](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#AF7). The direct linking of terms is on the left; if there are several references to a term, it is numbered. The right-hand side shows an example of when the program is set up (see [Figure A6](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#AF6)) to use only sequence numbers that carry the links. To link the PAGE field numbers of an index taken from Word, the direct linking of the terms must be set.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.8/asset/35545a8e-f9b5-4d11-b94f-111dcd875dc1/assets/graphic/indexer_2021_8_afig7.jpg)

Figure A7. Ebook index with automatically linked entries, as created with Jutoh

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.8#AF7)

It is worth emphasizing the fundamental importance of the fact that with Jutoh it is possible to use the work that has been put into an embedded index in Word for the ebook. Any ebook with a functional index can be created with a few commands in a short time (depending on the size and complexity of the content). I am not aware of any method that can compete with the Jutoh method in terms of quality and speed.

## References

Coe, M. and Wright, J. (2019) ‘Looking for needles in a haystack: how do ebook reader applications handle active indexes? Part 1 – ereader and Web browser software’, _The Indexer_ 37(2), 125–40.

Coe, M. and Wright, J. (2020): ‘Looking for needles in a haystack: how do ebook reader applications handle active indexes? Part 2 – dedicated ereader devices’, _The Indexer_ 38(1), 29–44.

Greulich, W. (2020a) ‘Embedded indexing with Word: new light on an old topic. Part 1: how to monitor creation of an index’, _The Indexer_ 38(2), 207–18.

Greulich, W. (2020b) ‘Embedded indexing with Word. Part 2: editing entries and making work easier by using macros’, _The Indexer_ 38(3), 291–306.

Greulich, W. (2020c) ‘Embedded indexing with Word. Part 3: shifting method and field codes for cross-references and page ranges’, _The Indexer_ 38(4), 381–98.

Greulich, W. (2020d) _Indexing mit Word_. Hamburg: tredition.

Wenzel, C. (2008) ‘Can the humble page survive the E-book?’, _Key Words_ 16(3), 93, 106.
