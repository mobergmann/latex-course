---
layout: default
title: Mathematik
nav_order: 10
---

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>


# Mathematik
LaTeX bietet viele Features, um komplizierte mathematische Formeln gut darzustellen.
Dies ist auch der Hauptgrund, warum viele LaTeX überhaupt verwenden.


## Einfache Syntax
Damit sie Formeln, oder Rechnungen in LaTeX schreiben können **müssen** sie diese mit `$` Zeichen umgeben.
Wenn sie etwas in dieser Schreibweise schreiben, wird dies Mathe-Modus genannt.<br>
Wollen sie z.B. `a+b=c` schreiben, dann schreiben sie `$a+b=c$`, das ergibt $$a+b=c$$.


### Index
```latex
a_{b}
```
$$
a_{b}
$$

Indexe können dargestellt werden, indem man an der Variable ein `_` schreibt, gefolgt von dem Index in geschweiften Klammern.

#### Index von Rechnungen
```latex
a_{b+c}
```
$$
a_{b+c}
$$

Rechnungen in Indexe können dargestellt werden, indem man einfach die Rechnung in die geschweiften Klammern schreibt.

#### Index eines Indexes
```latex
a_{b_{c}}
```
$$
a_{b_{c}}
$$

Ein Index eines Indexes, usw kann darstellt werden, indem man in den geschweiften Klammern ein weiteren Index einfügt.


### Potenzen
```latex
a^{b}
```
$$
a^{b}
$$

Potenzen können dargestellt werden, indem man die Basis gefolgt von einem `^`, wiederrum gefolgt von der Potenz in geschweiften Klammern darstellt.

#### Potenz von Rechnungen
```latex
a^{b+c}
```
$$
a^{b+c}
$$

Für eine Potenz aus mehreren Zeichen schreibt man einfach die Rechnung in die geschweiften Klammern.

#### Potenz einer Potenz
```latex
a^{b^{c}}
```
$$
a^{b^{c}}
$$

Eine Potenz einer Potenz, usw kann darstellt werden, indem man in den geschweiften Klammern eine weitere Potenz einfügt.


### Bruch
```latex
\frac{a}{b}
```
$$
\frac{a}{b}
$$

Brüche können durch den Befehl `frac` dargestellt werden.
Als ersten Parameter übergibt man den Zähler und als zweiten Parameter den Nenner.

#### N-Fache Brüche
```latex
\frac{c}{\frac{a}{b}}
```
$$
\frac{c}{\frac{a}{b}}
$$

Du kannst auch Brüche von Brüchen darstellen, usw.
Schreib dazu in den Zähler und/ oder Nenner den weiteren Bruch.


### Mengen
```latex
M := \{ 1, 2, 3, 4 \}
```
$$
M := \{ 1, 2, 3, 4 \}
$$

Eine Menge kann recht einfach mit den Standardsymbolen dargestellt werden, indem man die geschweiften Klammern [escaped](./Escape).


## Erweiterte Syntax
Die einfache Mathematik kann mit den Symbolen dargestellt werden, die man auf der Tastatur findet.
Möchte man allerdings erweiterte Symbole benutzen, gibt es von LaTeX vordefinierte Befehle.
Bitte beachten, dass diese Befehle nur **im Mathe-Modus verwendet werden können**.


### Mengenoperationen
Mengenoperationen sind ebenfalls in LaTeX definiert.

| Name              | Befehl      | Symbol          |
|-------------------|-------------|-----------------|
| Leere Menge       | `\emptyset` | $$ \emptyset $$ |
| Mit               | `\mid`      | $$ \mid $$      |
| Vereinigungsmenge | `\cup`      | $$ \cup $$      |
| Schnittmenge      | `\cap`      | $$ \cap $$      |
| Differenzmenge    | `\setminus` | $$ \setminus $$ |
| Teilmenge         | `\subset`   | $$ \subset $$   |
| Obermenge         | `\supset`   | $$ \supset $$   |
| Element           | `\in`       | $$ \in $$       |
| Nicht Element     | `\notin`    | $$ \notin $$    |

Eine Tabelle aller Mengenoperationen kann [hier](https://de.wikipedia.org/wiki/Liste_mathematischer_Symbole#Mengenlehre) gefunden werden.


### Summe
```latex
\sum_{lower}^{upper} i
```
$$
\sum_{i=1}^{n} i
$$

Summen können mit dem `sum` Befehl erzeugt werden.
Kombiniere einfach den Index als untere Grenze mit einer Potenz als obere Grenze und setze das, worauf sich die Summe bezieht, nach dem Befehl.


### Produkt
```latex
\prod_{lower}^{upper}
```
$$
\prod_{i=1}^{n} i
$$

Produkte können mit dem `prod` Befehl erzeugt werden.
Kombiniere einfach den Index als untere Grenze mit einer Potenz als obere Grenze und setze das, worauf sich das Produkt bezieht, nach dem Befehl.


### Integrale
```latex
\int_{lower}^{upper}
```
$$
\int_{i=1}^{n} i
$$

Integrale können mit dem `int` Befehl erzeugt werden.
Kombiniere einfach den Index als untere Grenze mit einer Potenz als obere Grenze und setze das, worauf sich das Integral bezieht, nach dem Befehl.


### Matrix
```latex
\begin{pmatrix}
    a_{0,0} & a_{0,1} & a_{0,2} \\
    a_{1,0} & a_{1,1} & a_{1,2}
\end{pmatrix}
```

Um Matrizen benutzen zu können muss das **amsmath** Paket geladen werden.

Danach kann mit dem Enviroment `\begin{matrix} ... \end{matrix}` eine Matrix definiert werden.
Ähnlich wie bei [Tabellen](./Tabellen) werden die Einträge durch `&` Zeichen getrennt und das Ende einer Zeile wird mit einem [Zeilenumbruch](./Umbrüche#zeilenumbruch) gekennzeichnet.

| Name         | Code              |                                            Ergebnis                                            |
|--------------|-------------------|:----------------------------------------------------------------------------------------------:|
| Parentheses  | `\begin{pmatrix}` | $$ \begin{pmatrix}a_{0,0} & a_{0,1} & a_{0,2} \\ a_{1,0} & a_{1,1} & a_{1,2} \end{pmatrix} $$  |
| Brackets     | `\begin{bmatrix}` | $$ \begin{bmatrix} a_{0,0} & a_{0,1} & a_{0,2} \\ a_{1,0} & a_{1,1} & a_{1,2} \end{bmatrix} $$ |
| Braces       | `\begin{Bmatrix}` | $$ \begin{Bmatrix} a_{0,0} & a_{0,1} & a_{0,2} \\ a_{1,0} & a_{1,1} & a_{1,2} \end{Bmatrix} $$ |
| Pipes        | `\begin{vmatrix}` | $$ \begin{vmatrix} a_{0,0} & a_{0,1} & a_{0,2} \\ a_{1,0} & a_{1,1} & a_{1,2} \end{vmatrix} $$ |
| Double pipes | `\begin{Vmatrix}` | $$ \begin{Vmatrix} a_{0,0} & a_{0,1} & a_{0,2} \\ a_{1,0} & a_{1,1} & a_{1,2} \end{Vmatrix} $$ |
