---
layout: default
title: Befehle
nav_order: 1
---

# Befehle
Damit $$\LaTeX$$ einen Befehl von Text unterscheiden kann, müssen diese mit einem `\` Zeichen angekündigt werden. 
Um z.B. den (ausgedachten) Befehl `command` zu benutzen schreibt man im $$\LaTeX$$ Dokument `\command`.

Damit der Befehlt allerdings weiß, auf welchen Text er sich beziehen soll, wird der Text (auch Parameter genannt) mit geschweiften Klammern (`{}`) umschlossen.
Daraus ergibt sich die folgende Syntax `\command{parameter}`.

Mit diesem Wissen können die meisten Befehle bereits benutzt werden, manche Befehle können allerdings auch Optionen annehmen.
Diese werden mit eckigen Klammern `[]` angekündigt: `\command[option=value, ...]{parameter}`, oder auch `\command[value, ...]{parameter}`.

- Aus `\textit{Kursiver Text}` wird: $$ \textit{Kursiver Text} $$
- Aus `\textbf{Fetter Text}` wird: $$ \textbf{Fetter Text} $$
- Aus `\underline{Unterstrichener Text}` wird: $$ \underline{Unterstrichener Text} $$
