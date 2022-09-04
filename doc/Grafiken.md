---
layout: default
title: Grafiken
nav_order: 12
---

# Grafiken
```latex
\includegraphics[width=0.5\textwidth]{path/to/image}
```

Oft möchte man in seinem LaTeX Dokument Grafiken einbinden.
Dafür muss das **graphicx** Paket eingebunden werden: `\usepackage{graphicx}`.

Wenn du lediglich ein Bild einfügen möchtest, dann geht dies über den Befehl `\includegraphics[width=0.5\textwidth]{pfad_zur_datei}`.
Als Parameter wird der relative Pfad zur Datei angegeben.
Die Dimensionen des Bildes kann mit den Optionen `width` und `height` angegeben werden.
Es ist üblich eine fixe Breite anzugeben, da die Höhe automatisch angepasst wird.
Um die Breite relativ zur Seitenbreite anzugeben, benutzen man den Befehl `\textwidth`.
Die Breite kann mit einer Zahl "multipliziert" werden, somit wird dann das Vielfache der Text-/ Seitenbreite genommen (`0.5\textwidth` ist die hälfte der Text-/ Seitenbreite).


## Grafik mit Titel
```latex
\begin{figure}[t]
    \centering
    \includegraphics[width=0.5\textwidth]{path/to/image}
    \caption{Titel des Bildes}
    \label{fig:unique identifier}
\end{figure}
```

Grafiken können auch mit einem Titel und einer Referenz dargestellt werden.
Dafür kapselt man den `includegraphics` Befehl in ein `figure` Enviroment (`\begin{figure}`) und gibt danach eine `caption` und ein `label` an.

Die `caption` gibt den Titel des Bildes an, welcher unter dem Bild dann dargestellt wird.

Der `centering` Befehl macht, dass die Tabelle auf der Seite zentriert ist.

Die Option des Enviroments (im Beispiel `[t]`) gibt an, wo die Grafik platziert werden soll.
Grundsätzlich versucht LaTeX dann die Grafik dort zu platzieren.
Wenn dies aber nicht möglich ist, dann setzt LaTeX die Grafik an eine FallBack Option.
Die kann angegeben werden, indem man nach der ersten Option noch eine Zweite angibt (z.B. `tb`: erst am Anfang und wenn das nicht möglich ist am Ende).
Man kann LaTeX auch versuchen zu zwingen das Bild an eine gewisse Stelle zu setzen, indem man ein `!` nach der Option setzt (`h!`), aber LaTeX hat hier immer das letzte Wort und kann auch den Zwang umgehen.
- `t` steht für top, also am Anfang der Seite
- `b` steht für bottom, also am Ende der Seite
- `h` steht für here, also an der Stelle im Fließtext


[//]: # (## Subfigures)
[//]: # (TODO)
