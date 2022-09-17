## Description

Cloze notes are very powerful for spaced repetition softwares like Anki. This add-on along with the attached note type aims to improve Anki's mechanism of displaying clozes and offers great features for better user interaction. The name of the note type the add-on uses is "**Enhanced Cloze 2.1 v2**". **Preview** ![](https://raw.githubusercontent.com/RisingOrange/anki-enhanced-cloze/master/screenshots/main_features.gif)

![](https://raw.githubusercontent.com/RisingOrange/anki-enhanced-cloze/master/screenshots/main_features_note.png) **Main features**-   Improved Mechanism of Displaying Clozes

-   Take card1 for example.

-   All c1 clozes (let me call them "genuine cloze" for this card) will be red.
-   All other clozes (let me call them "pseudo cloze" for this card), eg. c2, c3 will be blue.

-   On the front of the card, all clozes (genuine or pseudo) will be shown as their hint (if one exists) or empty.
-   You can show the answer of every cloze (genuine or pseudo) by clicking it.
-   This means you can think about a genuize cloze and check the answer one by one without getting hints from pseudo-clozes and genuine clozes after it.

-   Handy Keyboard And Touchscreen Shortcut

You can ...-   uncover genuine clozes one by one using the keyboard shortcut [J] (conifgurable) or by touching the left border of the card
-   uncover pseudo clozes one by one using the keyboard shortcut [N] (conifgurable) or by touching the right border of the card
-   toggle all genuine clozes using the keyboard shortcut [Shift+J] (conifgurable) border
-   toggle all pseudo clozes using the keyboard shortcut [Shift+N] (conifgurable) border
-   This makes uncovering clozes super convenient, no matter whether it's on a computer using the keyboard or on a mobile phone.
-   You can edit the shortcut keys by editing the configuration section of the note type (top of the front card template).

-   Auto Scroll To The Relevant Cloze

-   The card will scroll to the first genuine cloze at the very beginning.
-   When you use shortcut to uncover clozes one by one, if the next cloze is out of view (common situation on mobile phones with small screen), the card will automatically scroll to it. Super fluent experience of answering cards. This behaviour can be turned off (by editing the configuration section of the note type)

-   Can Be Used In No-Cloze Basic Mode

-   It is also Ok to go without clozes using this note type. (Note: Creating such notes only works on Anki Desktop, not on mobile!) Just type the question in the Content field and the answer in the Note field. The Note field, as answer, will be hidden on the front of the card and shown on the back of the card, just like with the Basic note type.
-   Anki won't warn you that no clozes are found.

-   "Normal" clozes

-   If you want a cloze to alway be displayed when it's a pseudo cloze, prepend the answer with a #-sign like this: {{c1::#some text}}.

**Usage**

-   In the editor select the "Enhanced Cloze 2.1 v2" note type
-   The content field is the only necessary field that you have to write something into. Other fields are optional.
-   Write down anything in the Content field, whether with clozes like {{c1::abc}} or not, the add-on will process the note intelligently.
-   For you information, you may create clozes with increasing numbers like {{c1::aa}} {{c2::bb}} with Ctrl+Shift+C and clozes with the same number like {{c1::aa}} {{c1::bb}}.
-   I'd recommend you to group several closely related pieces of information to use the same cloze number and review them together on a card for convenience; use different cloze numbers to turn you informative note into several cards to maximize review efficiency.
-   When you have [Edit Field During Review (Cloze)](https://ankiweb.net/shared/info/385888438) installed, Ctrl+Click fields to edit them

**Configuration** ![](https://raw.githubusercontent.com/RisingOrange/anki-enhanced-cloze/master/screenshots/configuration.png) If the underline options do not work, try using "Reset Enhanced Clozes css to default" from the Tools menu of the main window. **Credits** The 2022-02-04 - update was inspired by [TRIAEIOU's](https://github.com/TRIAEIOU) [Flexible Cloze](https://ankiweb.net/shared/info/1632356464) add-on This add-on is a fork of [https://github.com/ijgnd/anki-enhanced-cloze](https://github.com/ijgnd/anki-enhanced-cloze) by [ijgnd](https://github.com/TRIAEIOU) Previous version of the add-on by Arthur Milchior: [https://github.com/Arthur-Milchior/anki-enhanced-cloze](https://github.com/Arthur-Milchior/anki-enhanced-cloze) Previous version of the add-on by LuZhe610: [https://ankiweb.net/shared/info/873439973](https://ankiweb.net/shared/info/873439973) **Problems, Bugs, Errors, Improvements** If you have an idea for an improvement or encounter a problem please create an issue on [Github](https://github.com/RisingOrange/anki-enhanced-cloze/issues). **Support my work** If this add-on is useful to you please consider buying me a coffee: [![](https://i.imgur.com/9bfEVZ6.jpg)](https://www.buymeacoffee.com/jakubfidler) **Changelog** 2022-07-21: Changes to actions in the Tools menu. 2022-07-19: Fixed the Extra field. To get the fixed note type you have to go to Tools -> "Reset Enhanced Cloze note type to default" on the main Anki window 2022-07-15: Added option to reveal pseudo-clozes by default 2022-04-22: Added compatibility with [Edit Field During Review (Cloze)](https://ankiweb.net/shared/info/385888438) add-on, added option to not underline revealed clozes 2022-03-18: Fixes for iOS, other fixes 2022-03-15: Added option to disable hints for pseudo clozes (showHintsForPseudoClozes on the front card template) 2022-03-15: Added option to reset note type to default version (it's in the main window in the Tools menu) 2022-02-09: Added option to disable scroll animation (animateScroll = false). Force a full sync to get the new version to your mobile device (Preferences -> Network -> Check "On next sync force changes in one direction") 2022-02-09: Shortcuts now reveal only one cloze even if multiple clozes have the same id 2022-02-04: Big update: Adding/Editing on mobile works now, removed unnecessary fields (Thanks to TRIAEIOU for showing how to do this), added shortcuts, some fixes 2022-01-28: Update for Anki 2.1.50 2021-10-20: Fixed incompatibility with [Field during Review (Cloze)](https://ankiweb.net/shared/info/385888438) (cards work now, but you still can't edit them during review) 2021-10-15: Fixed images not working in the Content field (again, because the first fix was not complete) 2021-9-31: Fixed touches not working properly on iOS devices 2021-9-22: Fixed mathjax not working inside of clozes 2021-9-16: Fixed images not working in first field 2021-9-14: Fixed incompatibilty with Popup-dictionary 2021-9-08: Fixed no-cloze-mode on Ankidroid (force sync collection from desktop to phone to make it work) + clozes start at 1 when using the shortcut in the editor 2021-8-28: Add-on doesn't overwrite changes of the note type now (you can add new fields, just don't delete the existing ones) 2021-8-26: You can now have 50 clozes on one note if you want to (before this update the limit was 20) 2021-8-19: Added backwards compatibilty down to Anki 2.1.28 2021-8-18: Fixed no cloze mode 2021-8-17: Fixed "type in the answer" message showing up on mobile, Fixed "show one cloze" hotkey action

## Download

As add-ons are programs downloaded from the internet, they are potentially malicious. You should only download add-ons you trust.

Supported Anki versions:

-   2.1.28-2.1.54+ (Updated 2022-07-21)

To download this add-on, please copy and paste the following code into Anki 2.1:

1990296174

If you were linked to this page from the internet, please open Anki on your computer, go to the Tools menu and then Add-ons>Browse & Install to paste in the code.