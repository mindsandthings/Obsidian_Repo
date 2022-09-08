Other useful notes: 

Cindex knows that successively typed characters are part of the same heading as
long as you type them at reasonable speed; if a long interval separates keystrokes,
Cindex assumes you are starting to specify a new heading. The interval Cindex
attends to is determined by standard Mac keyboard settings. To change the interval,
use the System Preferences panel, and choose Keyboard. Adjust the “Delay
until Repeat.”

Even if you are using word-by-word or letter-by-letter alphabetizing, Cindex will ignore "the" only if it is the first word in a sub-heading. Cindex does not ignore leading articles and prepositions in main headings. If you want Cindex to ignore "The" as a leading word in a main heading, place the word to be ignored inside angle-brackets, as in <The >Wind in the Willows.

To retrieve the text of a main heading from the last-edited record and place it at the insertion point, hit CONTROL 1 (CONTROL 2 for subheading, 3 for sub-subheading, 0 for the locator field text)

You can set Cindex so that as it creates each new record
it fills the locator field with the contents of the one you last made. (preferences --> editing)

Cmd-X - new entry
Add a subheading - return
Move to locator field - tab
When done, command-return

Do not mix cross-references and page references in the same record. Instead, make two records with identical headings, one with the page references in the locator field and the other with the cross-reference(s). 

To demote a heading to a subheading, so
Working Efficiently with Records
CHAPTER 3 Adding and Editing Entries 41
that you can insert a new main heading above it, place the insertion point at the
beginning of the main heading, and hit RETURN.

To convert a heading with a modifying phrase into a heading with a subheading,
place the insertion point to the right of the comma before the modifying phrase,
hit DELETE to delete the comma, then hit RETURN. Cindex will move the modifying
phrase into a new subheading field. You can break any field (except the
locator field) by placing the insertion point where you want the break then hitting
RETURN.

You can set Cindex to check locators and warn you about (or forbid) the entry of
a record that has an empty locator field or a malformed range of page numbers
(e.g., 95-93). Choose Preferences… from the Cindex menu (Figure 8 on page 27)
and click Editing then click the appropriate button under Bad Locator.
Cindex can check that each reference you enter falls within limits that you specify.
You can specify a value that no reference may exceed, and you can specify the
greatest permitted span in a range of references. To specify limits choose Reference
Syntax... from the Document menu. The relevant settings are under Page
References.

You can attach text to a function key whenever a record is open for editing

Because you normally duplicate records as a prelude to modifying them, Cindex
displays the new record(s) so as to facilitate editing:
• If you duplicate a single record, Cindex immediately opens it for editing in the
record-entry window. Regardless of whether you subsequently modify it, the record
remains a part of the index.
• If you duplicate several records, Cindex forms a temporary “group” from them, and
displays just this group in the main document window. You can edit these records in
the normal way. “Groups of Records” on page 67 explains what groups are and how
to use them while preparing an index. To restore the display of all index records in the
main document window, choose All Records from the View menu, or click in the
toolbar.

