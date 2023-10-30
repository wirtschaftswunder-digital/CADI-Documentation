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

## Konfiguration bei Einbindung durch WordPress-Plugin

Falls Sie die Buchungsmaske mithilfe unseres WordPress-Plugins eingebunden haben können Sie die Konfigurationseinstellungen in den Einstellungen des Plugins vornehmen.

1. Loggen Sie sich auf Ihrer WordPress Seite ein.

2. Klappen Sie das Navigationsmenü aus, sodass nicht nur die Icons zu sehen sind sondern auch die Beschriftungen.

3. Klicken sie auf **Einstellungen**. Nun sollten unter dem Menüpunkt **Einstellungen** untergeordnete Menüpunkte angezeigt werden.

4. Klicken Sie auf dem Menüpunkt **CADI Booking Mask**.

5. Nun sehen Sie die Einstellungen. Nehmen Sie Ihre Änderungen vor. In dieser [Übersicht](#übersicht-der-einstellungsmöglichkeiten) wird jede Option erklärt. Außerdem erfahren Sie welche Einstellungen erforderlich sind und welche optional sind.

7. **Wichtig:** denken Sie daran die Änderungen zu speichern, indem Sie auf den Button **Änderungen speichern** unten auf der Einstellungsseite klicken.

<div style="text-align:center">
    <img src="/img/scrennshot1.png" alt="Screenshot vom Menü Einstellungen" width="50%" />
</div>


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

## Übersicht der Einstellungsmöglichkeiten

TODO