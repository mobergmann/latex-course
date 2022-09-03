---
layout: home
---

<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>



# Willkommen zum $$ \LaTeX $$ Kurs
Hier lernen Sie die Basics von $$ \LaTeX $$ kennen.


## Befehle
Damit $$\LaTeX$$ einen Befehl von Text unterscheiden kann, müssen diese mit einem `\` Zeichen angekündigt werden. Um z.B. einen ausgedachten Befehl `command` zu benutzen schreibt man im $$\LaTeX$$ Dokument `\command`.<br>
Damit der Befehlt allerdings weiß, auf welchen Text er sich beziehen soll, wird der Text (auch Parameter genannt) mit geschweiften Klammern (`{}`) umschlossen. Daraus ergibt sich die folgende Syntax `\command{parameter}`.<br>
Mit diesem Wissen können die meisten Befehle bereits benutzt werden, manche Befehle können allerdings auch Optionen annehmen.
Diese werden mit eckigen Klammern `[]` angekündigt: `\command[option=value, ...]{parameter}`, oder auch `\command[value, ...]{parameter}`.

- Aus `\textit{Kursiver Text}` wird: $$ \textit{Kursiver Text} $$
- Aus `\textbf{Fetter Text}` wird: $$ \textbf{Fetter Text} $$
- Aus `\underline{Unterstrichener Text}` wird: $$ \underline{Unterstrichener Text} $$


## Kommentare
```latex
% Lorem Ipsum
```

Wenn Sie etwas schreiben wollen, was nicht im PDF erscheinen soll, z.B. um Anmerkungen für Personen mit Bearbeitungsberechtigung an ihrem Projekt zum Machen, dann können sie ein Kommentar verfassen.
Kommentare beginnen mit einem `$` und alles, was darauf in der Zeile folgt, wird vom Compiler ignoriert.<br>
Wenn sie also `Hallo %Welt` schreiben, dann sehen sie im kompilierten PDF lediglich $$Hallo% Welt$$.

## Symbole escapen
```latex
\& \% \$ \# \_ \{ \}
```

Es kann vorkommen, dass sie Symbole benutzen wollen, welche in der $$ \LaTeX $$ Syntax eine Bedeutung haben.
In dem Fall kann es hilfreich sein, wenn sie diese Symbole escapen.
Dafür müssen sie vor dem Symbol ein `\` Symbol schreiben.<br>
Manchen escaped Symbole haben allerdings auch eine Bedeutung, dafür gibt es von $$ \LaTeX $$ vordefinierte Befehle:

- `\textasciitilde` ergibt `~`
- `\textasciicircum` ergibt `ˆ`
- `\textbackslash` ergibt `\`


## Umbrüche
Das Einfügen von Zeilenumbrüchen, Seitenumbrüchen, oder auch Absätzen ist recht einfach.

### Zeilenumbruch

```latex
\newline
\\
```

Sie können den `\newline` Befehl für einen Zeilenumbruch verwenden, da Zeilenumbrüche allerdings sehr häufig verwendet werden wurde ein kürzerer Befehl eingefügt: `\\`. Beide Ausdrücke sind equivalent.

### Seitenumbruch
```latex
\newpage
```

Um eine neue Seite zu beginnen, können sie den `\newpage` Befehl benutzen.

### Absatz
```latex
\par
```

Wenn sie einen Absatz erzeugen wollen, dann können sie `\par` benutzen, oder aber sie lassen in Ihrem Source Code eine Zeile frei (machen ein Absatz).


## Grundlegende Dokumenten Struktur
```latex
\documentclass{article}
\usepackage[utf8]{inputenc}

\title{Beispiel}
\author{Max Mustermann}
\date{August 2021}

\begin{document}

\maketitle

\end{document}
```

Jedes Dokument muss mit `\documentclass{}` starten.
Danach werden alle Pakete aufgelistet, welche sie einbinden möchten (siehe <ref href="packtes"/>) und als Nächstes folgt das Setzen von Variablen (diese werden z.B. benötigt für Maketitle).<br>
Daraufhin folgt der Block `\begin{document} ... \end{document}`.
In diesem Block schreiben sie den Inhalt ihrer PDFs.


## Dokumentenklasse
```latex
\documentclass[option1, option2]{class_name}
```

In dem Beispiel aus Kapitel <ref href="structure"/> wird in der ersten Zeile eine Dokumentenklasse definiert.
Zur Auswahl stehen Ihnen <i>article</i>, <i>proc</i>, <i>minimal</i>, <i>report</i>, <i>book</i>, <i>slides</i>, <i>memoir</i>, <i>letter</i> und <i>beamer</i>.
Das setzen dieser eines dieser Werte gibt dem Dokument eine Grundstruktur.
Für eine Liste der verfügbaren Werte und deren Auswirkung klicken sie bitte <a href="https://en.wikibooks.org/wiki/LaTeX/Document_Structure#Document_classes">hier</a>.
<!--TODO implement list-->

## Pakete einbinden
```latex
\usepackage[option1=value1, option2=value2]{package_name}
```

Es ist möglich in $$ \LaTeX $$ Pakete einzubinden, um gewisse Extrafunktionalitäten zu erhalten.
Dazu gibt man vor dem `\begin{document}`, aber nach dem `\documentclass{article}` den Befehl an, welcher den Compiler zum Laden des Pakets auffordert.
Die grundlegende Syntax für den Befehl ist `\usepackage{package_name}`.<br>
Es kann vorkommen, dass ein Paket Optionen verlangt, oder Sie einer der verfügbaren Optionen des Pakets wahrnehmen möchten.
Dafür müssen sie die Optionen-Syntax anwenden.
Ein solches Paket haben sie bereits kennengelernt: *inputenc*, `\usepackage[utf8]{inputenc}`.
Das Paket sorgt dafür, dass unter anderem Umlaute erkannt und verwendet werden können, bzw. alle Zeichen aus dem UTF-8 Datensatz (dies umfasst auch Indische, Chinesische, … Schriftzeichen).<br>
Ein beliebtes Beispiel ist die Funktionalität Grafiken einzubinden.
Hierfür müssen Sie per Befehl $$ \LaTeX $$ informieren, dass es das **graphicx** Paket einbinden soll.
Der Befehlt lautet `\usepackage{graphicx}`.

Beachten sie, dass Pakete nur vor `\begin{document}` eingebunden werden können.

Welches Packet wie eingebunden werden muss, und welche Optionen zur Verfügung stehen müssen Sie allerdings selbstständig recherchieren.


## Maketitle
```latex
\title{Beispiel}
\author{Max Mustermann}
\date{August 2021}

...

\maketitle
```


Titelblätter werden von $$ \LaTeX $$ direkt unterstützt (sie benötigen allerdings Pakete, wenn sie das Aussehen des Titelblattes anpassen wollen).
$$ \LaTeX $$ hat die vorgefertigt Funktion `\maketitle`, welche keine Parameter nimmt. Stattdessen müssen sie die Parameter selbst mit `\title{}`, `\author{}` und `\date{}` setzen.


## Mathematik in $$ \LaTeX $$

### Einfache Syntax
Damit sie Formeln, oder Rechnungen in $$ \LaTeX $$ schreiben können müssen sie diese lediglich mit <code>$</code> Zeichen ummanteln.
Wenn sie etwas in dieser Schreibweise schreiben, wird dies Mathe-Modus genannt.<br>
Wollen sie z.B. <code>a+b=c</code> darstellen, dann schreiben sie <code>$a+b=c$</code> (das ergibt $a+b=c$).

#### Index
```latex
a_1
```

Wenn sie ein Index verwenden wollen, dann können sie dies mit dem <code>_</code> zeichen erreichen: <code>$a_1$</code> wird zu $a_1$.


Möchten sie einen Index machen, welcher mehr als ein Zeichen umfasst, so können sie den Index mit geschweiften Klammern gruppieren: <code>$a_{2a}$</code> wird zu $a_{2a}$.

Es ist möglich fast allen Symbolen einen Index zu geben, sogar mehrfache Indexierungen sind möglich: <code>$a_1_2$</code> wird zu $a_{1_2}$.

#### Potenzen
```latex
a^b
```

Um Potenzen darzustellen, können sie einfach die Basis konkatenieren mit dem <code>^</code> Zeichen gefolgt von der Potenz.


Möchten sie eine Potenz aus mehreren Zeichen machen, dann müssen sie diese in geschweiften klammern schreiben: <code>$a^{bc}$</code> wird zu $a^{bc}$.

Wollen sie eine mehrfache Potenz darstellen, dann umklammern sie immer die tiefste Potenz: <code>$a^{b^c}$</code> wird zu $a^{b^c}$.

#### Brüche
```latex
\frac{a}{b}
```

Sie können Brüche darstellen durch den Befehl <code>$\frac{a}{b}$</code> (das ergibt $\frac{a}{b}$).<br>
Sie können auch n-fache Brüche darstellen.
Dazu schreiben sie einfach in den Zähler/ Nenner den weiteren Bruch: <code>$\frac{c}{\frac{a}{b}}$</code> ergibt $\frac{c}{\frac{a}{b}}$.

## Erweiterte Syntax
Die einfache Mathematik kann mit den Symbolen dargestellt werden, die sie auf der Tastatur schreiben können.
Wollen Sie allerdings erweiterte Symbole benutzen gibt es von $\LaTeX$ vordefinierte Befehle.
Bitte beachten Sie, dass diese Befehle <mark>nur im Mathe-Modus verwendet werden können</mark>.

### Mengen
```latex
M := \{ 1, 2, 3, 4 \}
```

Eine Menge kann recht einfach mit den Standardsymbolen dargestellt werden.

#### Mengenoperationen
```latex
\cup
\cap
\subset
```

Mengenoperationen sind ebenfalls in $\LaTeX$ definiert.


| Name               | Befehl       | Symbol          |
|--------------------|--------------|-----------------|
| Leere Menge        | `\emptyset`  | $$ \emptyset $$ |
| Mit `              | `\mid`       | $$ \mid $$      |
| Vereinigungsmenge  | `\cup`       | $$ \cup $$      |
| Schnittmenge       | `\cap`       | $$ \cap $$      |
| Differenzmenge     | `\setminus`  | $$ \setminus $$ |
| Teilmenge          | `\subset`    | $$ \subset $$   |
| Obermenge          | `\supset`    | $$ \supset $$   |
| Element            | `\in`        | $$ \in $$       |
| Nicht Element      | `\notin`     | $$ \notin $$    |


Eine Tabelle aller Mengenoperationen kann <a href="https://de.wikipedia.org/wiki/Liste_mathematischer_Symbole#Mengenlehre">hier</a> gefunden werden.


### Summe
```latex
\sum_{lower}^{upper} i
```

Summen können mit dem <code>$\sum_{i=1}^{n} i$</code> Befehl erzeugt werden.
Kombinieren sie einfach den Index als untere Grenze mit einer Potenz als obere Grenze $\sum_{i=1}^{n} i$

### Produkt
```latex
\prod_{lower}^{upper}
```

Produkte können mit dem <code>$\prod_{i=1}^{n} i$</code> Befehl erzeugt werden.
Kombinieren sie einfach den Index als untere Grenze mit einer Potenz als obere Grenze $\prod_{i=1}^{n} i$

### Integrale
```latex
\int_{lower}^{upper}
```

Integrale können mit dem <code>$\int_{i=1}^{n} i$</code> Befehl erzeugt werden.
Kombinieren sie einfach den Index als untere Grenze mit einer Potenz als obere Grenze $\prod_{i=1}^{n} i$

### Matrix
**amsmath**

```latex
\begin{pmatrix}
    a_{0,0} & a_{0,1} & a_{0,2} \\
    a_{1,0} & a_{1,1} & a_{1,2}
\end{pmatrix}
```

Um Matrizen benutzen zu können müssen sie das <b>amsmath</b> Paket laden.
Danach können sie mit dem Block <code>}\$begin{matrix} ... \end{matrix}</code> ihre Matrix definieren.
Schreiben Sie in den Block die Werte für die Matrix Zeilenweise.
Fügen Sie ans Ende einer Zeile einen Zeilenumbruch und trennen sie die Werte mit <code>&</code> Zeichen.

<p>Es gibt mehrere Arten von Matrizen:</p>
<table>
    <thead>
        <th>Name</th>
        <th>Code</th>
        <th>Ergebnis</th>
    </thead>
    <tbody>
        <tr>
            <td>Parentheses</td>
            <td><code>\begin{pmatrix}</code></td>
            <td>$\begin{pmatrix}
                    a_{0,0} & a_{0,1} & a_{0,2} \\
                    a_{1,0} & a_{1,1} & a_{1,2}
                \end{pmatrix}$</td>
        </tr>
        <tr>
            <td>Brackets</td>
            <td><code>\begin{bmatrix}</code></td>
            <td>$\begin{bmatrix}
                a_{0,0} & a_{0,1} & a_{0,2} \\
                a_{1,0} & a_{1,1} & a_{1,2}
                \end{bmatrix}$</td>
        </tr>
        <tr>
            <td>Braces</td>
            <td><code>\begin{Bmatrix}</code></td>
            <td>$\begin{Bmatrix}
                a_{0,0} & a_{0,1} & a_{0,2} \\
                a_{1,0} & a_{1,1} & a_{1,2}
                \end{Bmatrix}$</td>
        </tr>
        <tr>
            <td>Pipes</td>
            <td><code>\begin{vmatrix}</code></td>
            <td>$\begin{vmatrix}
                a_{0,0} & a_{0,1} & a_{0,2} \\
                a_{1,0} & a_{1,1} & a_{1,2}
                \end{vmatrix}$</td>
        </tr>
        <tr>
            <td>Double pipes</td>
            <td><code>\begin{Vmatrix}</code></td>
            <td>$\begin{Vmatrix}
                a_{0,0} & a_{0,1} & a_{0,2} \\
                a_{1,0} & a_{1,1} & a_{1,2}
                \end{Vmatrix}$</td>
        </tr>
    </tbody>
</table>

## Verlinkungen
### Fußnoten
```latex
\footnote{text}
```

### Zitieren
```latex
\cite{reference}
```

### Referenzieren
```latex
\label{unique ref}
...
\ref{unique ref}
```


## Grafiken und Tabellen
Oft möchte man in seinem $\LaTeX$ Dokument Grafiken oder Tabellen einbinden.

### Grafiken
Wenn sie Grafiken einbinden möchten, dann müssen sie das <b>graphicx</b> Paket einbinden.

### Einfache Grakfik
```latex
\includegraphics[width=0.5\textwidth]{pfad_zur_datei}
```

Wenn sie ledeglich ein Bild einfügen wollen, dann geht dies über den Befehl <code>\includegraphics</code>.
Als Parameter geben sie den relativen Pfad zur Datei an.
Die Dimensionen des Bildes können sie mit den Optionen <code>width</code> und <code>height</code> setzen.
Üblich ist es eine fixe Breite anzugeben, da die Höhe automatisch angepasst wird.
Um die Breite relativ zur Seitenbreite anzugeben, benutzen sie den Befehl <code>\textwidth</code>.
Sie können die Breite "multiplizieren" mit einer Zahl, die das Vielfache der Bildbreite angibt (<code>0.5\textwidth</code> ist die hälfte der Seitenbreite).


### Grafik mit Titel
```latex
\begin{figure}[t]
\centering
\includegraphics[width=0.5\textwidth]{path/to/image}
\caption{Titel des Bildes}
\label{fig:reference name}
\end{figure}
```

## Tabellen
```latex
\begin{table}[t]
    \centering
    \begin{tabular}{c|c}
        Name & Klasse \\
        Max M. & 3c \\
        Niels & 5a \\
        ... & ...
    \end{tabular}
    \caption{Titel der Tabelle}
    \label{tab:unique table reference}
\end{table}
```

<!--
### Subfigures
-->

## Modularisierung
```latex
\input{path/to/texfile}
```

Sie sollten, wenn sie große Dokumente schreiben, die Texte aufteilen in mehrere Dateien.
Dies erhöht die Lesbarkeit und Wartbarkeit des Source Codes, und wird Ihnen viel Zeit ersparen, wenn sie Texte wiederfinden möchten.
