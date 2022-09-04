---
layout: default
title: Tabellen
nav_order: 11
---

# Tabellen
```latex
\begin{tabular}{c|c}
    Name & Klasse \\ \hline
    Max M. & 3c \\ \hline
    Niels & 5a \\ \hline
    ... & ... \\ \hline
\end{tabular}
```

Tabellen erstellt man, indem man seine Daten formatiert in das `tabular` Enviroment (`\begin{tabular}`) schreibt.<br>
Das Enviroment nimmt als Parameter eine Menge von Buchstaben an.
Dies Codieren die Anzahl der Spalten und die Ausrichtung des Textes der Spalten.
Es können `|` zwischen den Buchstaben eingefügt werden, wodurch Trennstriche zwischen den Spalten eingefügt werden.
Diese können auch am Anfang und oder am Ende der Buchstaben stehen.<br>
Für jeden Buchstaben wird eine Spalte hinzugefügt.
Die Buchstaben an sich codieren wie der Text in der Tabelle ausgerichtet werden soll.
- `r` steht für right, der Text ist somit nach rechts ausgerichtet
- `l` steht für left, der Text ist somit nach links ausgerichtet
- `c` steht für center, der Text ist somit zentriert

Die Daten in der Tabelle werden mit `&` Zeichen voneinander getrennt.
Achte darauf, wenn du ein "&" Zeichen verwenden möchtest dies zu [escapen](./Escape).
Das Ende einer Zeile wird einem [Zeilenumbruch](./Umbrüche#zeilenumbruch) gekennzeichnet.
Wenn du Horizontale Trennlinien einfügen möchtest, dann kannst du dies durch das Einfügen von dem Befehl `\hline` erreichen.

## Tabelle mit Titel
```latex
\begin{table}[t]
    \begin{tabular}{c|c}
        Name & Klasse \\ \hline
        Max M. & 3c \\ \hline
        Niels & 5a \\ \hline
        ... & ... \\ \hline
    \end{tabular}
    \caption{Titel der Tabelle}
    \label{tab:unique table reference}
\end{table}
```

Tabellen können auch ein Titel und ein Label haben.
Dafür muss man das `tabular` Environment in ein `tabular` Enviroment kapseln.
Den Titel gibt man einfach mit dem `caption` Befehl an und ein Label mit dem `label` Befehl.
Der `centering` Befehl macht, dass die Tabelle auf der Seite zentriert ist.
