---
created: 2022-11-14T09:14:42 (UTC -08:00)
tags: []
source: https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25
author: Walter Greulich
---

# Embedded indexing with Word. Part 6 – sorting and export of entries | Indexer (The)

> ## Excerpt
> This series of articles on embedded indexing with Word concludes with two topics that are particularly important for all indexes: sorting and exporting the entries. How can you easily switch betwee...

---
Publication: The Indexer: The International Journal of Indexing

Volume 39, Number 3

## Abstract

This series of articles on embedded indexing with Word concludes with two topics that are particularly important for all indexes: sorting and exporting the entries. How can you easily switch between alphabetical sorting and sorting by page numbers? Is it possible to implement letter-by-letter sorting? Directly related to these problems is the question of exporting the index entries into a format understood by Excel or dedicated indexing programs. The first five articles in the series can be found in the June, September and December 2020 issues and in the March and June 2021 issues of _The Indexer_ (**38**(2), **38**(3), **38**(4), **39**(1), **39**(2)).

## Sorting index entries in Word: introduction

As noted in the other articles in this series, Word offers possibilities that surprise and impress when it comes to sorting. Once again, Word shows its full power only when different functions and approaches are combined. Here, we start with the obvious: the sorting possibilities of the indexing function. Later we will see how these possibilities can be extended – using Word’s own tools.

Word’s indexing function sorts wordwise alphabetically by default, according to ISO, which means that spaces are sorted as well, but hyphens are ignored. To force special sorting, a semicolon must be entered after the term in the XE field plus the spelling of the term to sort by.

For example, sorting ‘4-aminoazobenzene’ under ‘A’ rather than ‘4’ can be achieved if the corresponding XE field looks like this:

> { XE "4-Aminoazobenzol;Aminoazobenzol4-" }

Here the term is repeated after the semicolon, with the prefix ‘4-’ placed at the end (the prefix could also be omitted). This semicolon method of influencing sorting is familiar to anyone with some experience in embedded indexing with Word. One of the first to point it out was Seth [Maislin (2003)](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#core-R9).

The semicolon method can be used to satisfy basically any conceivable request for sorting index entries. For example, it could also be used to sort entries by page numbers. To do this, simply add the PAGE field after the semicolon according to the same principle:

> { XE "Hauptthema; { PAGE }" }

Likewise, it would be possible to force a letter-by-letter sort by repeating a multi-word term without spaces after the semicolon, such as

> { XE "New York;NewYork" }

In indexing projects, the type of sorting – wordwise or letterwise – is usually specified in advance and not changed during the project. In most cases, Word’s default setting – ISO word-by-word sorting – is used, and the indexer does not need to take any special action (except in special cases). If letter-by-letter sorting is the goal, the indexer can adjust each XE field accordingly as soon as it is created. This is a certain additional effort, but it is kept within limits, because only index terms consisting of several words are affected by the adjustment.

However, there are situations where there are further requirements for sorting. For publishers and also for indexers it can be interesting to use an already created index in multiple ways. The following scenarios are conceivable (I present only four that are particularly important from my point of view):

•

An indexer may sometimes want to be able to sort an index by page or even chronologically (i.e. in the order of occurrence of the XE fields in the text) and without much effort, in order to take a different look at the current result and to be able to edit the index better.

•

When working on a new edition, sorting the index entries of the previous edition page by page or chronologically enables the indexer to understand more quickly how it was created. A prerequisite for this is the availability of the Word files of the previous edition with built-in XE fields.

•

The terms of an embedded index should be exported without much effort so that they can be further processed in Excel, in a dedicated indexing program or in a database.

•

The indexes within a book series may be created in various ways, partly with dedicated indexing programs, partly by embedded indexing; for the sake of uniformity, all indexes should be sorted by letter by letter. With indexes based on dedicated indexing programs, this can be done at the push of a button. But how can an existing embedded index, which is sorted word by word by default, be converted to letter-by-letter sorting at a later date without much effort?

The key issue, therefore, is the desire to subsequently modify existing index entries to meet different sorting requirements. This article is dedicated to these issues.

## Sorting by page numbers

Let us first look at sorting by page numbers. In some steps towards this sorting, the contents of the XE fields must be changed so much that errors can happen when bringing it back to the original state. Therefore, for security reasons, it is advisable to work in a copy of the current ‘live’ document; the copy is simply obtained via ‘Save as’ (where the original file name can be supplemented by \_page, for example).

To achieve page-by-page sorting, the PAGE field must be inserted into all XE fields (for the field-in-field method, see [Greulich, 2020d)](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#core-R5). There are two possible places to insert the PAGE field:

•

at the very beginning of the entry text in the XE field, i.e. directly after the first quotation mark.

The pattern for the first insertion type is (as already mentioned):

> { XE "Main heading;{ PAGE }" }

and for the second it looks like this:

> { XE "{ PAGE } Main heading and possibly further entry text" }

Method 1 is obvious, because it is known that a special sorting is brought about by entering a notation or a value after a semicolon, according to which sorting is to take place. By including the PAGE field after the semicolon, sorting by page number is enforced. However, the PAGE field must be _manually_ built into each XE field; a macro would be conceivable, but is not trivial because there are many special cases. Most importantly, other existing sort instructions would have to be queried to find the appropriate insertion point. So the method would be relatively laborious and therefore cannot be recommended. It is mentioned here mainly for reasons of principle, because it would use the obvious way to influence the sorting.

In contrast, method 2 has the great advantage of being completely controllable by find/replace. As we will see, a few find/replace runs are sufficient to change the XE fields so that the index can be output ordered by page.

In order to be able to include the PAGE field in the XE fields, a little preparation has to be done. The PAGE field is temporarily inserted once at any position of the document (e.g. at the beginning), marked and copied. This makes it available as clipboard content for the further steps.

Now the _Replace_ window is opened (via ) and entered:

| Search for | Replace with |
| --- | --- |
| XE\_" | ^&^c\_ |

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#tabular-1)

_Explanation:_ The \_ character stands for the space character, which means that a space character must be keyed in its place. The beginning of each XE field is marked by the text XE followed by a space and a quotation mark. This find-what string is to be replaced by itself (^&) and supplemented with the contents of the clipboard (^c) and a following space. So the result would be as desired:

> { XE ”{ PAGE } main heading” }

With _Replace All_, all XE fields are equipped with the PAGE field. It is still important that all PAGE fields are updated, otherwise they will return incorrect page numbers. That means that the display of the field syntax is switched off (by <Alt-F9>), then the whole document content is marked, and finally <F9> is pressed.

Now the index can be created or updated. This should again be done in a separate file in which the RD field is used to refer to the content document (cf. [Greulich, 2020a)](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#core-R2). The cross-references should also be in a separate file; their content is also integrated into the index via the RD field. The index then looks like the example shown in [Figure 1](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#F1).

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.25/asset/4189d0e7-c02d-4cf4-9a49-39ffeddc5d88/assets/graphic/indexer_2021_25_fig1.jpg)

Figure 1. Index with page numbers at the beginning of the entries. Basically, the sorting is done according to the PAGE field page numbers, but if a special sorting is specified in the XE fields, this will take effect and the page-by-page sorting will get out of step (see right part of the figure)

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#F1)

Six things stand out here:

1

The entries are sorted alphanumerically: Word sorts the PAGE field page numbers at the beginning of the entries like letters. This is basically correct, because the numbers now belong to an alphanumeric text string: number and entry text are one unit (Figure 1, left).

2

Double naming of page numbers: in addition to the PAGE field page numbers, the page numbers that Word automatically assigns to each entry can also be seen. As usual, they are placed after the entry text and separated from it by two spaces (or by a comma and a space, depending on style requirements).

3

Subentries are in separate lines.

4

If a main entry with different subentries occurs several times on a page, Word also forms a nest for this main entry in the page-by-page arrangement (Figure 1, left: 107 LADME schema). Within the nest, the subentries are again sorted alphabetically.

5

The entries belonging to a page are sorted alphabetically within the page.

6

Since the PAGE field page number belongs to the text, entries for which a special sorting was forced by semicolon setting are not sorted by page number but according to this special specification. That is, here the page-by-page ordering is interrupted (Figure 1, right: 199 N-acetyltransferases (NAT) is sorted like acetyl-transferases). The fact that the PAGE field page number and the index function page number do not match (199 compared to 200) has another explanation, which can be found in [Greulich (2020c)](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#core-R4).

Since the page-by-page arrangement of entries is intended purely for checking purposes, and to get a quick impression of the distribution of entries across the entire document, only a few clean-ups need to be made, namely the following. (The numbers relate to the points in the above list.)

### _1\. Alphanumeric sorting_

The fact that the PAGE field page numbers are sorted alphanumerically disturbs the overall picture because this makes it impossible to check the entries quickly. In order to achieve a ‘clean’ sorting by page numbers, the page numbers at the beginning of the entries must be supplemented by _leading zeros._ Whether one, two or more leading zeros are needed depends on the number of pages in the book, as shown in [Table 1](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#T1).

Table 1. Insertion of leading zeros in page number sorting

| Number of pages | Number of leading zeros | Insertion where? | Examples |
| --- | --- | --- | --- |
| < 100 | 1 | Only for single-digit page numbers | 03, 08 |
| < 1,000 | 1 or 2 | For one- and two-digit page numbers | 003, 025 |
| < 10,000 | 1, 2 or 3 | For one-, two- and three-digit page numbers | 0003, 0025, 0654 |

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#T1)

The leading zeros are inserted directly in the XE fields (i.e. in the _content document)._ Here, too, a preparatory step is necessary first: the PAGE fields must be fixed (i.e. converted into ‘normal’ text). To do this, the entire document is marked with <Ctrl-a> and all fields (and thus also the PAGE fields) are updated with F9. If the selection is still active, the contents of the PAGE fields are fixed by <Ctrl-6>. That means that the field function of the PAGE fields is lost, and the PAGE field page numbers are now fixed numbers.

Now the leading zeros can be inserted with find/replace. Here we consider the case of a content document with more than 100 but less than 1,000 pages. This means that two zeros are to be inserted for single-digit page numbers and one zero for two-digit page numbers. The order of the two find/replace runs does not matter in principle, because with pattern search it is always possible to specify exactly what is being searched for. Here the sequence first for one zero, and then two zeros, is shown:

| Search for | Replace with |
| --- | --- |
| (XE\_")(<\[0-9\]\[0-9\]>\_) | \\10\\2 |
| (XE\_")(<\[0-9\]>\_) | \\100\\2 |

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#tabular-3)

_Explanation:_ The angle brackets in the search string express the instruction that whole words (in this case ‘words of digits’) are to be searched for. For example, <\[0-9\]> finds only one-digit numbers, <\[0-9\]\[0-9\]> only two-digit numbers, etc. The round brackets are used to form groups that can be referred to when replacing. The \_ character again stands for the space character, which means that a space character must be keyed in its place.

In the replace string, \\1 stands for the first group (i.e. XE "), followed by the leading zeros (0 or 00). \\2 stands for the second group (i.e. two- or one-digit numbers followed by a space). This means that the leading zeros are inserted between the two groups. If the index is now output, all entries are correctly sorted by page number. The result is shown in [Figure 2](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#F2). Leading zeros, as we will see, also play a major role in chronological sorting (see next section).

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.25/asset/f1865d8a-254c-4423-af4d-11ac3064016c/assets/graphic/indexer_2021_25_fig2.jpg)

Figure 2. After inserting leading zeros, sorting is done correctly by page numbers

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#F2)

### 2\. Page number duplication

If the duplicate page numbers are annoying, those generated by the index function (at the end of the entries) should be removed by search/replace. This is done directly in the _separate index file._ To do this, the index must first be fixed: click into it and press <Ctrl-6> or <Ctrl-Shift-F9>. The find/replace run for the page number at the end looks like this:

| Search for | Replace with |
| --- | --- |
| \_ \_ \[0-9\]{2;2}(^013) | \\1 |

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#tabular-4)

_Explanation:_ Here \_ stands again for a space character. ^013 is the code for the paragraph mark.

### _3\. Subentry display_

All embedded indexing programs (besides Word, e.g. also InDesign) always display individual (‘orphaned’) subentries in separate paragraphs (with indentation). Even in dedicated indexing programs this is usually the case, as long as no ‘reconciling’ has been done. It is recommended that this point is accepted rather than cleaning it up.

### _4 and 5. Nesting and alphabetical arrangement_

The nesting and the alphabetical arrangement of the entries belonging to a page correspond exactly to the picture that dedicated indexing programs also provide when sorting page by page. A clean-up is not appropriate, because it guarantees the clarity of the view of the index entries from another perspective.

### _6\. Special sorting_

Special sort specifications that ensure correct sorting in alphabetical output also take effect in the page-by-page output of the index. This means that the page-by-page arrangement is interrupted. This problem can be solved by replacing the semicolon in the XE field (now we are back in the _content file)_ with another character (e.g. the hash #). In order to achieve this via find/replace, one must manage to distinguish the semicolon in the XE field from other semicolons in the document text. To do this, all XE fields are first highlighted in colour (e.g. yellow). This is also done via find/replace:

| Search for | Replace with |
| --- | --- |
| ^d XE | ^& ((highlight color yellow)) |

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#tabular-5)

Now you can search specifically for the semicolon in connection with highlighting:

| Search for | Replace with |
| --- | --- |
| ; ((highlighting)) | # |

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#tabular-6)

The highlighting can be removed by selecting the entire document and then choosing _Highlighting: no colour._ If the index is now updated, all entries are correctly sorted by page number. An illustration of this is shown in the next section, which is about chronological sorting. It is worth noting that the procedure of highlighting the XE fields just described can basically be used whenever a search for any character is to be limited to the XE field. The highlighting then simply serves as an additional criterion during the character search.

## Chronological sorting

Page-by-page sorting is mainly for checking purposes. Chronological sorting – the arrangement of the entries in the order of their occurrence – has, as we will see, somewhat different characteristics and offers more possibilities of use.

How can chronological sorting be achieved using the tools within Word? To do this, a field must be used that starts at a number to be specified and then counts up in increments of one. The ideal field for this purpose is the SEQ field. SEQ stands for ‘sequence’. The syntax of the field is:

> { SEQ \[designation of the numbering run\] \[switch\] }

It consists of three parts:

•

the designation of the numbering run; this can be chosen arbitrarily, it can be e.g. ‘chron’

•

a switch that specifies how the SEQ function should act. For our purposes no switch is needed because we only use the standard functionality. In the first SEQ field the number 1 is generated and in all following fields it is automatically incremented by 1.

An XE field in the text would then look like this, for example:

> { XE "{SEQ "chron" } Kanzerogenitätsstudien }

The syntax of the SEQ field can be transferred unchanged to all XE fields via find/replace. For this to succeed, some preparation is required, as with the PAGE field (see above). The SEQ field is temporarily created anywhere in the document, given the name ‘chron’ and then marked and copied. Thus it is available as content of the clipboard for the further steps.

Now the _Replace_ window is opened (via <Ctrl+h>) and entered:

| Search for | Replace with |
| --- | --- |
| XE\_" | ^&^c\_ |

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#tabular-7)

_Explanation_: everything is handled analogous to the PAGE field (see above). With _Replace all_, all XE fields are equipped with the SEQ field.

It is also important here that the SEQ fields are updated via <Alt+F9> followed by <F9> so that they provide the correct numbers. If the index is now updated (in the separate index file), the result is a display as in [Figure 3](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#F3).

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.25/asset/c092e24b-d858-48b7-b0c1-a9ba20c7ee37/assets/graphic/indexer_2021_25_fig3.jpg)

Figure 3. Index with sequence numbers (generated by SEQ field) at the beginning of the entries. Here, too, it is noticeable that the entries with forced special sorting are arranged differently (in the right part of the figure)

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#F3)

Several differences are apparent compared to the PAGE field index:

d1

There is no page number before the text of an entry, but a sequence number. All entries are _arranged according to this sequence number._

d2

The entries of a page are arranged according to their occurrence and not alphabetically.

d4

The page number generated by the index function now plays an independent role: it provides additional useful information.

However, there are also four similarities with the PAGE field index:

s1

Run numbers are again sorted alphanumerically, but not numerically.

s2

Special sorts (by setting the semicolon in the XE fields) interrupt the correct ordering here as well.

s3

After the text of an entry there is again a page reference.

s4

Subentries are again in separate paragraphs.

Is there anything to clean up? If so, for what reason? Points d1 to d4 can simply be accepted as characteristic features. This also applies to point s3 (page references), which correlates directly with d4. Points s1, s2 and possibly s4 need to be corrected. (The numbering here refers to the above lists.)

### S1. _Run number sorting_

Analogous to the page-by-page sorting, leading zeros must also be introduced in the chronological sorting in order to achieve a correct arrangement. Whether one, two or more leading zeros are required now depends not on the number of pages but on the _number of entries (i.e. XE fields)_, as shown in [Table 2](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#T2).

Table 2. Insertion of leading zeros for chronological sorting

| Number of entries | Number of leading zeros | Insertion where? | Examples |
| --- | --- | --- | --- |
| < 100 | 1 | Only for single-digit numbers | 03, 08 |
| < 1,000 | 1 or 2 | For one- and two-digit numbers | 003, 025 |
| < 10,000 | 1, 2 or 3 | For one-, two- and three-digit numbers | 0003, 0025, 0654 |

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#T2)

The fixing of the SEQ fields is done analogously to the fixing of the PAGE fields (see above). Now the leading zeros can be inserted with find/replace. We consider here the case of a content document with more than 1,000 but less than 10,000 entries. The find/replace runs are as follows:

| Search for | Replace with |
| --- | --- |
| (XE\_")(<\[0-9\]\[0-9\]\[0-9\]>\_) | \\10\\2 |
| (XE\_")(<\[0-9\]\[0-9\]>\_) | \\100\\2 |
| (XE\_")(<\[0-9\]>\_) | \\1000\\2 |

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#tabular-9)

### s2. _Special sorts_

The semicolon for special sorting settings is replaced by a hash # analogous to the page-by-page sorting (see above). Again, the small detour via the highlighting must be used. After the search/replace run, the highlighting is removed again (select the entire document and choose _Highlight: no colour)._ If the index is now updated, all entries are correctly sorted by SEQ number, i.e. chronologically. The result is shown in [Figure 4](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#F4).

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.25/asset/fd04e67c-8346-4694-89c5-e857b9195dc9/assets/graphic/indexer_2021_25_fig4.jpg)

Figure 4. Continuous chronological sorting. In XE fields with special sorting, the semicolon has been replaced by a hash #. The special sort text is thus revealed in the index (run numbers 1391 and 1397)

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#F4)

### s4. _Subentries_

The fact that subentries are in separate paragraphs does not necessarily have to be cleaned up. It only becomes important when the entries are to be exported. This will be looked at in more detail in the next section.

### _Granularity: index of the previous edition_

An essential difference between chronological and page-by-page sorting results from the _granularity_ achieved. Page-wise sorting means granularity at the page level; chronological sorting means granularity at the entry level. This fine granularity becomes important, for example, if one wants to recognize how an author or indexer proceeded in creating the index of a previous edition. Word files for new editions often contain only a part of the XE fields, or no XE fields, from the previous edition. In most cases, they have been lost during editing by the author. In such cases it is helpful to generate a chronologically sorted output of the index of the previous edition based on the old Word files.

This output can be open on the screen as a PDF alongside the Word file of the new edition. The chronological arrangement of the old index terms makes it relatively easy to find the appropriate places in the new document and to re-create the missing XE fields. Although one could also view the old Word files directly with the embedded XE fields next to the new Word files on the screen, one will quickly find that this approach is more cumbersome and time-consuming because it does not provide an overview and orientation.

## Notes on page-by-page and chronological sorting

Quickly switching from alphabetical to page-by-page sorting (and vice versa), as known from dedicated indexing programs, is basically not possible with embedded indexing. But the procedures described above are – at least as long as only a single content file is considered – not complex either. The following steps take only a few minutes (all steps together) even for a large content file with several thousand entries:

1

creating a copy of the file

2

inserting the PAGE field in all XE fields

3

updating and fixing the PAGE fields

4

first output of the index (for control purposes)

5

inserting leading zeros in the XE fields

6

highlighting all XE fields and replacing the special-sort semicolon with another character, such as the hash

7

final output of the index in correct page-by-page sort order.

The same statements apply to the chronological sorting and the insertion of the SEQ field. It is important to emphasize that the ability to sort chronologically is a feature that sets Word apart from all other programs that can be used for indexing – even dedicated indexing programs.

## Export of XE fields

The chronological sorting holds a surprise, which results from the fact that in this arrangement each reference is listed individually. Let us consider the example of the two entries ‘Filtrationsrate, glomeläre’ and ‘First-pass-Effekt’, which can be found on several pages of a book. In the alphabetical arrangement, the page numbers are listed one after the other, separated by commas, as shown in [Figure 5](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#F5). In contrast, in the chronological arrangement, each find location is presented individually ([Figure 6](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#F6)).

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.25/asset/e112f0fc-bdbc-40fa-b691-065c7ce459fc/assets/graphic/indexer_2021_25_fig5.jpg)

Figure 5. Usual representation in alphabetical sorting: multiple find locations are arranged one after the other, separated by commas. Everything is in a single paragraph

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#F5)

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.25/asset/cae2d2bc-c78b-4ef2-87e8-6d29b8f4636b/assets/graphic/indexer_2021_25_fig6.jpg)

Figure 6. Separate presentation of the find locations

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#F6)

Here, as noted in the previous section (point s4), only the fact that the subentries are in separate paragraphs is disturbing. However, clean-up can again be done quickly in the XE fields of the content document.

The distinguishing feature of subentries or sub-subentries in the XE fields is the colon. The goal is to disable the colon’s function. The deactivation can be achieved by prefixing it with a backslash via substitution (i.e. \\: ). The targeted search for the XE field colons is done analogously to the search for the semicolon described above. That is, the detour via highlighting is taken again. After these search/replace runs, the index appears as in [Figure 7](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#F7).

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.25/asset/edd26644-29ee-4dd5-8ac7-0778d1496603/assets/graphic/indexer_2021_25_fig7.jpg)

Figure 7. The subentries have been raised to the main entries and are now separated from them by \\:. Each paragraph contains the complete information of an entry

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#F7)

The crucial thing is that now _each index paragraph corresponds exactly to one complete index entry._ Each paragraph is now, if you will, a data record. Because of this fact, the index is ideally suited for export.

The index obtained can be further optimized so that its import into further processing programs is unproblematic. First, tabs are inserted (in the separate index file) after the number at the beginning of each paragraph (i.e. the run number) and before the page number at the end of the paragraph. This can be done by a single find/replace run (preferably pattern search). In a second find/replace run, all \\: are replaced by a tab:

|   | Search for | Replace with |
| --- | --- | --- |
| 1. | ^013(<\[0-9\]{1;4}>)\_(\*)\_\_ ((pattern search)) | ^p\\1^t\\2^t |
| 2. | \\: ((normal search)) | ^t |

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#tabular-10)

_Result:_ now there are not only data records, but even data fields, because their characteristic is separation by tabs.

Now the index can be saved as a pure (tab-delimited) text file – that would be the export. The text file can then be imported by database programs such as FileMaker, Access or SQL databases or spreadsheet programs such as Excel, as well as stand-alone indexing programs such as Cindex, Sky and Macrex. There, the index entries can be further processed as desired.

The reasons for wanting such further processing include the following:

•

The index is to be output sorted letter-by-letter (see next section).

•

The new index should no longer be updated in Word, but in a separate index program.

•

The index data created should be transferred to a publisher’s or company’s own database as _metadata_ or _controlled vocabulary._

### _Advantages of this type of export over index conversions_

The method of exporting described above can be achieved with Word’s own tools. The only prerequisite is the chronological sorting of the entries, which can be generated quickly. An outstanding feature of this export is the fact that the _complete contents of the XE fields, including the specifications for special sorting, are exported._ This information can be used in a subsequent program into which the index data have been imported, in order to set the special sorting here as well. The indicator of the imported sorting defaults is the hash #, which was built in instead of the semicolon in the XE fields (see above). In a program like Excel or Cindex, all entries containing a hash can be selected and post-processed en bloc.

Exporting embedded indexing data is basically not easy. Usually, the alphabetical index is used as a starting point. However, this does not contain any information about special-sort specifications. In addition, the paragraphs of subentries or sub-subentries lack the information to which main entries they belong. Converting such an index into a form that is understood by other programs must be done manually or with the support of tools like IndexConvert (2021). This is possible in principle, but it is much more time-consuming than the export procedure described above. However, if files with embedded XE fields are _not_ available, tools like IndexConvert offer help.

## Letter-by-letter sorting

Word, as mentioned, sorts word by word according to ISO by default. However, some publishers require a letter-by-letter sort. How can it be achieved? One solution is to export the contents of the XE fields using the procedure described in the last section, load them into Excel or a dedicated indexing program, and output them from there sorted letter by letter. This is probably the easiest way. The intention is to cover this in more detail in a future article.

The question is: is it possible to switch from one sorting type to another directly in Word? Unfortunately, this is not possible by simple means, because Word does not offer a ready-made command with which this could be accomplished (unlike stand-alone indexing programs, where such a function is part of the standard repertoire). In order to reach the goal, nevertheless, the XE fields concerned must be accessed and here a sorting preparation must be carried out by setting the semicolon. The main thing is to delete existing blanks, not directly in the entry text, of course, but in the copy of it that is inserted after the semicolon (the indicator for initiating a special sort). Blanks occur only in entries that consist of several words, so the editing effort is not very high for small indexes (a few hundred entries). For larger indexes (with e.g. several thousand entries), however, it would be desirable if Word could support the user in letter-by-letter sorting, despite the lack of a sort-switching function, in order to save manual intervention to a large extent.

Support comes from a function that one does not necessarily associate with indexing, namely from paragraph formatting or style sheets. The crucial point here is the so-called _outline levels._ By default, all heading styles in Word have outline levels: the _Heading 1_ style has outline level 1, _Heading 2_ has outline level 2, and so on. Common text style sheets have outline level 0 (also called ‘body text’). In Outline View (which is one of five possible view types in Word), it is possible to set that, for example, only the text of outline level 1 is displayed – then only the first-order headings are visible. The text of all other outline levels is hidden, but still present. If now one of the headings is selected with the mouse and moved, the entire subordinate text is moved with it. In this way, a Word document can be rearranged quickly and effectively. Authors appreciate this function very much. The trick is that headings do not necessarily have to be rearranged manually, but Word’s general sorting function can be used to rearrange them. This makes sense, for example, if the document contains encyclopedia articles that are to be arranged alphabetically (see [Greulich, 2017](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#core-R1): 363–6). If each article has a first-order heading, only these headings are displayed in the outline view and then the sort function is invoked: Menu <Start – Sort>. The Sort command is located in the ‘Paragraph’ group. A window opens ([Figure 8](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#F8)) where settings for sorting text can be made.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.25/asset/6fe87b49-a3ad-4854-b8a3-d8655ad2a39c/assets/graphic/indexer_2021_25_fig8.jpg)

Figure 8. Word sorting window

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#F8)

Text in Word is sorted by paragraphs by default, in alphabetical ascending order. The settings do not need to be changed. After selecting the OK button, the reordering of all paragraphs that can be seen (i.e. all Heading 1 paragraphs) takes place immediately. The texts attached to the heading paragraphs are dragged along in the background. If the Outline View is now exited, the complete article texts are displayed in alphabetical order. This technique of paragraph sorting can also be used for indexes.

If an index is created with Word’s index function, main entries are assigned the style _Index 1_, subentries are assigned the style _Index 2_, and so on. The aim is to sort the main entries letter by letter, dragging all subentries, sub-subentries and so on along with them. The structure of the index must be preserved. To achieve this, a new style is defined, named e.g. _index\_sort_, which is based on the _Standard_ style. The most important features are certain settings for the outline level and the font. For the outline level, a value between 1 and 9 (e.g. 5) can be selected. For the font, the attribute ‘Hidden’ is set.

The non-printable characters must be visible. If this is not the case, simply press the key combination <Ctrl-\*>.

The procedure is now as follows:

1

Search for text with the style _Index 1._

2

The found text is copied (without the paragraph marker). This places it on the clipboard.

3

Directly above the current paragraph a blank line (i.e. a new paragraph) is inserted (_Enter_ key).

4

The contents of the clipboard are pasted into the new paragraph.

5

The paragraph is assigned the style _index\_sort_ and the cursor is moved down two paragraphs by pressing <Ctrl + Arrow Down> twice.

6

These steps are done for all main entries. To avoid this taking too much time, a macro should be recorded that includes steps 1 to 5. The macro is packed into a loop, and the macro loop works through the complete index to the last main entry. Now all main entries are present twice: once with style _index\_sort_, and once with style _Index 1_ ([Figure 9](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#F9)). The important thing is the order: _Index 1_ must always come exactly after _index\_sort_ (which is ensured by using the macro).

8

The value for the level to be displayed is set to 5 ([Figure 10](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#F10)). With this, all paragraphs that are not assigned the style _index\_sort_ disappear into the background. That is, now neither the actual main entries nor the subentries, sub-subentries and so on are visible. Only the main entry paragraphs assigned the _index\_sort_ style are displayed. Find/replace runs that are executed now only affect these paragraphs, while the paragraphs that exist in the background remain unchanged.

9

All blanks are removed via search/replace (Replace All can be selected). For German indexes, the umlauts Ä, Ö, Ü, ä, ö, ü and the ß are replaced by the basic vowels a, o, u or the double letter ss.

10

Call up the sorting function (see [Figure 8](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#F8)). The entire index is automatically selected.

12

Close the Outline View. All index levels are now displayed and two features are apparent: (a) the index is now sorted letter by letter, and (b) the index structure is still in order.

13

Since the paragraphs with the style _index\_sort_ are a distraction, the display of the non-printable characters is switched off by <Ctrl-\*>. The goal is reached.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.25/asset/f85b09a3-901b-48f8-8e18-8e76d79f4de1/assets/graphic/indexer_2021_25_fig9.jpg)

Figure 9. Index after insertion of the sorting paragraphs. These can be recognized by the dotted underlining, which is the characteristic of hidden texts

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#F9)

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2021.25/asset/1666f237-80bf-46a0-9fb2-d4e2fd077fb8/assets/graphic/indexer_2021_25_fig10.jpg)

Figure 10. Outline view with level 5 selection

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2021.25#F10)

_A special feature:_ this procedure can also be used to re-sort indexes that originate from other index programs. If an index was, for example, created with InDesign, it can be copied and pasted into a new Word file. InDesign uses the names _Index Level 1, Index Level 2_ and so on for the styles of the different index levels. They are immediately available in Word as styles. In the sorting macro described above in Word (see step 6), only the name of the style has to be changed from _Index 1_ to _Index Level 1._ After the re-sort, the index can be copied and pasted back into InDesign, where it replaces the old index.

## Conclusion and outlook

This final part of the series on indexing with Word has shown how to implement page-by-page, chronological and letter-by-letter sorting with Word’s own tools. The PAGE and SEQ fields are used for this. With the help of a few search/replace runs the goal is quickly reached. Sorting letter by letter is much more abstract, because it is necessary to become familiar with topics like ‘styles’ and ‘outline function’. But even that can be mastered. Although this is less easily achieved than in dedicated indexing programs, those who do not own these programs can manage without them. It is remarkable that it is possible to export the complete contents of the XE fields on the basis of chronological sorting. Thus indexes that were started with Word can be further processed in special indexing programs or also in Excel. To supplement this series on indexing in Word, a short series on indexing with Excel is planned. The possibilities of this program have hardly been recognized and appreciated in the indexer scene so far.

## References

Greulich, W. (2017) _Dokument- und Formatvorlagen für Word 2016, 2013 und 2010_. Hamburg: tredition.

Greulich, W. (2020a) ‘Embedded indexing with Word: new light on an old topic. Part 1 – how to monitor creation of an index’, _The Indexer_ 38(2), 207–18.

Greulich, W. (2020b) ‘Embedded indexing with Word. Part 2 – editing entries and making work easier by using macros’, _The Indexer_ 38(3), 291–306.

Greulich, W. (2020c) _Indexing mit Word_. Hamburg: tredition.

Greulich, W. (2020d) ‘Embedded indexing with Word. Part 3 – shifting method and field codes for cross-references and page ranges’, _The Indexer_ 38(4), 381–98.

Greulich, W. (2021a) ‘Embedded indexing with Word. Part 4 – page reference annotations and functional ebook indexes’, _The Indexer_ 39(1), 85–100.

Greulich, W. (2021b) ‘Embedded indexing with Word. Part 5 – locators other than page numbers’, _The Indexer_ 39(2), 183–98.
