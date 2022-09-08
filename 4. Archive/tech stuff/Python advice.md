# Python advice
My friends had a lot of advice, but it sounds like the bottom line is that the tutorial on the python site is very good. 

**Learning Python**

10:52 <mikecotton> the official docs at  [python.org](http://python.org/)  are pretty uniquely good
 [https://docs.python.org/3/tutorial/index.html](https://docs.python.org/3/tutorial/index.html) 

[everyone agrees to look for tutorials that are specific to Python 3, unless you'll be taking over a large existing codebase]

11:00 <steve> Learn Python the Hard Way is a well made tutorial with a few obnoxious opinions scattered throughout [Most other sources I see warn away from this one. Also it used to be a website and now it's only a book. - M]

<steve> I am expert-level in python and always happy to answer questions 

**Environments**
11:42 <brandon> enkidu: I recommend the PyCharm IDE. There's a free version. 
It catches many errors that other languages catch at compile-time, but that python only catches are run-time. You can even use optional types and it will type check your code for you. 
 [Here's a 50% discount for a Mastering PyCharm online video course: ](https://training.talkpython.fm/courses/explore_pycharm/mastering-pycharm-ide?code=6d6f0135-658e-45e9-af63-7d622ac68c99&utm_source=jetbrains_offer&utm_medium=email&utm_campaign=jetbrains_talkpython%0A) 
<steve> I would say if you already use a code editor of some kind, stick with the one you know, but if you don't have a preferred code editor, PyCharm is a fine choice for doing a little python 

12:05 <mikecotton> I hear that the everyone under 30 uses Visual Studio Code. I find this world where the kids are down with M$FT strange and terrifying. 
12:07 <steve> mikecotton: vscode is indeed very popular, but pretty much the same as all the editors the kids have been jumping around between for the past 10 years 
12:07 <steve> they're all pretty much emacs lite with a more modern UI 
**other advice**

10:56 <mikecotton> for python in general, I'd just say 'strings are just lists of characters', and 'if you aren't totally sure whether to use a list or a dict for something, use a dict' [I agree with this. - M]

11:04 <steve> to mikecotton’s starting advice, I would add: the self parameter is confusing, it confuses everyone, so if it doesn’t make sense that probably means you’re getting there 

<steve> oh, and learn list comprehensions early and use them often, they make a lot of tasks easier (by leading you to do things in a way that works out better long term) [I agree with this - M.] 

11:35 <mikecotton> oh, the sort method doesn't return anything, so if you try to do foo = bar.sort() foo will be a NoneType, not a sorted version of bar.

11:36 <mikecotton> in general, pay attention to NoneTypes, the sooner you understand them, the sooner you'll understand python.

#z-archives