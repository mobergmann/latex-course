---
layout: default
title: Struktur
nav_order: 5
---

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

Jedes Dokument muss mit einem `\documentclass{}` starten.
Danach werden alle [Pakete](./Pakete) aufgelistet, welche eingebunden werden sollen.
Als Nächstes folgt das Setzen von Variablen (diese werden z.B. benötigt für [Maketitle](./Maketitle)).<br>
Daraufhin folgt der Block `\begin{document} ... \end{document}`.
In diesem Block wird der eigentliche Text/ Inhalt des PDFs geschrieben.
