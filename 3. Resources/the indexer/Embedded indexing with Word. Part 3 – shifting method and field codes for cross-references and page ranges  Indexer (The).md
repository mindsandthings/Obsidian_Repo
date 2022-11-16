---
created: 2022-11-14T09:17:18 (UTC -08:00)
tags: []
source: https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36
author: Walter Greulich
---

# Embedded indexing with Word. Part 3 – shifting method and field codes for cross-references and page ranges | Indexer (The)

> ## Excerpt
> In this third article in a series on the underexploited potential for using Microsoft Word as a tool for embedded indexing, the focus is on what is called the ‘shifting method’ and the use of the P...

---
Publication: The Indexer: The International Journal of Indexing

Volume 38, Number 4

## Abstract

In this third article in a series on the underexploited potential for using Microsoft Word as a tool for embedded indexing, the focus is on what is called the ‘shifting method’ and the use of the PAGE field within the XE field. It covers the application of these methods to see also cross-references and page ranges. The important search/replace method in this context, the pattern search, is described in detail. The addition of decorations to page references and the automatic conversion of a Word index into an active ebook index are also considered. The first two articles in the series can be found in the June and September 2020 issues of _The Indexer_ (38(2) and 38(3)).

The first two parts of this series ([Greulich, 2020a](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#core-R1); [2020b](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#core-R2)) described the basics for effective indexing with Word. In practical work, however, indexers are often faced with challenges that are commonly believed to be impossible to overcome with Word:

•

Can _see also_ cross-references be arranged at the end of an array?

•

Is it possible to create page-range specifications in a simple way, without the cumbersome method of using bookmarks?

•

Can page numbers be decorated?

•

Is it possible to transfer the XE field contents to an ebook program in such a way that page numbers are linked automatically?

_Indexing mit Word_ ([Greulich, 2020c](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#core-R3)) answers these questions in the ‘Tips and tricks’ chapter, because that’s what it’s all about: technical tricks. Again, as stated in the first article of the series, if you choose the appropriate ones from the huge potential of technical possibilities offered by Word and implement them for indexing, indexing with Word is really fun, and will bring the success hoped for. In the course of my professional life as an editor and indexer, I have taken several attempts to apply insights I have gained, for example, in search/replace or the use of fields, to indexing. At some point it just ‘clicked’ and suddenly everything was very simple. The results of this learning process can now be shared with readers of _The Indexer_. For the general use of fields in Word, [Wempen (2011)](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#core-R4) and Microsoft<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#fn1" role="doc-noteref" id="body-ref-fn1">1</a></sup> are recommended.

One of the Word techniques that can also play an important role in indexing is pattern search, i.e. the use of regular expressions. Anyone familiar with pattern searches, for example in Cindex or another dedicated indexing program, will immediately understand the pattern searches described below. For others, the principle is explained so that the searches can be understood. Useful explanations and tips for searching/replacing can be found in any of the better Word manuals. Especially recommended are [Wyatt (2014)](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#core-R5) and the website of the Word MVPs (Most Valuable Professionals).<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#fn2" role="doc-noteref" id="body-ref-fn2">2</a></sup>

As far as the use of fields is concerned, in the standard cases of indexing it is sufficient to take a closer look at the PAGE field in addition to the XE field and the index field. Its typical use in Word documents (for paginating the pages) should be familiar to everyone, but, as shown below, the PAGE field can extend the possibilities of indexing with Word enormously.

However, the decisive step towards answering the above questions is not a technique provided by Word, but a certain procedure for creating the XE fields. The so-called ‘shifting method’ is used, which is discussed in detail below. The method is described in more detail in [Greulich (2020c)](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#core-R3).

## Arrangement of see also cross-references

We begin with _see also_ cross-references (later referred to as _see also_ references), because the principle of shifting can be demonstrated most easily with them. If a _see also_ reference starts from a main entry, it is always placed directly behind the main entry. This is how Word is set up. In principle, however, such a cross-reference could also be arranged at another location, such as at the end of a list (i.e. after all other sub-entries). This is even preferred by many publishers. Unfortunately, there is no switch in Word with which the arrangement of cross-references can be easily influenced. In order to achieve this, the cross-reference text itself must be treated as a sub-entry. This means that it is moved down one index level.

The following case is given:

> InDesign 315–30, _siehe auch_ FrameMaker
> 
> Gesamtindexerzeugung 324–30
> 
> Indexmarken 317–23
> 
> Platzierung von Dokumenten 316
> 
> Zwischenüberschriften 327

Here, the XE field belonging to the _see also_ reference (‘siehe auch’ in this German index) has the appearance:

> { XE „InDesign“ \\t „siehe auch FrameMaker“ }

This is the usual syntax for cross-references. To achieve the following arrangement:

> InDesign 315–30
> 
> Gesamtindexerzeugung 324–30
> 
> Indexmarken 317–23
> 
> Platzierung von Dokumenten 316
> 
> Zwischenüberschriften 327
> 
> _siehe auch_ FrameMaker

the XE field has the syntax

> { XE „InDesign:siehe auch FrameMaker;zzz“ \\t „“ }

**Explanation:** A new index level (in this case, a second one) is opened by entering a colon after the main entry in the XE field. In order that the resulting sub-entry is arranged at the end of all sub-entries to the same main entry, a special sorting must be requested. This is done by entering a semicolon and the sort text ‘zzz’. Since this is a cross-reference, no page number may be output. This is achieved using the \\t switch and the two quotation marks, between which no text is entered. The function of the \\t switch here is simply to suppress the output of a page number.

_See also_ references can be built up as soon as they are created in such a way that they appear in the index at the end of the list of subheadings. If, however, the decision is made to rearrange the _see also_ references during the middle or at the end of the project, it can be done with a search/replace routine:

> Search for (pattern search): “ (\\\\t) “(siehe auch \[A-zÄÖÜäöüß\\-\\;\\.\\(\\)“0-9\]@)“
> 
> Replace with (replace all): :\\2;zzz” \\1 “”

**Explanation:** The backslash \\, round and square brackets and the @ character (and other characters not mentioned here) play a special role in the pattern search. The search is performed using a quotation mark, followed by a space and the switch \\t. Since \\ has a control function in the pattern search, a second backslash must be placed before it, to instruct Word to actually search for a backslash as a character. Round brackets are placed around the expression \\\\t to form a group. Groups can be referred to later (when replacing). After the switch comes a space and another group (again introduced by a round bracket). This group looks a bit more complicated. It is an instruction to search for any combination of letters, numbers and special characters. Such a combination is put in square brackets. A–z means that the search covers all letters of the alphabet in upper and lower case, and 0–9 means that the search covers all digits from 0 to 9. The only special characters listed here are the hyphen \\-, the period \\., the semicolon \\; and the round brackets \\( and \\). Whether other special characters must be included in the search depends on the situation. All characters searched for should not only occur in any combination, but also as often as desired, which is expressed by the @ sign. Finally, another quotation mark is required. To be able to perform a pattern search in Word, the check mark ‘Use wildcards’ (‘Platzhalter verwenden’ in German) must be set in the search/replace window.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2020.36/asset/a4227fcd-2d83-4f09-9ba0-89648d9fcb63/assets/graphic/indexer_2020_36_fig1.jpg)

Figure 1. Pattern search in Word

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#F1)

Another advantage of these search/replace routines is that they are independent of the index level where the \\t switch is located. All cross-references are moved down one level with the same search/replace run. This means that even a cross-reference that starts from a sub-entry, for example, ‘lands’ at the correct position, in this case in the third index level.

Conversely, if all _see also_ references are arranged at the end of lists of subheadings, they can easily be brought directly to the main entry with an appropriate pattern search. If it seems too laborious to set up this pattern, a ‘normal’ search can also be used. The goal is to move the cross-references so that they become the first sub-entries of the respective sets. This is achieved with the following search/replace routine:

> Search for (normal search): ;zzz
> 
> Replace with (replace all): ;111.

The control via search/replace routines makes the shifting method extremely flexible. It is possible to switch from one arrangement to another in a few seconds. This is even more true when the cross-references are in a separate file (see [Greulich 2020a](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#core-R1)).

## Shifting method: principle and properties

The principle of shifting, using cross-references as an example, generally consists of moving information in the XE field to a new, deeper index level, or even creating information in this level in the first place. In practice, the principle is simply implemented by entering a colon.

It should be mentioned here that the shifting method is not limited to Word, but can also be used in other programs that have an embedded-indexing function, such as OpenOffice/LibreOffice, InDesign and FrameMaker, and even in ebook-creation programs like Jutoh ([www.jutoh.com](http://www.jutoh.com/)). It therefore does not seem exaggerated to call it a universal method. In these programs, it boils down to moving the information within the index entry or index marker window.

Because of its universality, the method is ideal for exchanging index data between Word and other embedded-indexing programs. But it is important to note that some of these programs (like InDesign) only allow four entry levels. So to avoid losing anything, information in Word may only be moved up to the fourth level at most. For example, _see also_ references that have been moved to the third index level in Word would also be in the third level in InDesign, because, technically speaking, these shifted _see also_ references are no different from other entry text. However, all these _see also_ references in InDesign would be provided with a page reference when the index is output. However, these unwanted page numbers could easily be found and removed with a simple pattern search (GREP – Global Regular Expressions Print). A particularly positive feature is that page-range specifications can be exchanged using the shifting method. This is not possible with page-range specifications based on bookmarks (in Word), formatting marks (InDesign) or range-building blocks (FrameMaker). This is discussed in more detail below.

The shifting method can also be used with Index Manager, in which it is also true that shifted information is technically no different from other information.<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#fn3" role="doc-noteref" id="body-ref-fn3">3</a></sup> The full potential of the shifting method in Word becomes apparent when it is combined with another Word method, namely the field-in-field method (also known as the nested-field method). Then all answers to the questions asked at the beginning of the article can be found.

## Use of fields in indexing: the ‘field-in-field’ principle

All authors, editors and proofreaders who use Word for writing cannot avoid using certain fields. One field stands out: the PAGE field. Without this, documents cannot be easily paginated. How it is inserted into a Word document is described in every Word manual. It is done using the Insert function:

> Menu \[Insert – Quick Parts – Insert Field\]

In the dialog box that appears, the PAGE field can be selected and inserted with OK.

The PAGE field belongs to a certain class of fields, namely those that can be inserted into other fields and provide useful results here. This property of the PAGE field is important for indexing. The PAGE field also belongs to the information-extracting fields, not to the information-generating fields. This is because the information about which page a piece of text (such as an XE field) is located on is already present in the document due to the pagination made by Word; it only needs to be extracted. Information-generating fields are, for example, fields for generating numbers, such as the ListNum or SEQ field.

The insertion of fields in other fields is basically always possible, but often such fields are then no longer active. Microsoft has made sure that the PAGE field can be built into the XE field and displays the page number here. If the index is now created, the PAGE field page number can also be seen in the index. Then (surprisingly) the entry has two page numbers: the page number supplied by the index function and the PAGE field page number. The purpose of including the PAGE field in the XE field is discussed below.

For example, after the PAGE field is placed in the XE field, it looks like this:

> { XE “{ PAGE } main heading” }

The position of the PAGE field (or any other built-in field) is not limited to a specific location within the XE field. The only restriction is that it must always be between the quotation marks of the entry text or the quotation marks after the \\t switch, as here:

> { XE “main heading:subheading { PAGE }” }

or here:

> { XE “main heading” \\t “{ PAGE }” }.

What purpose can the PAGE field serve? After all, in the end it provides nothing more than the indexing function itself, namely the page number. The difference between the two processes is that, as the user, the indexer has virtually no influence on the page number generated by the indexing function, but can deliberately insert and manipulate the page number at certain positions in the XE field using the PAGE field. It is precisely this flexibility that makes it possible to easily insert page-range specifications and annotations (decorations) to page numbers, for example, or to convert Word indexes into functional ebook indexes. How to deal with the double display of page numbers is described below.

The PAGE field is not updated automatically. To display the current values in the index, the entire document should be marked with <Ctrl-A> and then updated with <F9>.

## Page-range specifications with code shifting and insertion of the PAGE field

For page ranges to appear in a Word index, there must actually be bookmarks in the document, as described in all Word manuals. The name of the ‘matching’ bookmark must be specified in the index entry window or in the XE field. This procedure is cumbersome and time-consuming and is therefore rarely used. Even add-ins such as DEXter, DEXembed or WordEmbed do not bring great improvement here, because they also require the use of bookmarks. The biggest disadvantage of using bookmarks for page-range information is that they cannot be easily transferred to subsequent programs (such as InDesign). This means that in most cases important information is lost here and must be laboriously reinstated later or be left out.

On the other hand, page-range specifications provide important information for the reader. It would therefore be desirable to find a method that reduces the effort involved. There is only one additional program that really does bring an improvement: Index Manager. But this is not the subject of this series of articles. People who only create an index from time to time will buy neither one of the mentioned add-ins nor Index Manager. However, as noted in the first article of the series [Greulich (2020a)](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#core-R1), it is useful for professional indexers to have this background information on indexing with Word, so that they can explain in discussions with authors, editors and proofreaders how to create good indexes without a major technical add-on, using only the resources provided by Word. And a criterion for a good index is the presence of (not too few) page-range specifications.

When specifying ranges, it is always a question of marking the beginning (start) and the end. So the proecedure is to insert, at the start and at the end of the range, an XE field, which carries a corresponding identification, a coding, in addition to the actual content. The main requirements for codes for page ranges are that they should be universally applicable and require only a small additional effort. Both can be achieved by working with the shifting method and the PAGE field.

The overall procedure consists of two stages. In _stage 1_, the entries in the document are defined and edited – the index is written. In this writing stage, the shifting method is used, but it is not necessary to worry about the PAGE field. It is important that the growth of the index is permanently monitored (see part 1 of this series – [Greulich, 2020a)](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#core-R1), which only works if the index is kept in a separate file; the cross-references should also be created in a separate file. The writing stage lasts as long as the content of the document and also the index is being worked on.

In _stage 2_, the index is output in its final form. Content corrections should no longer be made. If necessary, go back to stage 1 and then reopen stage 2. Stage 2 is purely technical. It mainly involves search/replace routines; manual intervention is almost unnecessary.

In practice, each stage could be assigned to a different person. In this way an indexer could concentrate on the work of stage 1 and would only have to pay attention to a few things so that everything is prepared for stage 2. And a technically oriented person, such as a typesetter or designer (or a student at the institute of the author/indexer), could then do all the work of stage 2. In my experience, however, many authors, editors and proofreaders are so familiar with the technology of Word that, once they have written the index, they can also master the technical challenges of stage 2. This, I guess, holds for many professional indexers too. At least such skills can’t hurt.

### Stage 1: input of start and end codes

The entries are created in the writing stage. As soon as a page range is to be specified, codes must be entered in addition to the actual entry text. The angle brackets < and > can be used as codes. They are inserted in a new index level in an XE field as an identifier for the start or end of the range, for example:

> { XE “PDF-Dateien:als Datenquelle:<“ }
> 
> { XE “PDF-Dateien:als Datenquelle:>“ }

where the two entries shown may be on different pages, for example 223 and 224. The new index level is identified by a colon. It is important that it is the lowest level of an entry. In this example, the codes are in the third index level because there is already a second level with the subheading ‘als Datenquelle’.

A start-page entry is defined as usual (highlight word, press <ALT-Shift-X>, OK ), then colon and < are entered at the end in the resulting XE field. If necessary, the contents of the field are edited. Now the field is copied and inserted on the end page of the range. Here, the ‘<’ must be changed to a ‘>’. Thus a page range specification can be created with very little effort.

Parallel to the input, the index should be observed. [Figure 2](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#F2) shows an excerpt from an index which also shows how the two above entries for ‘PDF-Dateien:als Datenquelle’ are presented.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2020.36/asset/07a08351-7de7-45cc-bfb7-cd75cb57aef5/assets/graphic/indexer_2020_36_fig2.jpg)

Figure 2. Index section with page-range coding during the write stage

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#F2)

‘PDF-Dateien, als Datenquelle’ is a special case, which will be dealt with separately below. Let us first look at how page ranges are represented in the index. The codes < and > appear as sub-entries, behind which the respective page reference is shown. < 78 and > 79 (for ‘Papyrus Autor’) or < 248 and > 249 (for ‘Parameter, Entscheidungsfindung’) mean 78–9 and 248–9 respectively. Bear in mind that this is not the final output form of the index, but the index as it is presented (and monitored) during the writing stage.

There are several special features in this section. For example, it is noticeable that the sort order of ‘Papyrus Autor’ is not correct. Here in the index, the reference on page 307 appears before the reference with the page range 78–9, but this is not a problem, because all sequence problems are solved automatically in stage 2.

In addition, two page references are given behind the start and end codes of the entry ‘PDF-Dateien, als Datenquelle’. This is because there is a second reference with a page range, namely 256–7. Since the codes are quite common sub-sub-entries, all page references belonging to the respective sub-sub-entry are listed, separated by commas. This is also automatically corrected in stage 2.

In the writing stage the index author should only assign the codes and accept small ‘imperfections’ while monitoring the index.

If the index is not made ready for printing in Word, but in a subsequent layout program, no further work is required on the XE fields in Word. The document status at the end of stage 1 can be transferred to InDesign, for example. The codes for the page ranges are also transferred to the layout program. How the codes are ‘resolved’ in InDesign and how the order of the entries is controlled will be the subject of a future article.

### Stage 2a: work steps before issuing the final index

If the index is to be completed in Word, stage 2 begins, which is divided into steps to be carried out in the XE fields in the document (stage 2a) and steps in the index itself (stage 2b). The most important point in stage 2a is the inclusion of the PAGE field in the XE fields. The idea here is to create all page references with the PAGE field and to do without the page references that the index function automatically provides. Only under this condition can the codes be converted into real page-range specifications and all sequence problems be solved. All work in stage 2 should be done in a copy of the Word document.

The following steps must be taken:

1.

At the end of all XE fields, the PAGE field is inserted in a new index level. This is not done manually, but in one go via search/replace. The XE fields that belong to the entries shown in [Figure 2](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#F2) are spread over several pages. The situation shown in [Figure 3](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#F3) would arise for them after the PAGE field has been inserted (note that the page range codes and the colons that indicate a new index level are highlighted).

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2020.36/asset/97c524f0-1da9-40cb-ba7b-9aa2cff2ceb2/assets/graphic/indexer_2020_36_fig3.jpg)

Figure 3. The index from [Figure 2](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#F2) after the PAGE field has been inserted

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#F3)

2.

Now page-range codes and the PAGE field are placed in the same index level, which formally means nothing else but removing the colon between both. Additionally (but simultaneously), an inversion is performed (again via search/replace): first PAGE field, then code. The inversion is important for sorting. So we get the situation shown in [Figure 4](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#F4).

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2020.36/asset/e3f21015-7c9e-4aa9-a731-63ba0baa774b/assets/graphic/indexer_2020_36_fig4.jpg)

Figure 4. The index from [Figure 3](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#F3) after the inversion of the PAGE field and page-range codes

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#F4)

3.

All PAGE fields are updated. To do this, switch off the display of non-printable characters, then select the entire document (<Ctrl-a>) and finally press <F9> to update the fields. It is important to note that only when the display of non-printable characters is switched off will the PAGE fields display the correct page numbers. _These page numbers are displayed directly in the XE fields_ (and then later in the index, of course)!

4.

For all subsequent steps, it is important that the page information is retained in the XE field. This means that the field function of the PAGE field must be cancelled; the contents must be fixed. There are two possible ways of doing this, which are described in the Appendix. The first one is rather easy, the second one is for people who like challenges.

5.

The page number is located at the lowest index level, just like normal text. It is therefore sorted alphanumerically, like text. In the index, for example, 11 would come before 2, 236 before 8, and so on. This problem can be solved by inserting leading zeros via search/replace. If the highest page number has three digits (that is, 999 or less), a leading zero is inserted before two-digit page numbers in the XE field, and two zeros are inserted before one-digit page numbers. The example in [Figure 4](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#F4) then looks like that shown in [Figure 5](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#F5).

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2020.36/asset/9827465e-90bf-4a59-bdfc-cc9875f59174/assets/graphic/indexer_2020_36_fig5.jpg)

Figure 5. The index from [Figure 4](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#F4) after insertion of leading zeros

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#F5)

The completion of stage 2a marks another milestone. In this state the document can be transferred to an ebook program. The only ebook program known to the author that is capable of processing XE fields from Word is Jutoh. What the further processing with Jutoh looks like will also be described in a subsequent article.

### Stage 2b: work steps in the index up to its final form

If the index is to be output in its final form directly in Word, a few more steps are necessary.

1.

The index (which is contained in a separate file) is updated (<F9>). Among other things, all entries are automatically re-sorted. The index is then fixed with <Ctrl-6> or <Ctrl-Shift-F9>. Fixing is the prerequisite for the index to be able to get its final form by means of several search/replace runs. The most striking feature of the overall index is that all page numbers occur twice: once as page numbers generated by the PAGE field, and once as page numbers generated automatically by the index function. The index section for the above example looks like this:

> Papyrus Autor
> 
> 061 61
> 
> 078< 78
> 
> 079> 79
> 
> 307 307
> 
> Parameter
> 
> Entscheidungsfindung
> 
> 248< 248
> 
> 249> 249
> 
> PDF
> 
> als E-Book-Format
> 
> 263 263
> 
> PDF-Dateien
> 
> als Datenquelle
> 
> 223< 223
> 
> 224> 224
> 
> 256< 256
> 
> 257> 257
> 
> Umwandlung in EPUB
> 
> 092 92
> 
> PDF-Indexe
> 
> 079< 79
> 
> 082> 82

As can be seen here, as mentioned above, all sequencing problems have been solved as if by magic. In ‘Papyrus Autor’, the 307 comes after the 79 as desired, and the page-range specifications in ‘PDF-Dateien, als Datenquelle’ are unbundled and are placed in the correct order.

Now there are still some tasks to be done to give the index its final form. All the following steps are done by search/replace, where it is always possible to choose REPLACE ALL. The search/replace routines are described in the Appendix.

2.

All index-function page numbers are deleted, leaving only the PAGE field page numbers.

3.

Each from–to specification is brought into one line.

4.

Before the page references of an entry can be merged and arranged correctly, an intermediate step must be taken: due to the special behaviour of Word when deleting paragraph breaks via Find/Replace, the styles of the paragraphs with page numbers must be ‘normalized’. This means that paragraphs that are assigned the style _Index 2_ receive the auxiliary code # before the page numbers and are assigned the style _Index 1_, paragraphs of the style _Index 3_ receive the auxiliary code ## and the style _Index 2_. If further index levels are available, they are treated accordingly. The above example then has the following appearance:

> Papyrus Autor
> 
> #061
> 
> #078–079
> 
> #307
> 
> Parameter
> 
> Entscheidungsfindung
> 
> ##248–249
> 
> PDF
> 
> als E-Book-Format
> 
> ##263
> 
> PDF-Dateien
> 
> als Datenquelle
> 
> ##223–224
> 
> ##256–257
> 
> Umwandlung in EPUB
> 
> ##092
> 
> PDF-Indexe
> 
> #079–082

5.

The page numbers are merged and pulled up to the entry texts. At the same time the auxiliary codes are removed. The result is:

> Papyrus Autor, 061, 078–079, 307
> 
> Parameter
> 
> Entscheidungsfindung, 248–249
> 
> PDF
> 
> als E-Book-Format, 263
> 
> PDF-Dateien
> 
> als Datenquelle, 223–224, 256–257
> 
> Umwandlung in EPUB, 092
> 
> PDF-Indexe, 079–082

6.

If desired, the comma can be replaced by a double space after the entry text:

> Papyrus Autor 061, 078–079, 307
> 
> Parameter
> 
> Entscheidungsfindung 248–249
> 
> PDF
> 
> als E-Book-Format 263
> 
> PDF-Dateien
> 
> als Datenquelle 223–224, 256–257
> 
> Umwandlung in EPUB 092
> 
> PDF-Indexe 079–082

7.

The leading zeros are deleted:

> Papyrus Autor 61, 78–79, 307
> 
> Parameter
> 
> Entscheidungsfindung 248–249
> 
> PDF
> 
> als E-Book-Format 263
> 
> PDF-Dateien
> 
> als Datenquelle 223–224, 256–257
> 
> Umwandlung in EPUB 92
> 
> PDF-Indexe 79–82

With this, the index has reached its final form. Of course, the orphaned sub-entries would still have to be pulled up to the main entries and separated by commas. But this is a problem of all embedded indexes and has nothing to do with the method described here for generating page-range specifications. Furthermore, only a section of the complete index is shown here. If there should be further sub-entries, the problem of single sub-entries would solve itself.

## Conclusion and outlook

The shifting method is used to create a new index level and move important existing information to it (e.g. _see also_ references) or enter it here (e.g. a code like < or >). With the combination of the shifting method, code entry and inclusion of the PAGE field, both cross-references and page-range specifications can be easily and flexibly brought into an index. The shifting method and code input are intuitive to use and hardly prone to errors. To produce the final index after the writing stage (stage 1), depending on how the index is to be further processed, further steps are necessary (stages 2a and 2b), the most important of which is the insertion of the PAGE field. Here, find/replace routines with pattern searches are used.

To ensure that the overall process is fast and without input errors, the find/replace routines should be packed into macros. The macros for stage 2a must be VBA macros, because they are the only ones that can be used to address Word fields. The macros for stage 2b, on the other hand, could also be executed with an external macro program or by Perl or Python script. However, the latter would mean that the indexer would be acting as a programmer, which many indexers (or authors/editors) might not feel confident enough to do. Ready-to-use VBA macros for both stages (2a and 2 b) can be downloaded from the author’s website.<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#fn4" role="doc-noteref" id="body-ref-fn4">4</a></sup>

For page-range specifications, the code shifting procedure offers the great added value, compared to the bookmark procedure, that the codes and thus the range specifications are automatically transferred to further processing programs.

The shifting method also offers two further advantages:

•

Page-number decorations can be treated in the same way as page-range specifications. The steps described above in stages 2a and 2b apply equally to decorations; i.e. no additional work is required to convert them into a fully formatted index (as will be shown in a later article).

•

Based on the shift to the lowest index level, the ebook program Jutoh can automatically link all page references (including range specifications and decorations) (as will also be shown later).

## Footnotes

3

To find out more about cooperation between Word and Index Manager, please contact the author directly.

5

Double spaces are the standard setting in German indexes; in English indexes it’s sometimes a comma followed by a space. The setting can be adjusted by the switch \\e in the index field (see any good Word manual or [Greulich 2020c)](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#core-R3).

## Appendix: find/replace routines

### Steps in stage 2a

All searches are pattern searches, unless otherwise specified.

| Search for | Replace with (REPLACE ALL) |
| --- | --- |
| **1\. Insertion of the PAGE field in the lowest level of all XE fields:** |
| 
•

Switch on the display of non-printable characters (<Ctrl-\*>

•

Create, mark and copy a PAGE field anywhere in the document (i.e. put it on the clipboard), then :







 |
| (XE “\*)” | \\1:^c”  
The PAGE field is on the clipboard; ^c gets its contents. |
| **2\. Reverse the order of page range codes and PAGE field and bring both into the same index level:** |
| 

•

Switch on the display of non-printable characters (<Ctrl-\*>

•

Switch on display of the field syntax (<Alt-F9>

•

no pattern search, but usual search







 |
| :<:^d PAGE  
:>:^d PAGE | :^c<  
:^c> |
| **3\. Update the entire file by field.** |
| 

•

Switch off display of non-printable characters (<Ctrl-\*>)

•

Select entire document content (<Ctrl-A>)

•

Press <F9>







 |
| **4\. Fix PAGE field within all XE fields:**  
**a)**

•

Switch on the display of non-printable characters (<Ctrl-\*>

•

Select entire document content (<Ctrl-A>)

•

Press <Ctrl-6> or <Ctrl-Shift-F9>

  
**b)**

•

or run a macro that goes from PAGE field to PAGE field and fixes them





 |
| **5\. Insert leading zeros:**

•

Switch on the display of non-printable characters (<Ctrl-\*>, then:





 |
| :(\[0-9\]\[0-9\]”)  
:(\[0-9\]\[0-9\]\\<”)  
:(\[0-9\]\[0-9\]\\>”)  
:(\[0-9\]”)  
:(\[0-9\]\\<”)  
:(\[0-9\]\\>”)  
:: | :0\\1  
:0\\1  
:0\\1  
:00\\1  
:00\\1  
:00\\1  
: |

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#tabular-1)

In this state the Word data can be transferred to Jutoh. Jutoh automatically links the page references, so that an ebook with a functional index is available.

The data can be transferred to InDesign at the end of stage 1. But InDesign can also work with the data from the end of stage 2a. The two ways require different search/replace runs in order to get the final index.

### Steps in stage 2b

All searches are pattern searches, unless otherwise specified. The name ((_Index 1_)) means style _Index 1_.

| Search for | Replace with (REPLACE ALL) |
| --- | --- |
| **1\. Update the index once again and then fix it:**  
•

Update (<F9>)

•

click in the index, then press <Ctrl-6> or <Ctrl-Shift-F9>







 |
| **2\. Delete all ‘Word’s own’ page numbers** |
| ((double space)<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#fn5" role="doc-noteref" id="body-ref-fn5">5</a></sup>)<\[0-9\]{1;3}> | ((nothing)) |
| **3\. Bring from–to specifications into one line:** |
| (\[0-9\]{3;3})\\<^013(\[0-9\]{3;3})\\>  
^013 is the code for the paragraph break | \\1–\\2 |
| **4\. Normalize styles:** |
| (<\[0-9\]{3;3}>–<\[0-9\]{3;3}>) ((_Index 2_))  
(<\[0-9\]{3;3}>) ((_Index 2_))  
(<\[0-9\]{3;3}>–<\[0-9\]{3;3}>) ((_Index 3_))  
(<\[0-9\]{3;3}>) ((_Index 3_)) | #\\1 ((_Index 1_))  
#\\1 ((_Index 1_))  
##\\1 ((_Index 2_))  
##\\1 ((_Index 2_)) |
| **5\. Merge page numbers and simultaneously pull them up to the entry text:** |
| ^013#(\[0-9\]{3;3}) ((no formatting))  
^013##(\[0-9\]{3;3}) ((no formatting)) | , \\1 ((no formatting))  
, \\1 ((no formatting)) |
| **6\. If desired, replace the comma after the entry text with a double space:** |
| (\[A-zÄÖÜäöüß\\)\]), (\[0-9\]{3;3}) | \\1 \\2 |
| **7\. Delete leading zeros:** |
| <00(\[1-9\])>  
<0(\[1-9\]\[0-9\])> | \\1  
\\1 |
| **8\. Last check and correction** |

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.36#tabular-2)

## References

Greulich, W. (2020a) ‘Embedded indexing with Word: new light on an old topic. Part 1: how to monitor creation of an index’, _The Indexer_ 38(2), 207–18.

Greulich, W. (2020b) ‘Embedded indexing with Word. Part 2: editing entries and making work easier by using macros’, _The Indexer_ 38(3), 291–306.

Greulich, W. (2020c) _Indexing mit Word_. Hamburg: tredition.

Wempen, F. (2011) _Microsoft Word 2010 in depth_. Indianapolis: Que Publishing.
