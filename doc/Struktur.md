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

Jedes Dokument muss mit `\documentclass{}` starten.
Danach werden alle Pakete aufgelistet, welche sie einbinden möchten (siehe <ref href="packtes"/>) und als Nächstes folgt das Setzen von Variablen (diese werden z.B. benötigt für Maketitle).<br>
Daraufhin folgt der Block `\begin{document} ... \end{document}`.
In diesem Block schreiben sie den Inhalt ihrer PDFs.
