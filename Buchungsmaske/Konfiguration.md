---
layout: default
title: Konfiguration
parent: Buchungsmaske
nav_order: 2
---

# Konfiguration der Buchungsmaske
{: .no_toc }

## Inhaltsverzeichnis
{: .no_toc .text-delta }

1. TOC
{:toc}

Auf dieser Seite erfahren Sie wie Sie Ihre Buchungsmaske konfigurieren können. Voraussetzung dafür ist, dass Sie die Buchungsmaske bereits auf Ihrer Webseite eingebunden haben. Falls Sie die Buchungsmaske noch nicht auf Ihrer Webseite eingebunden haben oder sich nicht mehr sicher sind welche Art der Einbindung Sie gewählt haben folgen Sie bitte unserer [Anleitung zum Einbinden der Buchungsmaske](/CADI-Documentation/buchungsmaske/Einbindung).

---

## Konfiguration bei Einbindung durch WordPress-Plugin

Falls Sie die Buchungsmaske mit Hilfe unseres WordPress-Plugins eingebunden haben können Sie die Konfigurationseinstellungen in den Einstellungen des Plugins vornehmen.

1. Loggen Sie sich auf Ihrer WordPress Seite ein.

2. Klappen Sie das Navigationsmenü aus, sodass nicht nur die Icons zu sehen sind, sondern auch die Beschriftungen.

3. Klicken sie auf **Einstellungen**. Nun sollten unter dem Menüpunkt **Einstellungen** untergeordnete Menüpunkte angezeigt werden.

4. Klicken Sie auf dem Menüpunkt **CADI Booking Mask**.

5. Nun sehen Sie die Einstellungen. Nehmen Sie Ihre Änderungen vor. In dieser [Übersicht](#übersicht-der-einstellungsmöglichkeiten) wird jede Option erklärt. Außerdem erfahren Sie, welche Einstellungen erforderlich sind und welche optional sind.

7. **Wichtig:** denken Sie daran die Änderungen zu speichern, indem Sie auf den Button **Änderungen speichern** unten auf der Einstellungsseite klicken.

<!-- []: # BEGIN: ed8c6549bwf9
<img src="/CADI-Documentation/img/scrennshot1.png" alt="Screenshot vom Menü Einstellungen" width="50%" style="max-width: 120px" />
[]: # END: ed8c6549bwf9 -->

---

## Konfiguration bei Einbindung durch HTML Script

Falls Sie die CADI Buchungsmaske als HTML Script eingebunden haben, nehmen Sie die Einstellungen direkt im HTML Code vor. Das geschieht über HTML Attribute.

### Beispiel für ein HTML Attribut:

```html
<div data-example="true"></div>
```

In dem Beispiel hat das `<div>` Element ein HTML Attribut mit dem Schlüssel `data-example` und dem Wert `true`

{: .important }
> - Achten Sie auf die korrekte Schreibweise, auch auf Groß- und Kleinschreibung.
> - Trennen sie die Attribute durch ein Leerzeichen.
> - Jedes HTML Attribut darf nur **einmal** gesetzt werden. Um 

{: .note }
> Wenn ein HTML Attribut nicht gesetzt wird, wird die Standarteinstellung verwendet.

### HTML Attribute im Einbindungscode der Buchungsmaske

Die HTML Attribute der Buchungsmaske müssen am Anfang des [Einbindungscodes](/CADI-Documentation/buchungsmaske/Einbindung#einbindungscode) in das `<div>` Element gesetzt werden:

```html
<div id="booking-mask-wrapper" HIER_HTML_ATTRIBUTE_EINGEBEN>
```

In dieser [Übersicht](#übersicht-der-einstellungsmöglichkeiten) wird jede Option erklärt. Außerdem erfahren Sie welche Einstellungen erforderlich sind und welche optional sind.

### Beispiel

Ein Anbieter möchte die Buchungsmaske einbinden und hat folgende Eigenschaften:

- **API Base URL:** https://my.camps.digital
- **Subdomain:** my
- **Anbieter ID:** 13

Der Anfang des Einbindungscodes würde für diesen Anbieter wie folgt aussehen:

```html
<!-- Booking mask START -->
<div id="booking-mask-wrapper" data-api-base-url="https://my.camps.digital" data-subdomain="my" data-anbieter-id="13">
  <!-- booking mask gets inserted here -->
</div>
...
```

---

## Übersicht der Einstellungsmöglichkeiten

Die Konfiguration von **API Base URL**, **Anbieter ID** und **Subdomain** sind **erforderlich** für den Betrieb der Buchungsmaske. Alle weiteren Einstellungen sind optional und können auch leer- bzw. weggelassen werden.

### API Base URL

Durch den Wert *API Base Url* weiß die Buchungsmaske wo sie ihre Daten abrufen soll.

In der Regel setzt sich die URL zusammen aus `https://` + *Subdomain* + `.camps.digital`. Für einen Anbieter mit der Subdomain `my` wäre der korrekte Wert also `https://my.camps.digital`. In Sonderfällen kann die URL abweichen. In diesem Fall werden wir Sie informieren.

{: .note-title}
> Konfiguration im HTML Code
>
> Verwenden Sie das HTML Attribut `data-api-base-url`\
> **Beispiel:** `data-api-base-url="https://my.camps.digital"`


### Anbieter ID

Mittels Anbieter ID und Subdomain können wir unsere Anbieter identifizieren und die Daten korrekt verarbeiten. Bei der Anbieter ID handelt es sich um eine Zahl.

{: .note-title}
> Konfiguration im HTML Code
>
> Verwenden Sie das HTML Attribut `data-anbieter-id`\
> **Beispiel:** `data-anbieter-id="12"`


### Subdomain

Die Subdomain dient neben der [Anbieter ID](#anbieter-id) dazu den Anbieter zu identifizieren.

{: .note-title}
> Konfiguration im HTML Code
>
> Verwenden Sie das HTML Attribut `data-subdomain`\
> **Beispiel:** `data-subdomain="my"`


### URL zur Übersetzungsdatei (optional)

{: .warning-title }
> Nicht empfohlen
>
> Wir empfehlen Ihnen mit dem neuen Übersetzungseditor zur arbeiten: [mehr erfahren](/CADI-Documentation/Buchungsmaske/Texte-anspassen)

Sie können alle Texte und ihre Übersetzungen in der Buchungsmaske ändern und individuell auf Ihre Anforderungen anpassen. Wir empfehlen Ihnen dafür allerdings unsere vorgefertigte Lösung durch den [Übersetzungseditor](/CADI-Documentation/Buchungsmaske/Texte-anspassen). Falls Sie diesen nicht verwenden wollen können Sie diese Einstellung nutzen und den relativen URL zu Ihrer eigenen Übersetzungsdatei angeben.


### Angepinnte Länder (optional)

{: .new-title }
> Empfohlen
>
> Wir empfehlen Ihnen diese Einstellung zu setzen und hier die Länder anzugeben aus denen die meisten Ihrer Kunden kommen. Dadurch gestalten Sie die Buchung Ihrer Kunden angenehmer.

Sie haben die Möglichkeit in unserer Buchungsmaske häufig verwendete Länder als Favoriten zu markieren. Bei der Auswahl des Landes oder der Vorwahl werden dieser Favoriten im Drop Down Menü oben angezeigt.

![Screenshot von angepinnten Ländern](/CADI-Documentation/img/pinnedCountries.png)

Die Länder werden dabei als Alpha-2 Ländercodes (internationaler ISO 3166 Standard) angegeben. Deutschland hat beispielsweise den Code **DE** und Österreich den Code **AT**. Es können mehrere Länder als Favorit markiert werden, indem die Ländercodes durch ein Komma getrennt aufgelistet werden (zum Beispiel: `de,at,ch`). Die Reihenfolge der List bestimmt auch die Reihenfolge im Dropdown.

{: .note-title}
> Konfiguration im HTML Code
>
> Verwenden Sie das HTML Attribut `data-pinned-countries`\
> **Beispiel:** `data-pinned-countries="de,at,ch"`


### Darstellung der Buchungsmaske (optional)

Diese Einstellung bestimmt ob es eine kleine Lücke zwischen dem Hauptbereich und der Sidebar der Buchungsmaske geben soll.

{: .note-title}
> Konfiguration im HTML Code
>
> Verwenden Sie das HTML Attribut `data-split-form-boxes`. Mögliche Werte sind `true` und `false`. Der Standardwert ist `true`.\
> **Beispiel:** `data-split-form-boxes="false"`


### Version (optional)

{: .warning-title }
Achtung!

Wir empfehlen Ihnen bei dieser Einstellung den **Production Mode**. Der Development Mode kann teilweise noch nicht vollständig getestete oder experimentelle Features enthalten.


### Footer Badge Image URL	(optional)

Wenn Sie unten im Footer der Buchungsmaske ein Bild einsetzen möchten, können Sie hier die URL des Bildes einfügen.

{: .note-title}
> Konfiguration im HTML Code
>
> Verwenden Sie das HTML Attribut `data-footer-badge-img`\
> **Beispiel:** `data-footer-badge-img="https://example.com/image.jpg"`


### Footer Badge Target URL (optional)

Wenn Sie unten im Footer der Buchungsmaske ein Bild eingesetzt haben und möchten, dass der Benutzer auch auf dieses Bild klicken kann, dann können Sie hier die URL einsetzen auf die Sie verlinken möchten.

{: .note-title}
> Konfiguration im HTML Code
>
> Verwenden Sie das HTML Attribut `data-footer-badge-link`\
> **Beispiel:** `data-footer-badge-ling="https://example.com"`


### Sidebar Badge (1) Image URL (optional)

In der Sidebar der Buchungsmaske können Sie Bilder einfügen. Geben Sie hierfür hier den URL des Bildes an.

{: .note-title}
> Konfiguration im HTML Code
>
> Verwenden Sie das HTML Attribut `data-sidebar-badge-1-img`\
> **Beispiel:** `data-sidebar-badge-1-img="https://example.com/sidebar-image1.jpg"`

![Screenshot von Sidebar mit Bildern bzw. Logos](/CADI-Documentation/img/screenshot2.png)


### Sidebar Badge (1) Target URL (optional)

Klick der Benutzer auf das [Sidebar Badge (1)](#sidebar-badge-1-image-url-optional), öffnet sich ein neuer Tab, der die hier definierte URL aufruft.

{: .note-title}
> Konfiguration im HTML Code
>
> Verwenden Sie das HTML Attribut `data-sidebar-badge-2-link`\
> **Beispiel:** `data-sidebar-badge-1-link="https://example.com"`


### Sidebar Badge (2) Image URL (optional)

Falls Sie unter [Sidebar Badge (1)](#sidebar-badge-1-image-url-optional) ein weiteres Bild anzeigen möchten, können Sie hier wie bei [Sidebar Badge (1)](#sidebar-badge-1-image-url-optional) hier die Adresse des Bildes angeben.

{: .note-title}
> Konfiguration im HTML Code
>
> Verwenden Sie das HTML Attribut `data-sidebar-badge-2-img`\
> **Beispiel:** `data-sidebar-badge-2-img="https://example.com/sidebar-image2.jpg"`


### Sidebar Badge (2) Target URL (optional)

Klick der Benutzer auf das [Sidebar Badge (2)](#sidebar-badge-2-image-url-optional), öffnet sich ein neuer Tab, der die hier definierte URL aufruft.

{: .note-title}
> Konfiguration im HTML Code
>
> Verwenden Sie das HTML Attribut `data-sidebar-badge-2-link`\
> **Beispiel:** `data-sidebar-badge-2-link="https://example.com"`


## Sie können nicht auf den Quellcode der Webseite zugreifen? *Kein Problem!*

Wenn Sie die Buchungsmaske auf Ihrer Webseite mittels HTML Script eingebunden haben und nun Einstellungen ändern möchten, können wir das auch für Sie erledigen. Kontaktieren Sie uns und wir nehmen die Änderung in unsrem System vor.

{: .note-title }
> Wichtig
>
> **Subdomain** und **Anbieter ID** müssen in der Buchungsmaske bereits konfiguriert sein damit von uns vorgenommene Einstellungen geladen werden.

---

## Einstellungen auf Destinationen-Ebene

Einige Einstellungen der Buchungsmaske gelten lediglich auf Destinations-Ebene. Nutzen Sie unsere **Travel App**, um diese zu konfigurieren.