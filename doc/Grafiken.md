---
layout: default
title: Grafiken
nav_order: 12
---

# Grafiken
Oft möchte man in seinem $\LaTeX$ Dokument Grafiken einbinden.
Wenn sie Grafiken einbinden möchten, dann müssen sie das <b>graphicx</b> Paket einbinden.

## Einfache Grafik
```latex
\includegraphics[width=0.5\textwidth]{pfad_zur_datei}
```

Wenn sie lediglich ein Bild einfügen wollen, dann geht dies über den Befehl <code>\includegraphics</code>.
Als Parameter geben sie den relativen Pfad zur Datei an.
Die Dimensionen des Bildes können sie mit den Optionen <code>width</code> und <code>height</code> setzen.
Üblich ist es eine fixe Breite anzugeben, da die Höhe automatisch angepasst wird.
Um die Breite relativ zur Seitenbreite anzugeben, benutzen sie den Befehl <code>\textwidth</code>.
Sie können die Breite "multiplizieren" mit einer Zahl, die das Vielfache der Bildbreite angibt (<code>0.5\textwidth</code> ist die hälfte der Seitenbreite).

## Grafik mit Titel
```latex
\begin{figure}[t]
\centering
\includegraphics[width=0.5\textwidth]{path/to/image}
\caption{Titel des Bildes}
\label{fig:reference name}
\end{figure}
```
