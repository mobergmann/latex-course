---
layout: default
title: Packete
nav_order: 7
---

# Pakete einbinden
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
