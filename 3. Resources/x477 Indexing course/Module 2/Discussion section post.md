My tips:

1. When I open Macrex on Windows 10, it opens with the bottom line—where I input a filename—offscreen and invisible. The window appears to show an input field at the top, but that field actually contained a number representing the number of characters in the full filepath. If this happens to you, move the window upward and you'll be able to see the filename at the bottom. Maximizing the window may result in the contents becoming unintelligible; if this happens, hitting a valid menu key should cause it to refresh.

2. In Macrex, when changing the placement of See also in the Merge menu, if you get an unexpected result, the options may be labeled the opposite of what you might expect (as well as the opposite of how Cindex and Sky do it):

-   To print the "See also" cross-reference to the RTF at the END of the list of the subheadings, set it to "Separate".
-   To print the "See also" cross-reference to the RTF as a SEPARATE entry that repeats the previous main heading, set its position "to End" or "to Beginning" - these both produce an identical effect for me.

(It seems like this can't possibly be right, but I've verified it repeatedly by saving the settings both locally and globally, exiting back out to the main menu, returning to the Merge menu to confirm that it set as how I remembered setting it, and then printing the index to an RTF again. Maybe it's a bug?)

3. In Macrex the Table of Authorities window indicates that you should use shift and the arrow keys to highlight, and the end key to select, but you have to use *shift*-end to select, not end. 

4. Macrex is very fast and powerful, and it will allow you to quickly, powerfully hose your settings in such a way that you can't open any index file at all. Be careful when pressing keys, go very slowly, and remember to hit F1 to back out without saving, _not_ escape. If you do what I did (and I'm not sure what I did, because it was very fast), uninstall and reinstall Macrex and redo any setting changes.

5. So that this isn't all about Macrex: in Cindex, you can reduce locator entry errors by setting it to warn or forbid you when entering an entry with an empty locator field or an invalid range of page numbers (Preferences -> Editing -> Bad Locator). You can also specify a maximum page number and a maximum allowed page range (Document -> Reference Syntax).