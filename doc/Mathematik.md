---
layout: default
title: Mathematik
nav_order: 9
---

# Mathematik

## Einfache Syntax
Damit sie Formeln, oder Rechnungen in $$ \LaTeX $$ schreiben können müssen sie diese lediglich mit <code>$</code> Zeichen ummanteln.
Wenn sie etwas in dieser Schreibweise schreiben, wird dies Mathe-Modus genannt.<br>
Wollen sie z.B. <code>a+b=c</code> darstellen, dann schreiben sie <code>$a+b=c$</code> (das ergibt $a+b=c$).

### Index
```latex
a_1
```

Wenn sie ein Index verwenden wollen, dann können sie dies mit dem <code>_</code> zeichen erreichen: <code>$a_1$</code> wird zu $a_1$.


Möchten sie einen Index machen, welcher mehr als ein Zeichen umfasst, so können sie den Index mit geschweiften Klammern gruppieren: <code>$a_{2a}$</code> wird zu $a_{2a}$.

Es ist möglich fast allen Symbolen einen Index zu geben, sogar mehrfache Indexierungen sind möglich: <code>$a_1_2$</code> wird zu $a_{1_2}$.

### Potenzen
```latex
a^b
```

Um Potenzen darzustellen, können sie einfach die Basis konkatenieren mit dem <code>^</code> Zeichen gefolgt von der Potenz.


Möchten sie eine Potenz aus mehreren Zeichen machen, dann müssen sie diese in geschweiften klammern schreiben: <code>$a^{bc}$</code> wird zu $a^{bc}$.

Wollen sie eine mehrfache Potenz darstellen, dann umklammern sie immer die tiefste Potenz: <code>$a^{b^c}$</code> wird zu $a^{b^c}$.

### Brüche
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
