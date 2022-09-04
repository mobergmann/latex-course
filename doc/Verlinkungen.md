---
layout: default
title: Verlinkungen
nav_order: 9
---

# Verlinkungen
Verlinkungen in LaTeX sind in der Regel Elemente, die auf gewisse Textpassagen zeigen, sodass sie später im Text schnell wiedergefunden werden können.
In der Regel werden sie durch Zahlen im Text dargestellt, sowohl an der zu Verlinkenden Textpassagen, als auch an der zu Referenzierenden Stelle.

Wenn du möchtest, dann kannst du auch das **hyperref** Paket inkludieren: `\usepackage[unicode,hidelinks]{hyperref}`.
Dies macht, dass wenn man auf die Verlinkung klickt, das man zu der Quelle weitergeleitet wird (innerhalb des Dokuments).

## Referenzieren
```latex
\label{unique identifier}
...
\ref{unique identifier}
```

Du kannst Referenzen zu deinem Text einfügen.
Dies sind Verlinkungen, dessen Nummern von LaTeX automatisch gemanagt werden.

Um die Referenzen zu verwenden, musst du ein Label definieren: `\label{unique identifier}`.
Diesem übergibst du als Parameter einen identifier, den du nur bei dem Label verwenden darfst (aber in beliebig vielen `\ref`'s).
Dies ist ein Text, der (im besten Fall) die Referenz beschreibt.

Um dann die Referenz zu verlinken musst du den Befehl `\ref{unique identifier}` verwenden.

## Fußnoten
```latex
\footnote{text}
```

Fußnoten sind relativ selbst erklärend.
Du kannst eine Fußnote (z.B. nach einem Text) setzen, eine kleine Zahl erscheint nach dem Text und der Text in der geschweiften klammer wird am Fuße des Dokuments zu der entsprechenden Zahl dargestellt.

[//]: # (## Zitieren)
[//]: # (```latex)
[//]: # (\cite{reference})
[//]: # (```)
[//]: # ()
[//]: # (Man kann in LaTeX auch zitieren.)
[//]: # ()
[//]: # (TODO)
