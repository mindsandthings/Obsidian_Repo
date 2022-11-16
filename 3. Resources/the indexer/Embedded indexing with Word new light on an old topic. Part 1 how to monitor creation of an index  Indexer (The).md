---
created: 2022-11-14T09:19:44 (UTC -08:00)
tags: []
source: https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.18
author: Walter Greulich
---

# Embedded indexing with Word: new light on an old topic. Part 1: how to monitor creation of an index | Indexer (The)

> ## Excerpt
> In the first of a series of articles on the under-exploited potential for using Microsoft Word as a tool for embedded indexing, the focus is on how to monitor an index while it is being created. It...

---
Publication: The Indexer: The International Journal of Indexing

Volume 38, Number 2

## Abstract

In the first of a series of articles on the under-exploited potential for using Microsoft Word as a tool for embedded indexing, the focus is on how to monitor an index while it is being created. It covers the use of window splitting, the advantages of having the index and the cross-references in separate files, how to keep track of recently added entries using highlighting, and how to index several documents that are part of one project. In addition, the use of the RD field is explained, and instructions for writing simple macros are given.

Over the years every professional indexer has found the best and most effective working methods for themselves. And when someone revisits a method of embedded indexing that has been around for many years, and has been rejected by many colleagues for good reasons, it can seem a little strange.

But there are at least two reasons why the story of indexing with Word should be retold:

1.

The great potential that Word offers in indexing has apparently not yet been recognized.

2.

Besides professional indexers, there are a number of other people who do indexing exclusively with Word, especially authors and copy-editors.

Indexing with Word involves much more than just using the indexing functions offered. In this respect Word does not differ from stand-alone indexing programs such as Cindex, Macrex or Sky: effective work is only possible if the software is mastered far beyond the basic functions and the indexer knows how to achieve a certain result – no matter whether particular technical features are used. The goal is always to obtain a good index. A good index should meet the generally accepted criteria, but in addition it must also meet the requirements defined by the client. Good indexes can also be created effectively with Word. However, Word is much more comprehensive than a specialized indexing program. Finding out what features and capabilities of Word can be used for indexing is not easy. A review of the literature (e.g. Browne and Jermey, [2007](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.18#core-R3); Clendenen, [2003](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.18#core-R4); Haskins, [2010](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.18#core-R5); Leise et al., [2008](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.18#core-R7); Mauer, [2003](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.18#core-R19)) on indexing with Word reveals that the program has been poorly understood and appreciated (see the author’s review notes with the reference list at the end of this article for further details).

For indexing with Word, in addition to the indexing functions, users should be familiar with

•

the organization of Word files (where particular files are located, how information can be interchanged between various files)

•

templates and styles (how to connect templates with index files, how to create and change styles)

•

fields (for example RD field, Page field, StyleRef field, SEQ field)

•

macros (e.g. macros for entry highlighting or double posting)

•

search and replace (the pattern search is especially important).

These are only the most important points. Without a solid experience in using the program itself, effective indexing with Word is not possible.

Most indexes are made by people who have experience in writing and editing documents, but who find indexing very difficult. These people do not read _The Indexer_, but we as indexing professionals have to deal with these people again and again and should not miss any opportunity to talk to them about good indexing. Most of them will never buy a stand-alone indexing program, but will continue to work with the features available in the text and layout programs they use. Experience suggests that they are happy to receive suggestions for making their indexing work more effective. And there are quite a few things that make indexing in Word or InDesign easier, so that better results can be achieved.

Therefore this and subsequent articles take a fresh look at this old issue, and it is likely that readers will have some ‘aha!’ experiences.

The first part of this small series on indexing with Word focuses on an aspect that is of essential importance in improving the quality of an embedded index: how the growth of an index can be permanently monitored. The second part will show how basic index editing functions can easily be brought into Word. These methods make some operations so much easier that many indexers will probably see for the first time some sense in embedded indexing. These basic editing methods can be reduced to a handful of main functions. When these are applied, an enormous amount of time is saved. Subsequent articles will be devoted to applications of what may be referred to as the ‘shifting method’, which makes it possible to easily solve problems that were previously considered unsolvable:

•

implementing page-range specifications in Word in a very simple way, without bookmarks

•

adding suffixes to page references, so that specifications like 37n or 58t become possible

•

how a Word index can be passed on to an e-book and how page references are not only retained in the e-book but are active.

## How to constantly observe the growth of the index

One of the drawbacks of embedded indexing in Word is often said to be that while creating index entries, it is not possible to observe at the same time how a new entry is sorted into the index. Therefore it is not possible to make immediate changes that contribute to the quality of the index. One does not ‘swim’ in the index, but only has a small portion (namely the current XE field) visible. However, this is only partially correct.

### Window splitting

Provided that the screen on which the document is viewed is deep enough to see more than one page, the view can be split. (It can also be split on a smaller screen, but then working becomes cumbersome.) This can be done as follows:

1.

Select: Menu \[View – Window group – Split\]. The horizontal split bar appears, dividing the window into an upper and a lower half. The bar can be clicked and moved while holding down the left mouse button. Releasing the mouse button divides the window at this point. Double clicking on the bar cancels the division.

2.

Navigate to the index in the lower part of the window (<Ctrl-End>, then scroll). The document text is unaffected and remains visible in the upper window, and can be edited here.

3.

To move from the upper subwindow to the lower subwindow, use the key combination <Shift-F6>; to move from the lower to the upper, use the <F6> key. In this way it is easy to quickly jump back and forth.

Window splitting enables the indexer to check whether an entry already exists on another page of the document and how it was written (e.g. with or without hyphen, singular or plural, etc.). This means that some editing of the index can be done while the index is still being created.

To see the result of the editing – in other words, to observe the growth of the index – all that needs to be done is to press the <F9> key in the lower part of the window, i.e. in the overall index, which updates the index.

### Index in a separate file

By using a really big screen, or working with two screens, which is highly recommended, it is possible to go one step further: inserting the complete index in a separate Word file and viewing it there only.

The index in the second file must of course be ‘fed’ automatically by the entries in the document, just as if it were at the end of the document, as is usually the case. The index should be updated at the push of a button. All this is done using the so-called RD field, where RD stands for ‘Referenced Document’. This field (more details are described below) allows the creation of an index to one or even more Word documents in a separate file and displayed here in its current form. To do this, the RD field simply needs to be placed in the index file. In addition, the command for inserting the index must be called once. This means that at least two fields are contained in the index file (see [Figure 1](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.18#F1)):

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2020.18/asset/ab3758e7-31c4-44f2-80c4-2cd801cc49e6/assets/graphic/indexer_2020_18_fig1.jpg)

Figure 1. RD field and index field in the separately kept file in which the index is to be displayed

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.18#F1)

If several Word documents contribute entries to the overall index, an additional RD field is required for each document. The index field then displays the total index of all documents addressed via the RD fields. The RD field is made up of three parts (see [Figure 1](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.18#F1)):

2.

The specification of the file name of the reference file, i.e. the file for which the index is to be generated. The file name must be complete, including the file name extension .docx, and it should be enclosed in quotation marks.

3.

The switch \\f. This switch must be used if all files are located in the same folder. It tells the field exactly this, and only the file name needs to be entered in the RD field. The switch can be omitted, but then the full path for the file must be specified. For files that are located in different folders, the complete path must always be given.

The separate index file can be placed next to the content file currently being processed, on the same screen or on a second screen. Separation of content and index has the advantage that a large section of the index can constantly be seen, and that both documents are managed independently on the computer (which can be helpful in case of crashes, for example).

To switch from the index file to the contents file (or vice versa), use the key combination <Ctrl-F6> or simply click into the other file, since both are visible on the screen at the same time. In the index file, <F9> can be used again to update the index.

### Searching and selecting index terms

The separate index file has another advantage: when performing a search for a text string, Word searches only in the index and not in the text of the content document. This sounds obvious, but has surprising consequences. The most important one is that it forms the basis for consistency checks of an index. This is because it gives the option of concentrating on subsets of the entire index. There are two methods available for doing this:

1.

The command <Ctrl-f> calls up the navigation area, in which the search results are presented as a list. The list shows a subset of the entire index, which contains exactly the places of interest (see [Figure 2](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.18#F2)). This gives a quick overview of where and especially how a term has been used in the index: as main entry, as subentry, inflected, not inflected, etc. In this way, it is possible to find inconsistencies systematically. Next to the list, the locations where the term was found in the index are highlighted. In this way the environment around the search term can be seen and contexts can be easily recognized. For example, it may become apparent that a term is used both inside and outside an array of subentries. Structural errors can thus be found and corrected quickly.

2.

Even without the navigation area, all occurrences of the term of interest can be highlighted in the index by calling up the usual search/replace window and using the command <Text Highlighting> while searching. By scrolling through the index, the highlighted areas are drawn to one’s attention, enabling decisions to be made. I personally prefer the first method because it presents a list of the locations.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2020.18/asset/21d54410-cefb-46d8-afc6-2b26fda710ea/assets/graphic/indexer_2020_18_fig2.jpg)

Figure 2. Search for the term ‘Regel’ in the index. The results list is shown on the left, and the highlighting of a selected location on the right. The results list is the index subset of interest. Inconstencies can easily be found here.

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.18#F2)

The question is: how and where will the corrections be done? Of course it would be nice if these could be done directly in the index, i.e. at the places that were found by the search. This is not possible as long as the index is a field. The index field is automatically updated every time <F9> is pressed, but this means that any changes made are overwritten. Therefore, in order to make the corrections, go to the respective page in the content document and edit the corresponding XE field here. The relevant page number is shown after each term in the index. Going to the page consists of the following steps:

1.

Click in the content document or switch to the window using <Ctrl-F6>.

2.

Press the key combination <Ctrl-Shift-+> (i.e. <Ctrl\*>) so that the XE fields are not visible.

3.

Use key combination <Ctrl-g> to call the Go-To dialog box.

4.

Type in the page number and send the command by pressing the <Enter> key, then press <ESC> to leave the dialog box.

5.

Again use the key combination <Ctrl-Shift-+> to display the XE fields.

6.

Find the XE field in question on the page and click into it.

To edit several positions in succession, and if one is already in the content document, steps 2 to 6 are sufficient.

These five or six steps take only a few seconds to complete, once one is familiar with them. Having done the corrections, the index should be updated (<F9>).<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.18#fn1" role="doc-noteref" id="body-ref-fn1">1</a></sup>

Immediately a question arises: is there a way of easily getting to the changed entries in the index? How can changed sections be recognized in an ever-growing index? The solution is the highlighting of XE fields.

### Highlighting XE fields

It is very helpful if new or changed entries are emphasized with a different color than the existing entries. Old entries should have the format ‘no colour’. For this purpose an XE field is marked immediately after its creation or correction in the text and coloured with the text-highlighting function (to be found in the <Font Type> group on the Start tab). Examples of highlighting are shown in [Figure 3](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.18#F3). Afterwards, the index needs only to be updated and the colour is displayed here as well ([Figure 4](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.18#F4)).

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2020.18/asset/d20e9545-f5c8-42df-98eb-452ac908b966/assets/graphic/indexer_2020_18_fig3.jpg)

Figure 3. Highlighted index entries in the text

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.18#F3)

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2020.18/asset/21266311-b9a9-4349-973a-0cbfb86a3611/assets/graphic/indexer_2020_18_fig4.jpg)

Figure 4. Index with highlighted entries

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.18#F4)

This gives two positive effects:

1.

Each time the index is updated, all entries of the current session are highlighted in colour.

2.

When scrolling through the content document, it is easy to see where XE fields have been created or corrected during the current session.

Since manual coloring is rather tedious, it is preferable to use a small macro.

At the end of a session or at the beginning of another session of the same indexing project, all highlighting should be deleted. This can be done with Find/Replace or again by a macro.

Many macros can be recorded. To record the highlighting macro, use the following procedure:

•

Select the recording button.

•

Assign a name to the macro.

•

Click in the text before the XE field.

•

Search forward for the text ‘^d XE’ (^d stands for: look for the next field; the addition ‘XE’ tells Word to look for an XE field)

•

Click on <Highlight Text> and select the desired colour

The macro is now in Normal.dotm. To get straightforward access to the macro, assign a key combination to it or create a user-defined button in the ribbon. To apply the macro, click before an XE field, then execute the key combination or click on the button in the ribbon. By repeatedly using the key combination or pressing the button, several XE fields in a row can be highlighted.

### Managing cross-references

In principle, cross-references can be created at any point in a document. They are included in the overall index just like other entries. Their main characteristic, from a technical point of view, is the absence of a page number. However, this can make it difficult to edit the corresponding XE field while writing the index or at the end of the writing process. To jump to the appropriate page where the cross-reference XE field is located, it is not possible to use the Go-to function; instead the search function must be used. That is noticeably more time-consuming. If the index is only to be created for a single document, this additional effort may not play a major role, but if several documents belong to the same project, it is no longer clear from which file a cross-reference originates, because a file number is also not displayed. That means that it now becomes really laborious: the search function has to be used in several files to find the cross reference XE field; only then can it be edited.

To avoid this problem, it is recommended that the XE fields of all cross-references are kept in a separate file. In other words, no cross references are created in the actual content document, but all cross references are in the separate file. Each cross-reference XE field should be on a separate line, as shown in [Figure 5](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.18#F5).

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2020.18/asset/8155ac1f-29b9-43f2-945c-e1754a4b1756/assets/graphic/indexer_2020_18_fig5.jpg)

Figure 5. Example of a cross-reference file. Left, the entries ‘Quelle’ and ‘Nest’ have been added in the current working session at the end of the list. Right, after sorting they are in correct alphabetical order.

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.18#F5)

Each new cross-reference is simply inserted at the end of the list of cross-reference XE fields. Since each cross-reference XE field is on a separate line, the Word sort function can be used (AZ button in the ‘Paragraph’ group on the start tab) to put the cross-references in alphabetical order. This makes it very easy to find any cross-reference XE field that needs to be edited.

To display the cross-references in the overall index, another RD field needs to be added in the index file (see [Figure 1](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.18#F1)) that refers to the file with the cross-reference XE fields.

Checking the cross-references is now also easy. For this purpose, below the list of cross-references, one or more RD fields and the index field are added. The RD fields refer to the content documents so that the index field can ‘pull’ all entry information. To check a particular cross-reference, simply call the Find function (using Ctrl-f) and type in the text of the cross-reference. After transmission of the Find command, Word looks for the term in the file. A Find list is presented, in which it is very quick to check whether the term is present in the index. Necessary changes can be made just as quickly in the cross-reference list above the index.

### Observation of an index to several documents

With the index to a single document, it is easy to observe its growth, because there are only two files to deal with: the document file and the index file. It is easy to jump back and forth between the two files using <Ctrl-F6>. However, to index several documents belonging to the same project, the process can be difficult. There are three problems to be solved:

•

the creation of the entire index across all files

•

switching from the index file to the document files and back.

To create the overall index across multiple files, the RD field can be used again, or the sub-documents can be merged into a master document. There are several possibilities for page numbering: harmonizing the page numbers in the master document or, if working with separate files, applying a combination of RD and SEQ fields together with special field switches.<sup><a href="https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.18#fn2" role="doc-noteref" id="body-ref-fn2">2</a></sup>

To switch from one file to the next, the key combination <Ctrl-F6> can be used again. This displays the contents of the respective file. Press <Ctrl-F6> until you reach the file you want to switch to; then stop and perform the desired editing (the editing of one or more XE fields) here. When switching, orientation is made easier if the file names are numbered. It is a good idea to include chapter or sub-chapter numbers in the file names.

## Conclusion and outlook

Using separate files for the index and for the cross-references turns out to be a crucial step towards effective indexing in Word. The permanent observation of an index, as well as a software-aided cross-reference check, is possible with relatively simple means. Based on these techniques, editing tasks can be completed quickly and a higher-quality index can be achieved.

Future articles will show how advanced index requirements such as page-range specifications without bookmarks can be realized.

## Footnotes

1

Note that you can also apply the searches if the index has been converted to plain text by pressing <Ctrl-6> or <Ctrl-Shift-F9>. You usually do this at the very end. Any errors you find now can be corrected directly in the index.

2

For more information on this, please contact the author.

## References and review remarks

The choice of sources was made when reviewing a part of the literature available to me. It is not complete. Several well-known and perhaps expected names like David K. Ream or Jan C. Wright do not appear at all, although they have written several and important contributions to embedded indexing. Some of the cited authors will certainly have other publications describing embedded indexing with Word from different angles and with different priorities. I am not interested in criticizing or even exposing the authors, but I wanted to find typical statements about Word. I was surprised by the large agreement of most of the statements.

Only small excerpts are quoted from the respective publications. Whenever statements are taken out of context, a wrong impression can arise. I would like to apologize at this point if this should have happened.

Browne, G. and Jermey, J. (2007) _The indexing companion_. Cambridge: Cambridge University Press. On page 183, the authors state that, ‘Relatively little professional indexing is done in Word because it is too complex for hobbyists and not powerful enough for full-scale publishing.’ However, the indexing function is used by many hobbyists because the application of this function is relatively easy to learn, and as will be shown in following articles, it is very powerful and can meet almost all professional requirements. They also state, ‘Word indexing supports _see_ and _see also_ cross-references and one level of subheading’; however, it should be noted that in Word, nine (!) levels of subentry are possible.

Clendenen, J. (2003) ‘The trials and tribulations of embedded indexing with Word’, in S. Schroeder (ed.), _Software for indexing_. Medford, NJ: Information Today, Inc., pp. 99–104. The author states that leading-function words are not ignored for sorting. I assume what meant is that they are not automatically ignored (on account of a list which is offered). That is right. However, there is no problem with function words, because you can easily set a special sort (by using a semicolon after a heading). By using pattern search, it is possible to change the sort order of all instances of a function word at once. She also says that page ranges can only be brought in via bookmarks and not in an intuitive way; however, when using the code-shifting method (being described in a later article), page ranges are no longer a problem. On page 103, she states, ‘There is no way to group related terms when making an index in Word’. However, the grouping of terms is possible, although somewhat limited. You have to work with a separate file for the index and simply use the search function (Ctrl-f) here. In the navigation pane then a subset of all entries containing the searched term is presented.

Haskins, L. (2010) ‘Embedded indexing: learning the smart way to index in Adobe FrameMaker and Microsoft Word’, in J. Perlman and E. L. Zafran (eds), _Index it right! Advice from the experts, volume 2_. Medford, NJ: Information Today, Inc.

The author considers the embedding process using only Microsoft Word’s indexing module to be time-consuming and frustrating. However, embedded indexing in Word does not need to be particularly time-consuming nor frustrating; in fact, with a little practice it can be done very quickly. She also says that Word’s indexing module lacks some important features, that it does not provide a way to preview the index as it’s being built, and that its editing features are practically nonexistent. But if the index is kept in a separate file, it can be viewed quickly and at any time. The editing options simply need to be brought out. A few small macros already work wonders.

Leise, F., Mertes, K., and Badgett, N. (2008) _Indexing for editors and authors_. Medford, NJ: Information Today, Inc.

On page 121, the authors state the following in the context of embedding indexing software (not only Word):

‘Due to software limitations, it is more difficult to create a quality index by embedding terms than by using dedicated indexing software. Challenges presented by embedded indexes include:

• No global editing functions – It may not be possible to use a global editing function to edit index source tags; hence, each embedded term will have to be edited individually.

• Limited sorting options – It may not be possible to force-sort terms to sort them in page-number order. Some programs can, however, generate a list of tags.

• No tools for checking cross-references or double postings.

• Difficulty in creating page ranges in the index.’

Especially when addressing editors and authors, it does not help, I would say, to point out disadvantages without offering solutions. Using dedicated indexing software or add-ins is not an alternative for many editors and authors. Leise et al.’s specific concerns are addressed below:

• With Search/Replace a good possibility is available in Word to edit index terms globally; important: use of the pattern search.

• By skilful application of search/replace and the insertion of the page field in a suitable place it is no problem to sort entries by page number in Word.

• If the XE fields of the cross-references are all created in a separate file, a software-supported check of the references can be carried out easily; all that is required is to use the search function (Ctrl-f). Double postings can also be checked with the search function if the index is kept in a separate file.

• Page ranges are very easy to realize with the code shifting method.

Mauer, P. (2003) ‘Embedded indexing’, in S. Schroeder (ed.), _Software for indexing_. Medford, NJ: Information Today, Inc., pp. 83–98.

From this article (it is one among others) comes the estimate that the creation of an embedded index takes about two to three times longer than if a stand-alone indexing program were used (such as Cindex, Sky Index or Macrex). I can only partially agree with this, because Word itself offers ways to easily support the embedded-indexing functions.
