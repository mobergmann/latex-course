---
layout: default
title: Befehle
nav_order: 1
---

# Befehle
```
\command[option=value, ...]{parameter}
```

Damit $$\LaTeX$$ einen Befehl von Text unterscheiden kann, müssen diese mit einem `\` Zeichen angekündigt werden. 
Um z.B. den (ausgedachten) Befehl `command` zu benutzen schreibt man im $$\LaTeX$$ Dokument `\command`.

Wenn der Befehl sich auf einen gewissen Text (oder auch auf weiteren Code) beziehen soll, dann muss der Text als Parameter dem Command übergeben werden.
Dafür muss man einfach den Text in geschweiften Klammern (`{}`) umschlossen an dem Command anhängen.
Dies resultiert dann in der folgenden Syntax `\command{parameter}`.

Mit diesem Wissen können die meisten Befehle bereits benutzt werden, manche Befehle können allerdings auch Optionen annehmen.
Diese werden mit eckigen Klammern `[]` angekündigt: `\command[option=value, ...]{parameter}`, oder auch `\command[value, ...]{parameter}`.

## Beispiele

| Eingabe                            | Ausgabe                                |
|------------------------------------|----------------------------------------|
| `\textit{Kursiver Text}`           | $$ \textit{Kursiver Text} $$           |
| `\textbf{Fetter Text}`             | $$ \textbf{Fetter Text} $$             |
| `\underline{Unterstrichener Text}` | $$ \underline{Unterstrichener Text} $$ |
