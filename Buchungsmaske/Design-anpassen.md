---
layout: default
title: Design anpassen
parent: Buchungsmaske
nav_order: 5
---

# Design anpassen
{: .no_toc }

## Inhaltsverzeichnis
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Einleitung

Das Design der Buchungsmaske kann angepasst werden, indem das CSS überschrieben wird. Am einfachsten ist das anpassen des Farbschemas, da hierfür die CSS Variablen für die Farben angepasst werden können.

---

## Standardfarbschema

**Screenshot von der Buchungsmaske im Standardfarbschema:**

![Screenshot von der Buchungsmaske](/CADI-Documentation/img/screenshot5.png)

---

## Übersicht der verwendeten CSS Variablen

### `--gray-1`
{: .no_toc }

> Default: `#f3f5f7` <span style="background-color: #f3f5f7; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

- Hellste der drei Grautöne in der Buchungsmaske

- Wird standardmäßig für den Hintergrund der Sidebar verwendet

![Sidebar](/CADI-Documentation/img/screenshotSidebar.png)

### `--gray-2`
{: .no_toc }

> Default: `#9aa9c1` <span style="background-color: #9aa9c1; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

- Mittlerer Grauton in der Buchungsmaske

- Wird beispielsweise für sekundäre Texte genutzt

### `--gray-3`
{: .no_toc }

> Default: `#293241` <span style="background-color: #293241; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

- Dunkelster Grauton in der Buchungsmaske

- Wird standardmäßig für die [Haupttextfarbe](#text-main-color) verwendet

### `--text-main-color`
{: .no_toc }

> Default: `var(--gray-3)` <span style="background-color: var(--gray-3); width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

- Farbe der Texte in der Buchungsmaske

### `--accent-color`
{: .no_toc }

> Default: `#3454d1` <span style="background-color: #3454d1; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

- Akzentfarbe

- Wird für CTA Buttons wie zum Beispiel den Buchen-Button verwendet

{: .note-title}
> Empfehlung
>
> Wir empfehlen Ihnen hier Ihre Brandfarbe einzusetzen. Denken Sie daran auch die Abwandlung der Akzentfarbe [`--accent-color-hover`](#accent-color-hover) anzupassen, damit Ihre Buchungsmaske ein stimmiges Farbschema hat.

### `--accent-color-hover`
{: .no_toc }

> Default: `#2b44a9` <span style="background-color: #2b44a9; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

- Abwandlung der Akzentfarbe

- Wird verwendet, wenn der Mauszeige über ein Button ist.

### `--primary-panel-background`
{: .no_toc }

> Default: `#fff` <span style="background-color: #fff; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

- Hintergrundfarbe der Hauptbox

### `--secondary-panel-background`
{: .no_toc }

> Default: `var(--gray-1)` <span style="background-color: #f3f5f7; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

- Hintergrundfarbe der Sidebar

### `--person-background-color`
{: .no_toc }

> Default: `#fff` <span style="background-color: #fff; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

- Hintergrundfarbe des Containers für das Form zu einem Reisenden

### `--person-outline-color`
{: .no_toc }

> Default: `var(--gray-2)` <span style="background-color: #9aa9c1; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

- Outlines werden in dieser Farbe angezeigt

![Screenshot](/CADI-Documentation/img/screenshotOutline.png)

### `--validation-error-color`
{: .no_toc }

> Default: `#dc2626` <span style="background-color: #dc2626; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

- Farbe der Fehlermeldungen, falls die Validierung Fehler erkennt

![Screenshot](/CADI-Documentation/img/screenshotError.png)

### `--validation-passed-color`
{: .no_toc }

> Default: `green` <span style="background-color: green; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

- Füllt der Benutzer in der Buchungsmaske eine Zeile fertig aus und die Validierung erkennt kein Fehler, wird ein Haken in der Farbe `--validation-passed-color` angezeigt

![Screenshot](/CADI-Documentation/img/screenshotPassed.png)

### `--booking-header-title-color`
{: .no_toc }

> Default: `var(--accent-color)` <span style="background-color: #3454d1; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

- Textfarbe des Titles

- Der Titel wird oben im Header der Buchungsmaske angezeigt

### `--booking-header-subtitle-color`
{: .no_toc }

> Default: `var(--accent-color)` <span style="background-color: #3454d1; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

- Textfarbe des Untertitels

- Der Untertitel wird oben im Header der Buchungsmaske unter dem Titel angezeigt

### `--checkbox-color`
{: .no_toc }

> Default: `#2196f3` <span style="background-color: #2196f3; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

- Farbe aller Checkbox-Inputs in der Buchungsmaske

### `--bm-url-color`
{: .no_toc }

> Default: `#00f` <span style="background-color: #00f; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

- Links in der Buchungsmaske (z.B. zu den AGB) werden in dieser Farbe dargestellt

### `--bm-drop-down-background`
{: .no_toc }

> Default: `var(--gray-1)` <span style="background-color: #f3f5f7; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

- Hintergrundfarbe der Dropdowns

![Screenshot](/CADI-Documentation/img/screenshotDropdown.png)

---

## Beispiel: Anpassung des Farbschemas

TODO