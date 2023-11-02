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

> Default: `#f3f5f7` <span style="background-color: #f3f5f7; width: 1em; height: 1em; display: inline-block; vertical-align: middle; border-radius: 50%; margin-left: 4px;"></span>

- Hellste der drei Grautöne in der Buchungsmaske

- Wird für den Hintergrund der Sidebar verwendet

![Sidebar](/CADI-Documentation/img/screenshotSidebar.png)

### `--gray-2`
{: .no_toc }

> Default: `#9aa9c1`

- Mittlerer Grauton in der Buchungsmaske

- Wird beispielsweise für sekundäre Texte genutzt

### `--gray-3`

> Default: `#293241`

- Dunkelster Grauton in der Buchungsmaske

- Wird standardmäßig für die [Haupttextfarbe](#text-main-color) verwendet

### `--text-main-color`

> Default: `var(--gray-3)`

- Farbe der Texte in der Buchungsmaske

### `--accent-color`

> Default: `#3454d1`

- Akzentfarbe



### `--accent-color-hover`

> Default: `#2b44a9`

TODO

### `--primary-panel-background`

> Default: `#fff`

TODO

### `--secondary-panel-background`

> Default: `var(--gray-1)`

TODO

### `--person-background-color`

> Default: `#fff`

TODO

### `--person-outline-color`

> Default: `var(--gray-2)`

TODO

### `--validation-error-color`

> Default: `#dc2626`

TODO

### `--validation-passed-color`

> Default: `green`

TODO

### `--booking-header-title-color`

> Default: `var(--accent-color)`

TODO

### `--booking-header-subtitle-color`

> Default: `var(--accent-color)`

TODO

### `--checkbox-color`

> Default: `#2196f3`

TODO

### `--bm-url-color`

> Default: `#00f`

TODO

### `--bm-drop-down-background`

> Default: `var(--gray-1)`

TODO

---

## Beispiel: Anpassung des Farbschemas

TODO