[Markdown-Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

https://github.com/gollum/gollum/issues/587
via: Tom Merrihew, Feb 21, 2014.
I was encountering an issue around capitalization with GitHub wiki anchors, and this is the top result on Google. The solution (unless this issue is still waiting to be fixed) is to use all lowercase in the anchor portion of the URL.

If you have a wiki page named Questions.md and you create heading tags ## Latest and ### Ask Your Question, working links would be like this:

From the same page

[See the latest questions](#latest)
[Ask Me Something](#ask-your-question)
From a different page

[See the latest questions](Questions#latest)
[Ask Me Something](Questions#ask-your-question)
