---
layout: default
title: Escape
nav_order: 3
---

# Symbole escapen
```latex
\& \% \$ \# \_ \{ \}
```

In dem vorherigen Kapitel haben wir das `%` Zeichen als Kommentar kennengelernt.
Dieses Zeichen macht es sehr einfach Kommentare zu verfassen, möchte man aber wirklich ein `%` Zeichen schreiben, dann muss man das Zeichen erst escapen.
Es gibt mehrere Zeichen, die in LaTeX eine Bedeutung haben. Diese müssen alle Escaped werden.

In der Regel escapen wir einfach, indem wir ein `\` vor dem gewünschten Zeichen setzen.
Z.B. wenn wir ein `%` escapen wollen, dann machen wir daraus einfach `\%`.

Manche Symbole haben aber, wenn sie escaped werden auch eine Bedeutung.
Dafür gibt es dann die folgenden Befehle:
- `\textasciitilde` ergibt `~`
- `\textasciicircum` ergibt `ˆ`
- `\textbackslash` ergibt `\`
