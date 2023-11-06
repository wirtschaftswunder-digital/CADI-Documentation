---
layout: default
title: Aufruf der Buchungsmaske
parent: Buchungsmaske
nav_order: 3
---

# Aufruf der Buchungsmaske
{: .no_toc }

## Inhaltsverzeichnis
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Einleitung

Damit die Buchungsmaske geladen werden kann und die Buchungen richtig verarbeitet werden können müssen beim Aufruf der Buchungsmaske ein paar URL Parameter gesetzt werden.

---

## Beispiel

Nehmen wir an, ein Anbieter hat die Buchungsmaske auf der Seite `https://example.com/buchung` eingebunden.

*Bei folgenden Eigenschaften:*
- Er möchte die Buchungsmaske für Destination mit der ID **260** und den Termin mit der ID **29222** verlinken
- Die Kennung des Vendor ist **Dev-Demo**
- Die Buchungsmaske soll standartmaßgig auf Deutsch (**de**) dargestellt werden.

*Wäre der korrekte URL zur Buchungsmaske:*\
`https://example.com/buchung/?destination_id=260&termin_id=29222&vendor=Dev-Demo&host=&extern=true&locale=de#/`

---

## URL Parameter der Buchungsmaske

### `destination_id`

Dieser Parameter gibt an welche Destination in der Buchungsmaske dargestellt werden soll. Geben Sie hier die ID der betreffenden Destination an.

### `termin_id`

Dieser Parameter gibt an welcher Termin in der Buchungsmaske dargestellt werden soll. Geben Sie hier die ID des betreffenden Termins an.

### `vendor`

Diese Parameter gibt an auf welchen Vendor die Buchungen zurückzuführen sind. Geben Sie hier die Kennung des jeweiligen Vendors an.

Die Sprache wird als Alpha-2 Code angegeben. Mögliche Werte können hier zum Beispiel `de` oder `en` sein.