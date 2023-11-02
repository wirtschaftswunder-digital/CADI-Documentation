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

- Wird für den Hintergrund der Sidebar verwendet

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

### `--accent-color-hover`
{: .no_toc }

> Default: `#2b44a9` <span style="background-color: #2b44a9; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

TODO

### `--primary-panel-background`
{: .no_toc }

> Default: `#fff` <span style="background-color: #fff; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

TODO

### `--secondary-panel-background`
{: .no_toc }

> Default: `var(--gray-1)` <span style="background-color: #f3f5f7; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

TODO

### `--person-background-color`
{: .no_toc }

> Default: `#fff` <span style="background-color: #fff; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

TODO

### `--person-outline-color`
{: .no_toc }

> Default: `var(--gray-2)` <span style="background-color: #9aa9c1; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

TODO

### `--validation-error-color`
{: .no_toc }

> Default: `#dc2626` <span style="background-color: #dc2626; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

TODO

### `--validation-passed-color`
{: .no_toc }

> Default: `green` <span style="background-color: green; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

TODO

### `--booking-header-title-color`
{: .no_toc }

> Default: `var(--accent-color)` <span style="background-color: #3454d1; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

TODO

### `--booking-header-subtitle-color`
{: .no_toc }

> Default: `var(--accent-color)` <span style="background-color: #3454d1; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

TODO

### `--checkbox-color`
{: .no_toc }

> Default: `#2196f3` <span style="background-color: #2196f3; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

TODO

### `--bm-url-color`
{: .no_toc }

> Default: `#00f` <span style="background-color: #00f; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

TODO

### `--bm-drop-down-background`
{: .no_toc }

> Default: `var(--gray-1)` <span style="background-color: #f3f5f7; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 8px; box-shadow: 0 1px 2px rgba(0,0,0,0.12), 0 3px 10px rgba(0,0,0,0.08);"></span>

TODO


---

## Beispiel: Anpassung des Farbschemas

TODO