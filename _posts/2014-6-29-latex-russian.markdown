---
layout: post
title:  "Cyrillic fonts in LaTeX on OS X"
categories: blog
---

There are two common ways of installing TeX on a Mac: full TeX Live (2.4 Gb) and BasicTeX (95 Mb), the second distribution is 24 times less. It is a subset of full TeX Live and supports most standard TeX typesetting. Cyrillic fonts package isn't included, but it's easy to install them.

To view all installed collections type `$ tlmgr info collections` in your terminal:
![TeXLive manager collections](/assets/images/latex-russian/latex-collections.png)
Two collections are recommended for cyrillic documents: `collection-fontsrecommended` (collection of widely used fonts) and `collection-langcyrillic` for cyrillc typesetting.

Now creating a document with following code will result working russian characters in output file.

{% highlight latex %}
\documentclass{article}
\usepackage{polyglossia}
\setmainlanguage{russian} 
\setotherlanguage{english}

\newfontfamily\russianfont[Script=Cyrillic]{Palatino}

\begin{document}
Привет
\begin{english}
Hello! 
\end{english}
\end{document}
{% endhighlight %}

Compile with XeLaTex and enjoy!