# Setting up highlight color keyboard shortcuts
[see email I set to sara for updated, full version]


Command-Option-V: Apply active highlight color
Command-Option-F: Remove active highlight color
Command-Option-H: Set font color to red

[set a second color to set it to black]

Here are instructions for Mac! If you have Windows these might be in different locations. 

1. In the menubar, go to Tools -> Customize Keyboard
2. Scroll down in Categories box on the left and select All Commands
3. Under Commands (box on the right), find Highlight
4. Click the box under "Press new keyboard shortcut" and enter a shortcut combo. I used Command-Option-V - conveniently located, hard to remember. It won't let you save a key combo if it's in use for something else in Word, but it will show you what that key combo is assigned to. Some key combos don't work because they get grabbed by other programs. 
5. Click the Assign button to save your shortcut

Go back to step 3 and do it again for HighlightOff, and then for Color:. When you select Color: there's a small dropdown below the menu that you can set to red. 

Highlight (highlights selected text to whatever color is currently selected in the highlight box): Command-Option-V
HighlightOff (remove highlight from selected text): Command-Option-F
Red text: Command-Option-H

10. Now you can hit that combo and it will apply whatever the active highlight color is.
11. Go back and do it again with Highlight, and again for HighlightOff
- - - -

ctrl-option-H - highlight
ctrl-option-P - color picker
ctrl-option-H-O
option-control-A font

Next, setting up macros 


Now you have commands to:
Apply the active highlight color to a section of text
Remove the highlight from a section of text
Apply the active font color to a section of text


1. Enable the Developer toolbar
2. Click "Macros" on the Developer toolbar
3. Click "Edit" (if there's no Edit or it's grayed out you might have to record a macro first)
4. Copy the following in:

Sub SetHighlightColorBlue()
'
' SetHighlightColorBlue Macro
'
'
    Sub SetHighlightColorBlue()
'
' SetHighlightColorBlue Macro
'
'
    Options.DefaultHighlightColorIndex = wdTurquoise
End Sub
Sub SetHighlightColorYellow()
'
' SetHighlightColorYellow Macro
'
'
    Selection.EscapeKey
    Options.DefaultHighlightColorIndex = wdYellow
End Sub
Sub SetHighlightColorGreen()
'
' SetHighlightColorGreen Macro
'
'
    Options.DefaultHighlightColorIndex = wdBrightGreen
End Sub
Sub SetFontColorRed()
'
' SetFontColorRed Macro
'
'
End Sub
Sub SetHighlightColorNone()
'
' SetHighlightColorNone Macro
'
'
    Options.DefaultHighlightColorIndex = wdNoHighlight
End Sub
Sub SetFontColorDefault()
'
' SetFontColorDefault Macro
'
'
End Sub

¸¸¸¸
    Specific text: Shift + Arrow keys
    All text: Command + A
    A word to the right: Shift + Option + Right arrow
    A word to the left: Shift + Option + Left arrow
    From the cursor’s current spot to the start of the line: Command + Shift + Left arrow or Shift + Home
    From the cursor’s current spot to the end of the line: Command + Shift + Right arrow or Shift + End
    From the cursor’s current spot to the start of the paragraph: Command + Shift + Up arrow
    From the cursor’s current spot to the end of the paragraph: Command + Shift + Down arrow
    From the cursor’s current spot to the start of the document: Command + Shift + Home
    From the cursor’s current spot to the end of the document: Command + Shift + End
    From the cursor’s current spot to top of the screen: Shift + Page Up
    From the cursor’s current spot to the bottom of the screen: Shift + Page Down


WindowS: https://wordribbon.tips.net/T004269_Shortcuts_to_Change_Text_Colors.html
#z-archives/writing	