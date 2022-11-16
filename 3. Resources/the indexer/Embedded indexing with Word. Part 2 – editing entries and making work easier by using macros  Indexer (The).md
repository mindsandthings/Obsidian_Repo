---
created: 2022-11-14T09:19:09 (UTC -08:00)
tags: []
source: https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.27
author: Walter Greulich
---

# Embedded indexing with Word. Part 2 – editing entries and making work easier by using macros | Indexer (The)

> ## Excerpt
> In this second article in a series on the under-exploited potential for using Microsoft Word as a tool for embedded indexing, the focus is on editing entries and using macros while the index is bei...

---
Publication: The Indexer: The International Journal of Indexing

Volume 38, Number 3

## Abstract

In this second article in a series on the under-exploited potential for using Microsoft Word as a tool for embedded indexing, the focus is on editing entries and using macros while the index is being created. This article covers the index entry window, XE fields, separate document templates and exported UI files. It also includes step-by-step instructions for using macros. The first article in the series can be found in _The Indexer_ **38**(2), 207–18.

The first article in this series described techniques that are essential for creating an embedded index in Word effectively and of good quality. The recommendation was that separate files should be used for both the index and the cross-references to avoid mixing them with the document content. This separation allows permanent observation of the growth of the index, and the cross-references can be easily created and checked. This second article in the series introduces further techniques without which effective indexing in Word is not possible. The focus is on the entries themselves, and on their creation, but especially on their editing.

## Index entry window: what for, what not

All programs that allow embedded indexing (see e.g. Schroeder, [2003](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.27#core-R6)) offer a dialog window for creating an entry. In FrameMaker, this is called the Index Marker window, in QuarkXpress it is the Index Palette and in InDesign and Word it is the Index Entry window.

The index entry window in Word appears as soon as a piece of text is selected and the key combination <Alt-Shift-x> is pressed. The marked text is then visible in the Main Entry (or Main Heading) box. If the ‘Mark’ button is now clicked, an XE field is inserted at the position in the text where the cursor flashes, the contents of which correspond to the marked text piece. An index entry has been created. The whole process takes only a few moments.

Optionally, some actions can be performed in the Index Entry window: an initial editing of the entry, the input of a subheading, the creation of a cross-reference, the specification of a page range based on a bookmark and the specification of a formatted display of the page number. The fact that the ‘Mark all’ button can be used to specify all occurrences of the marked text piece as index entries should only be mentioned here for the sake of completeness – this function does _not_ play a role in creating a good index.

The appearance of the XE field can be seen in [Figure 1](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.27#F1). If none of the optional actions mentioned above have taken place, the field looks rather unspectacular: it contains the field name and the entry. To create an XE field by hand, many more steps are required: Ribbon \[Insert – Building Blocks – Field\], then select the XE field. After OK, an empty XE field is inserted into the text. The property ‘field’ is in the special curly brackets. If these are simply typed in as characters, there is no field property. In the manually created XE field, the entry can now be entered or pasted from the clipboard. The Index Entry window eliminates the need to manually create the XE field by simplifying the process; its main purpose is to allow the user to easily create the XE field with the correct syntax.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2020.27/asset/5e484681-66d8-4a19-b43e-2f86aa6d3cc2/assets/graphic/indexer_2020_27_fig1.jpg)

Figure 1. Index Entry window (left) and associated XE field (right)

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.27#F1)

The Index Entry window is not modal, which means that it remains open after an index entry has been defined. If a further text passage is marked, the Index Entry window only needs to be clicked briefly and the marked text appears in this window and can be specified as the next entry. Not having to key in the text is a great relief.

However, it becomes cumbersome if one wants to use the optional possibilities offered in the Index Entry window. It is not possible to edit an entry correctly here. This is one reason why add-ons like DEXembed or WordEmbed were developed. However, editing entries is already possible using Word’s own functions, i.e. without add-ons. (But that does not mean that the add-ons are useless!) First of all, I give some recommendations based on my long experience with embedded indexing in Word.

•

First recommendation:

◦

The marking of an index-relevant piece of text does not have to be exact; several words or half-sentences can also be marked. This information automatically runs into the Main Entry box when one clicks on the Index Entry window (after which, of course, post-processing is necessary). This allows rapid progress, especially when combined with the next recommendations.

•

Second recommendation:

◦

All editing of an entry should be done in the XE field. In other words, editing or formatting of the entry text in the Index Entry window should be avoided as much as possible. The boxes offered for the subheading, the cross-reference and the page range should not be used. The page number formats (bold and italics) can be selected if necessary, as this is no effort.

◦

The XE field created in this way contains the raw main-heading information. The main heading can be adjusted quickly in the XE field (much faster than in the Index Entry window), either manually or with macro support. A subheading is entered in the XE field or created from parts of the information in the main heading, with macro support (described below). It is better to create a cross-reference in a separate Word file from the beginning (see Greulich, [2020](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.27#core-R3)). To perform these editing steps, the syntax of the XE field must be understood (see [Figure 2](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.27#F2)).

•

Third recommendation:

◦

Page-range information should not be created with bookmarks. In a future article a different method will be described.

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2020.27/asset/a0493e51-1402-4c1d-a1ac-0636b2364035/assets/graphic/indexer_2020_27_fig2.jpg)

Figure 2. Syntax of the XE field

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.27#F2)

## XE field: syntax, properties and possibilities

To edit XE fields, they must be visible. This is guaranteed if the view showing the so-called non-printable characters is switched on. If this view is switched off, the contents of all XE fields disappear into the background. With the key combination <Ctrl-\*> the content of the XE fields can be shown or hidden. Hiding the non-printable characters is important for those work steps where the XE fields should not disturb the layout and the Word document should look exactly as it will be printed (WYSIWYG).

This is where Word differs from other word-processing and layout programs (such as OpenOffice, LibreOffice, InDesign, FrameMaker and Quark XPress), because they offer an Index Entry _window_ for creating and editing entries, but no Index Entry _field_, and where an entry is located in the document text, only an icon is displayed, which itself does not take up any space. The _Index Entry field_ in Word, the XE field, has the great advantage that its contents are accessible to the usual editing functions.

Which usual editing functions are involved?

•

For example, most text formatting font mark-up can be done. This includes italics, bold and bold/italic, superscripts and subscripts, underlining and strikethrough, increasing or decreasing character spacing, etc. Basically everything offered in the Fonts window works, with one exception: Hidden. The contents of the XE field, as noted above, have this label by default, and it cannot be assigned a second time (i.e. ‘superimposed’).

•

Insertion options

◦

Since Word is a modern program, all Unicode characters can be inserted into the XE field. But that is not all: if desired, even mathematical formulae or images can be inserted into an XE field. The sorting of such graphical elements can be influenced as usual with the semicolon (see [Figure 2](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.27#F2)). And, of course, these elements are displayed in the index. This is useful for special characters that are only available as graphics.

◦

More importantly, other fields can be inserted into the XE field, which leads to an enormous expansion of the possibilities for displaying entries, sorting entries and further processing of the index with downstream programs (especially towards ebook output). This field-in-field method will be covered in a later article.

•

Another important editing feature of the XE field is the applicability of the search/replace function of Word. This even makes a RegEx search possible, as with a dedicated indexing program. It should be borne in mind that Word should not be seen as in competition with any dedicated indexing program, but on the other hand, anyone indexing with Word (for whatever reason), can use the same advanced techniques of a RegEx search as with dedicated indexing programs.

•

As with all other fields in Word, the contents of the XE field can be changed in the same way as normal text. This applies not only to the entry text, but also to the switches. In other words, all tools that Word provides for manipulating text are applicable to the XE fields. And the most powerful tool Word has to offer is the macro function. This provides a level of variability and flexibility that no other word-processing or layout program, or dedicated indexing program, can match – unless the indexer uses e.g. the languages C++, Perl or Python (i.e. acts as a ‘real’ programmer). The good thing about Word is that the macros that can help with indexing can first be recorded and then easily adapted. It is not necessary to become a programmer to do that.

The use of macros is one of the crucial points for creating a good index with Word, with an acceptable level of effort. The other points mentioned above (like search/replace) are also important and will be duly described in a subsequent article. Here the focus is on macros.

### Editing the XE field: accessing macros by shortcuts or ribbon customization

By its very nature, Word does not provide functions that support the editing of index entries. But the program is so general and so powerful that users can create the most important functions needed for indexing themselves. For this purpose, macros are recorded and post-processed with the Visual Basic Editor (see [Appendix](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.27#appendix)). This is not as difficult as it might at first appear. Comprehensible introductions to the use of macros are provided by, for example, Gonzalez et al. ([2005](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.27#core-R1)), Tyson ([2010](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.27#core-R7)), Lyon ([2012](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.27#core-R4)) and Greulich ([2017](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.27#core-R2)). When the macros are ready, it must also be ensured that they can be executed at the push of a button, as described below. First, the editing functions themselves should be considered.

Typical index editing functions are, for example, doubling an entry or flipping main heading and subheading. If such editing steps had to be done manually, embedded indexing with Word would be extremely tedious. The required macros are recorded and then adjusted as mentioned above. In addition, it must be ensured that they can be accessed easily. In principle, this could be done by assigning keyboard shortcuts to each macro, but keyboard shortcuts have one big disadvantage: it is necessary to remember them. Therefore, the recommendation is to add mouse functions to shortcuts. Ultimately, it boils down to customizing the ribbon so that all the functions for editing XE fields are presented and accessed here. The process of customization is described in Microsoft ([2020](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.27#core-R5)) and in any of the better Word manuals (e.g. Tyson, [2010](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.27#core-R7); Greulich, [2017](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.27#core-R2)). [Figure 3](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.27#F3) shows the result of such an adaptation: the tab ‘Indexing with Word’ (as named by me) contains the editing commands in a clearly arranged form. (Shown here is a section with some particularly important functions; I use several more functions in practice.)

![](https://www.liverpooluniversitypress.co.uk/cms/10.3828/indexer.2020.27/asset/eada75ef-333f-4503-9b28-f8f931e5893d/assets/graphic/indexer_2020_27_fig3.jpg)

Figure 3. Customized ribbon (in Word 2010 and newer) with self-defined functions that can be important for indexing. Because of the width of the image, it is displayed in two parts.

[Open in viewer](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.27#F3)

What do the individual functions do? They are explained here in the order in which they appear on the customized ribbon. Some of the underlying macro codes can be found in the [Appendix](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.27#appendix).

•

_Empty XE field_ inserts an empty XE field into which one can type immediately: { XE “ }. This function is only needed if the standard way of creating an XE field has not been chosen. The standard way consists (as described above) of marking a text passage, calling up the Index Entry window with the key combination <Alt-Shift-x> and specifying the entry with OK. Since the window remains open, further entries can be specified simply by marking and briefly clicking on the window.

•

_Selected text_ ➛ _SH_ If a part of a main heading (MH) is marked in the XE field, the marked text is cut and inserted as subheading (SH) in the same XE field. For example, if an adjective and the noun following it are defined as an index entry:

{ XE ‘adjective substantive’ }

If the adjective is now marked (by double clicking on it) in the XE field and the macro is triggered, then the entry will have the form

{ XE ‘substantive:adjective’ }

That is, the noun is the main heading, the adjective the subheading (both are separated by a colon). In many indexes, this order of adjective and noun is preferred. In some indexes it is useful to have both variants as entries, by double posting. The doubling of an XE field is brought about by the next macro.

•

_Doubling of entry_ The cursor must blink in the XE field to be duplicated, then this function places a second XE field with identical contents behind it. The second XE field can then be edited as desired. If a part of the MH in the duplicated XE field is to function as SH, this can be done with the macro ‘Selected text ➛ SH’ (see above).

•

_Flipping MH–SH_ Sometimes an XE field already exists that contains both a main heading and a subheading (indicated by the colon), as, for example, { XE ‘alignment:page numbers’ }.To create the inversion of this entry { XE ‘page numbers:alignment’ }, first the entry is doubled (with the macro ‘Doubling of entry’), then the macro ‘Flipping MH–SH’ is used. The swapping is done when the cursor is somewhere in the MH or SH of the duplicated field. In effect, the macro rounds off the double posting.

•

_Exchanging brackets_ If an XE field that contains an abbreviation and its written-out variant has been doubled, this macro can be used to swap the contents. For example, ‘Visual Basic for Applications (VBA)’ becomes ‘VBA (Visual Basic for Applications)’ or vice versa. The cursor must be located somewhere in the MH or SH of the duplicated field.

•

_Search for selected text_ can generally be used to search for a selected text piece. The principle is to mark text and trigger the macro, and then the next occurrence of the text piece is automatically searched for. The macro can also be used for cross-reference checking. This is done in the separate cross-reference file (see Greulich, [2020](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.27#core-R3)), in which an instance of the index is also located below the cross-reference list or table. First a reference target word is marked in a cross-reference. The macro then searches for this word in the index. A suitable main entry must be found. If the search yields nothing, the word selection should be changed (e.g. shortened) and the macro executed again; if no result is obtained, the cross-reference is probably incorrect.

•

_Go to_ jumps to the next XE field. The macro should only be used when the XE fields are visible (the display can be switched on and off using <Ctrl-\*>). This can be used to jump from one XE field to the next, to perform a systematic check, for example.

•

_HL next XE_ The cursor must be in front of an XE field. The macro jumps to the next XE field and highlights it in yellow (HL: Highlighting). This coloured highlighting is a great help for the permanent observation of the growth of an index, as discussed in Greulich ([2020](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.27#core-R3)).

•

_HL all XE_ All XE fields are highlighted in yellow.

•

_Del HL of next XE_ The macro jumps to the next XE field and removes the highlighting (Del: Deletion). This can be used to remove an individual highlighting or, for example, to systematically remove the highlighting of the last indexing session so that highlighting can be started afresh for the new session.

•

_Del HL of all XE_ The highlighting of all XE fields in the document is removed.

•

_Number of XE_ jumps to the beginning of the document and starts counting the XE fields from here. When the macro has reached the end of the document, a message window opens, in which the total number of XE fields is given. This is useful to keep the size of the index within the planned range or to quickly answer the client’s question about how many entries have already been completed.

•

_Group ‘DEL XE’_ (delete XE field):

◦

_Single XE, cursor in front_ deletes the following XE field.

◦

_Single XE, cursor inside_ deletes the XE field in which the cursor is currently located.

◦

_All XE_ deletes all XE fields in the document.

•

_Insert index_ eliminates the need for insertion via the ‘References’ tab and directly inserts the index, i.e. the index _field_. If the formatting of the index is not satisfactory, it can be changed with the corresponding switches of the index field (in the field view: <Alt-F9>). The switches of the index field (attention: not of the XE field!) will be discussed in a future article.

•

_Group ‘Views on document’_ The different views of a Word document (print layout, draft and Web layout) are Word-internal functions, which have been additionally arranged as buttons on this menu tab to make them more easily accessible.

## Separate document template and exportedUI file

If no other method is selected, the macros are saved in the Normal.dotm by default after recording. When Word is closed, it is important to answer ‘Yes’ to the question whether to save the changes to Normal.dotm. The customization of the ribbon is automatically saved in the background of Word. It does not depend on the currently open file, but remains as long as it is not changed. Each time Word is started, the customized ribbon is available.

Storage of macros and ribbon customizations in Normal.dotm, however, has some disadvantages. The most important is that they cannot easily be exchanged with other people, because a Normal.dotm is person-related and cannot be passed on. It is therefore recommended that the macros are stored in a separate document template, which could be called ‘indexing.dotm’, for example. When doing this, it is important to think about what to do with the ribbon customization, because it is closely related to the macros of the respective document template. The solution is to save the ribbon customization in a separate file. For non-programmers, Word offers the exportedUI format (UI: user interface), but only for Windows users. Mac users have to make do with the ribbon customization linked to Normal.dotm. Under Windows, the ribbon customization can be saved to a location on the hard disk with the ‘Export’ command (e.g. as an ‘indexing.exportedUI’ file). The ribbon can then be reset to work with the usual tabs and buttons and the customization added as needed by importing the indexing.exportedUI file. In order to access the macros in the associated document template (indexing.dotm), the document in which the commands of the ribbon are to be used must be deliberately linked to the document template. In other words, editing an index in Word requires two ‘background files’: the exportedUI file and the macro template. This sounds complicated, but is part of the daily routine of most freelance editors who edit manuscripts for publishers, for example. Authors are also used to linking templates to their documents. Adding the exportedUI file and connecting it to the macro template is done in a few minutes and can last as long (days or weeks) as needed.<sup>1</sup>

### Editing XE fields until an index exists

Once these prerequisites have been met, click on the ‘Indexing with Word’ tab and start editing XE fields. Experience shows that the macros ‘Selected text ➛ SH’, ‘Doubling of entry’, ‘Flipping MH–SH’, ‘Exchanging brackets’ and ‘Search for selected text’ are especially helpful for saving time and avoiding mistakes. During practical work the indexer should always switch between defining and editing an entry. At the same time, how a new entry fits into the index can be observed in the separate index file. If necessary, it can be edited immediately. The correction of the entry text is done manually, as in a dedicated indexing program. For larger changes to an entry, the macro functions are used, and several entries can be edited at once using the search/replace function. The function that perhaps saves most effort is to duplicate an XE field: with a single click a new XE field with editable content is available. If these points are observed, an index is created relatively easily, which can be proofread at the end as usual.

The corrections must be made in the XE fields, which is of course more time-consuming than in a dedicated indexing program. The determining step is to find the affected XE field. As described in the first article of the series (Greulich, [2020](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.27#core-R3)), this can be done quite successfully with the go-to function. In this way (observing the index in a separate file, using the macro functions as well as the go-to function) a reasonable or even good index can be created in an acceptable time. In any case, this procedure is much more effective than the standard method described in the usual Word manuals or even in Schroeder ([2003](https://www.liverpooluniversitypress.co.uk/doi/10.3828/indexer.2020.27#core-R6)).

## Conclusion and outlook

As with many other Word-related topics (e.g. document templates and styles), Microsoft only lays the foundation and leaves it to users to fully exploit the given potential. The on-board tools provided by Word are sufficient to optimize important steps of the indexing process. Subsequent articles will show some convincing examples of this.

## Footnote

1

The exportedUI file (indexing.exportedUI) described here, and the corresponding macro template (indexing.dotm), are available from the author ([walter.greulich@publishing-and-more.de](mailto:walter.greulich@publishing-and-more.de)) for interested readers, for continued work in the spirit of open-source software development.

## Appendix: step-by-step instructions for recording and editing some important macros

The first article in this series described how to record the highlighting macro. Here the method for recording four more macros is described: ‘Selected text ➛ SH’, ‘Doubling of entry’, ‘Flipping MH–SH’ and ‘Search for selected text’. The codes of the first three macros were created by recording alone (i.e. they did not need to be edited). With the ‘Search for selected text’ macro, the code had to be slightly post-processed.

By following these step-by-step instructions, readers can create these macros themselves. To apply the macros, either use keyboard shortcuts or store the macros as buttons on the ribbon and then call them up with the mouse.

**_Selected text ➛ SH_**

First, the text within the XE field that is to become the SH is marked. Now the recording starts.

1.

The marked text is cut out (using <Ctrl-x>).

2.

The residual text is marked from the current cursor position up to the quotation mark using the function ‘Extend text selection’; i.e. <F8-’> is entered.

3.

Terminate the function via ESC.

4.

Press the right arrow key once to place the cursor to the right of the quotation mark.

5.

Press the left arrow key once to place the cursor to the left of the quotation mark.

6.

Enter the colon. The cursor is automatically positioned to the right of the colon.

7.

Insert the contents of the clipboard: <Ctrl-v>.

Steps 2 to 5 are used to place the cursor directly in front of the quotation mark that closes the entry text. The search function could also be used for this, but it is easier with the ‘Extend text selection’ function.

Associated macro code:

Sub selection\_as\_sh()

‘

‘Macro for moving the selected text to the subheading; macro was recorded and not post-processed; text must be selected in the XE field

‘

Selection.Cut

Selection.Extend

Selection.Extend Character:=‘‘‘‘

Selection.EscapeKey

Selection.MoveRight Unit:=wdCharacter, Count:=1

Selection.MoveLeft Unit:=wdCharacter, Count:=1

Selection.TypeText Text:=‘:’

Selection.PasteAndFormat (wdFormatOriginalFormatting)

End Sub

**_Doubling of entry_**

First of all, the XE field to be duplicated must be clicked once. Now the recording starts.

1.

The search function is called – <Ctrl-H> – then click on the search tab.

2.

Enter: ^d XE (^d is the code for ‘Search by field’; the text XE tells Word to search for the XE field).

3.

Set the search to be performed upwards (‘Up’).

4.

Select ‘Find next’. Now the search is executed and the complete XE field is highlighted.

5.

Copy the marked field – <Ctrl-c>.

6.

Move the cursor one position to the right with the arrow key; this deselects the field and the cursor is positioned directly to the right of the field.

7.

Insert the contents of the clipboard – <Ctrl-v>. This inserts an identical XE field next to the existing field.

Associated macro code:

Sub entry\_doubling()

‘

‘ Macro for doubling an entry; macro was recorded and not post-processed; the cursor must be in the XE field

‘

Selection.Find.ClearFormatting

With Selection.Find

.Text = ‘^d XE’

.Replacement.Text = ‘‘

.Forward = False

.Wrap = wdFindAsk

.Format = False

.MatchCase = False

.MatchWholeWord = False

.MatchWildcards = False

.MatchSoundsLike = False

.MatchAllWordForms = False

End With

Selection.Find.Execute

Selection.Copy

Selection.MoveRight Unit:=wdCharacter, Count:=1

Selection.PasteAndFormat (wdFormatOriginalFormatting)

End Sub

**_Flipping MH–SH_**

First click into the XE field. Now the recording starts.

1.

The search function is called – <Ctrl-h> – then click on the search tab.

2.

Enter: XE ‘ (explanation: this will search for XE followed by a space and a quotation mark).

3.

Set the search to be performed upwards.

4.

Select ‘Find next’. Now the search is executed and the letter combination XE ‘ is highlighted.

5.

Move the cursor one position to the right with the arrow key. This deselects the search and the cursor is positioned to the right of the quotation mark.

6.

Call the ‘Extend text selection’ function (F8) and mark up to the colon, i.e. press : once.

7.

Deactivate the ‘Extend text selection’ function by pressing the ESC key. The marking of the text remains intact.

8.

Cut the marked text – <Ctrl-x>. The MH, including the colon, will be cut out.

9.

Call ‘Extend text selection’ (F8) and mark up to the quotation mark, i.e. key in ‘. This marks the entry text between the two quotation marks (including the closing quotation mark).

10.

Switch off the ‘Extend text selection’ function by pressing the ESC key. However, the marking of the text is retained.

11.

Move the cursor one position to the right with the arrow key. The marking is then removed and the cursor is positioned to the right of the quotation mark.

12.

Move the cursor one position to the left with the arrow key. The cursor is now to the left of the quotation mark.

13.

Enter a colon; the cursor is automatically positioned to the right of the colon.

14.

Insert contents of the clipboard <Ctrl-v>. Thus the original MH is behind the colon; i.e. it has now become SH.

15.

Delete the colon at the end with the backspace key.

Associated macro code:

Sub mh\_sh\_swap()

‘

‘ Macro to swap MH and SH; macro was recorded and not post-processed; the cursor must be in the XE field

‘

Selection.Find.ClearFormatting

With Selection.Find

.Text = ‘XE ‘‘‘

.Replacement.Text = ‘‘

.Forward = False

.Wrap = wdFindAsk

.Format = False

.MatchCase = False

.MatchWholeWord = False

.MatchWildcards = False

.MatchSoundsLike = False

.MatchAllWordForms = False

End With

Selection.Find.Execute

Selection.MoveRight Unit:=wdCharacter, Count:=1

Selection.Extend

Selection.Extend Character:=‘:’

Selection.EscapeKey

Selection.Cut

Selection.Extend

Selection.Extend Character:=‘‘‘‘

Selection.EscapeKey

Selection.MoveRight Unit:=wdCharacter, Count:=1

Selection.MoveLeft Unit:=wdCharacter, Count:=1

Selection.TypeText Text:=‘:’

Selection.PasteAndFormat (wdFormatOriginalFormatting)

Selection.TypeBackspace

End Sub

**Search for selected text**

The macro is used to search for selected text; this can be document text, text within an XE field or text in the index. In the separate cross-reference file it can be used to check the cross-references. First a text passage is marked, then the recording starts.

1.

The search function is called up – <Ctrl-h> – then click on the search tab.

2.

The marked text is automatically in the search field.

3.

The next occurrence of the text is searched for with ‘Find next’; search direction: downwards (‘Down’).

It can be seen that the macro code explicitly contains the letter sequence of the marked text passage. This means that when the macro is applied, the system searches exclusively for this text. However, to write a macro that searches for any marked text, the search text must be replaced with a variable. The variable must be declared at the beginning of the code, which is always done with the ‘Dim’ statement. For example, ‘Dim a’ is used to declare the variable ‘a’, where ‘a’ was freely chosen., It is also possible to declare a variable ‘b’: ‘Dim b’, or a variable ‘test’: ‘Dim test’ (or any other). Afterwards, it is necessary to specify what the variable is to be ‘loaded’ with, i.e. which value it is to take. In this case, the value of the selected text should be assigned to it, i.e:

> a = Selection.Text.

In the code for the search, the recorded text must now be replaced by the variable a:

> .Text = a.

All other code remains unchanged.

Associated macro code:

Sub search\_selected\_text()

‘

‘ Macro to search for selected text; can be document text or index text to search the index, e.g. to check a cross-reference; macro was recorded, then the variable a was inserted manually; text must be marked

‘

Dim a ‘declaration of variable

a = Selection.Text ‘variable is assigned the value of the selected text

Selection.Find.ClearFormatting

With Selection.Find

.Text = a ‘variable is used here

.Replacement.Text = ‘‘

.Forward = True

.Wrap = wdFindAsk

.Format = False

.MatchCase = False

.MatchWholeWord = False

.MatchWildcards = False

.MatchSoundsLike = False

.MatchAllWordForms = False

End With

Selection.Find.Execute

End Sub

In order to see the code of macros and to be able to edit it if necessary, the VBA editor must be opened, as follows.

**Opening the VBA editor**

The easiest way to open the VBA editor is via the ‘Developer’ tab, where the button ‘Macros’ is found on the left. A click on it opens the Macros dialog window. If a macro is selected here and then the ‘Edit’ button is pressed, the VBA editor opens and the user lands directly in the code of the selected macro and can edit it. Another rapid way to open the VBA editor is to use the shortcut <Alt-F11>.

The Developer tab is hidden by default. It can be shown by selecting the item ‘Customize Ribbon’ via the Word options. In the right-hand pane, the check mark for Developer must be set.

## References

Gonzalez, J. P., Meister, C., Ozgur, S., Dilworth, B., Altink, N. and Troy, A. (2005) _Office VBA: macros you can use today_. Uniontown, OH: Holy Macro! Books.

Greulich, W. (2017) _Dokument- und Formatvorlagen für Word 2016, 2013 und 2010_. Hamburg: Tredition.

Greulich, W. (2020) ‘Embedded indexing with Word: new light on an old topic’, _The Indexer_ 38(2), 207–18.

Lyon, J. (2012) _Macro cookbook for Microsoft Word_. West Valley City, UT: Editorium.

Schroeder, S. (2003) _Software for indexing_. Medford, NJ: Information Today for American Society of Indexing.

Tyson, H. (2010) _Microsoft Word 2010 Bible_. Chichester: Wiley.
