---
layout: default
title: Packete
nav_order: 7
---

# Pakete einbinden
```latex
\usepackage[option1=value1, option2=value2]{package_name}
```

Es ist möglich in LaTeX Pakete einzubinden, um gewisse Extrafunktionalitäten zu erhalten.
Dazu gibt man nach dem `\documentclass{article}`, aber noch vor dem `\begin{document}` das Paket an, welches man inkludieren möchte.
Die grundlegende Syntax für das inkludieren ist: `\usepackage{package_name}`.

Es kann vorkommen, dass ein Paket Optionen verlangt, oder du möchtest einfach eine Option angeben, die das Verhalten des Paketes nach deinen Wünschen anpasst.
Du kennst bereits (wenn du den Kapiteln folgst) ein Paket, dann Optionen annimmt: *inputenc* mit dem Befehl `\usepackage[utf8]{inputenc}`.
Das Paket sorgt dafür, dass unter anderem Umlaute erkannt und verwendet werden können, bzw. alle Zeichen aus dem UTF-8 Datensatz (dies umfasst auch Indische, Chinesische, … Schriftzeichen) und ist heutzutage der Standard.<br>

Ein beliebtes Beispiel ist die Funktionalität Grafiken einzubinden.
Hierfür müssen Sie per Befehl LaTeX informieren, dass es das **graphicx** Paket einbinden soll.
Der Befehlt lautet `\usepackage{graphicx}`.

Welches Packet wie eingebunden werden muss, und welche Optionen für das Paket zur Verfügung stehen musst du allerdings selbst in dessen Dokumentation recherchieren.
Typischerweise gibt es die Pakete, die du einbinden wirst auf der [CTAN Website](https://www.ctan.org/pkg/latex).
