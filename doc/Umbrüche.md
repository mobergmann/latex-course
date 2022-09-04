---
layout: default
title: Umbrüche
nav_order: 4
---

# Umbrüche
Zeilenumbrüche, Seitenumbrüche, oder auch Absätzen sind recht einfach.

## Zeilenumbruch
```latex
\newline
\\
```

Du kannst den `\newline` Befehl für einen Zeilenumbruch verwenden.
Da Zeilenumbrüche allerdings sehr häufig verwendet werden, wurde ein kürzerer Befehl eingefügt: `\\`. 
Beide Ausdrücke sind equivalent.

## Absatz
```latex
\par

```

Wenn man einen Absatz erzeugen möchte, kann der `\par` Befehl benutzt werden, oder man macht es sich noch einfacher und fügt eine **Freie Zeile/ Absatz** in dem LaTeX dokument ein.

Grundsätzlich sollte man nicht zwei oder mehrere Zeilenumbrüche als Alternative zum Absatz zu benutzen.

## Seitenumbruch
```latex
\newpage
```

Seitenumbrüche werden automatisch von LaTeX gemacht, wenn der Text länger als der Platz auf der Seite ist.
Möchte man aber einen Seitenumbruch forcieren, kann der Befehl `\newpage` benutzt werden.
