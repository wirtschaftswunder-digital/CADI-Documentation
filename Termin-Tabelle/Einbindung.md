---
layout: default
title: Einbindung
parent: Termin Tabelle
nav_order: 2
---

# Einbindung: Termin Tabelle
{: .no_toc }

## Inhaltsverzeichnis
{: .no_toc .text-delta }

1. TOC
{:toc}

Die neue Termintabelle wird (wie die Vorgängerversion auch) als iFrame eingebunden.

## 1. iFrame einfügen

Fügen Sie folgendes iFrame auf der gewünschten Stelle Ihrer Webseite ein, um dort die Termintabelle darzustellen.

```html
<iframe
src="https://pf.camps.digital/#/termin-tabelle?destination_id=INSERT_DESTINATION_ID&pf-anbieter-id=INSERT_ANBIETER_ID&pf-subdomain=INSERT_SUBDOMAIN&pf-host-id=INSERT_HOST_ID&pf-theme-color=2a67ea&pf-bg-color=fafafa" id="tt-iframe" scrolling="no" style="width: 100%; max-width: 960px; border: none; outline: none; margin: auto; border-radius: 6px;"
></iframe>
```

## 2. iFrame durch Ihre Angaben ergänzen

Damit die Termin Tabelle geladen werden kann müssen Sie Ihre Daten im Einbindungscode einfügen.

1. Ersetzen Sie `INSERT_DESTINATION_ID` durch die ID der Destination, die Sie in der Termin Tabelle anzeigen möchten.

2. Ersetzen Sie `INSERT_ANBIETER_ID` durch Ihre Anbieter ID.

3. Ersetzen Sie `INSERT_SUBDOMAIN` durch Ihre Subdomain (z.B. `my`).

4. Ersetzen Sie `INSERT_HOST_ID` durch Ihre Host ID.

5. **(Optional)** Ersetzen Sie den Wert hinter `pf-theme-color=` (Standard ist `2a67ea`) durch Ihre eigene Brand Farbe. Diese Farbe wird in der Termin Tabelle als Akzentfarbe verwendet.

6. **(Optional)** Ersetzen Sie den Wert hinter `pf-bg-color=` (Standard ist `fafafa`) durch Ihre eigene Farbe. Diese Farbe wird in der Termin Tabelle als Hintergrundfarbe verwendet. Die Hintergrundfarbe sollte zu Ihrer Brand Farbe passen.

{: .important-title}
> Wichtig
>
> Das `#` muss beim Ersetzen der Akzentfarbe und der Hintergrundfarbe weggelassen werden (siehe [Beispiel](#beispiel)).

### Beispiel

*Für einen Anbieter mit folgenden Eigenschaften:*
- Die Termine der Destination `260` sollen in der Termin Tabelle dargestellt werden
- Seine Anbieter ID ist `123`
- Seine Host ID ist `1`
- Seine Subdomain ist `my`
- Als Akzentfarbe verwendet der Anbieter `#5dc831` <span style="background-color: #5dc831; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

*Für diesen Anbieter sieht der iFrame Code wie folgt aus:*

```html
<iframe
src="https://pf.camps.digital/#/termin-tabelle?destination_id=260&pf-anbieter-id=123&pf-subdomain=my&pf-host-id=1&pf-theme-color=5dc831&pf-bg-color=fafafa" id="tt-iframe" scrolling="no" style="width: 100%; max-width: 960px; border: none; outline: none; margin: auto; border-radius: 6px;"
></iframe>
```

## 3. Script einfügen

Da die Termin Tabelle als iFrame eingebunden ist und diese standardmäßig nicht die Größe an ihren Inhalt anpassen können, haben wir ein Script bereitgestellt das diese Aufgabe übernimmt.

Am besten fügen Sie das Script vor dem iFrame ein.

```html
<script src="https://cdn.jsdelivr.net/gh/wirtschaftswunder-digital/CADI-Loaders@latest/TerminTabelle.js"></script>
```

Das Script muss nur ein Mal pro Seite eingefügt werden (auch mehreren Termin Tabellen).
