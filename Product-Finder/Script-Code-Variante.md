---
layout: default
title: Script Code Variante
parent: Product-Finder
nav_order: 4
---

# Script Code Variante
{: .no_toc }

## Inhaltsverzeichnis
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Einbindung

Kopieren Sie den folgenden Code-Abschnitt auf Ihre Webseite. Der Product Finder wird in das <div>-Element mit der ID "product-finder-wrapper" eingefügt.

### Code

```html
<!-- Product Finder START -->
<div id="product-finder-wrapper" data-product-finder-wrapper="true" data-anbieter-id="INSERT_ANBIETER_ID_HERE" data-host-id="INSERT_HOST_ID_HERE">
  <!-- Der Product Finder wird hier eingefügt -->
</div>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.6.0/jquery.min.js" integrity="sha512-894YE6QWD5I59HgZOGReFYm4dnWc1Qt5NtvYSaNcOP+u1T9qYdvdihz0PPSiiqn/+/3e7Jo4EaG7TubfWGUrMQ==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>
<script>
  (function($) {
    $(document).ready(function() {
      "use strict";
      let $productFinderWrapper = $('#product-finder-wrapper');
      if(!$productFinderWrapper.length) $productFinderWrapper = $('div[data-product-finder-wrapper="true"]');
      // Anfrage senden und die Antwort erhalten
      $productFinderWrapper.load(
        "https://pf.camps.digital/index.html",
        completeFunction
      );
      // Funktion nach Abschluss
      function completeFunction(responseText, textStatus, request) {
        if (textStatus == "error") {
          $productFinderWrapper.text(
            "Es ist ein Fehler bei Ihrer Anfrage aufgetreten: " +
            request.status +
            " " +
            request.statusText
          );
        }
      }
    });
  })(jQuery);
</script>
<!-- Product Finder END -->
```

---

### Einrichtung
1. Ersetzen Sie INSERT_ANBIETER_ID_HERE durch Ihre Anbieter-ID.
2. Ersetzen Sie INSERT_HOST_ID_HERE durch Ihre Host-ID.

---

## Einstellungen

### Filter deaktivieren

Verwenden Sie das HTML-Attribut `data-disabled-filters="..."` auf dem `<div id="product-finder-wrapper" ...>`-Tag, um Filter zu deaktivieren. Fügen Sie alle Filternamen ein, die Sie deaktivieren möchten, durch Kommas getrennt.
Filternamen: holiday, ageGroup, region, eventType, tag\
**Beispiel:** `data-disabled-filters="region, eventType"`

### Destinationen deaktivieren

Verwenden Sie das HTML-Attribut `data-disabled-destinations="..."` auf dem `<div id="product-finder-wrapper" ...>`-Tag, um Destinationen zu deaktivieren. Fügen Sie alle Destination-IDs ein, die Sie aus dem Product Finder ausschließen möchten, durch Kommas getrennt.\
**Beispiel:** `data-disabled-destinations="49, 242"`

### Individuelle Farbe des Designs

Verwenden Sie das HTML-Attribut `data-theme-color="INSERT_YOUR_HEX_THEME_COLOR_HERE"` auf dem `<div id="product-finder-wrapper" ...>`-Tag, um Ihre individuelle Farbe zu verwenden. Wenn Sie dieses HTML-Attribut verwenden, wird die benutzerdefinierte Farbe und ihre automatisch generierten Schattierungen verwendet.

{: .note-title}
> Wichtig
>
> Die Farbe muss ein Hex-Wert sein (wie `#1490FB`)!

### Individuelle Subdomain

Verwenden Sie das HTML-Attribut `data-subdomain="INSERT_YOUR_SUBDOMAIN_HERE"` auf dem `<div id="product-finder-wrapper" ...>`-Tag, um eine Subdomain auszuwählen. Der Standardwert, der verwendet wird, wenn `data-subdomain` nicht vorhanden ist, ist `my`.

### Hintergrundbild des Filtermenüs

Verwenden Sie das HTML-Attribut `data-filter-background-img-src="INSERT_YOUR_URL_HERE"` auf dem `<div id="product-finder-wrapper" ...>`-Tag, um ein individuelles Hintergrundbild zu verwenden.

### Spalten ausblenden

Verwenden Sie das HTML-Attribut `data-hidden-columns="..."` auf dem `<div id="product-finder-wrapper" ...>`-Tag, um Spalten auszublenden. Fügen Sie alle Spaltennamen ein, die Sie ausblenden möchten, durch Kommas getrennt.
Spaltennamen: **title**, **date**, **duration**, **price**, **availability**, **booking**\
**Beispiel:** `data-hidden-columns="title, price"`

### Lite-Modus

Der Lite-Modus ermöglicht es, alle Produkte zu verbergen, bis der Benutzer auf die Schaltfläche "Ergebnisse anzeigen" klickt. Mit dem Lite-Modus ist der Product Finder kompakt, wenn der Benutzer die Seite lädt.
Verwenden Sie das HTML-Attribut `data-pf-lite-mode="true"` auf dem `<div id="product-finder-wrapper" ...>`-Tag, um den Lite-Modus zu aktivieren. Der Lite-Modus ist standardmäßig deaktiviert und nur aktiv, wenn `data-pf-lite-mode` auf `true` gesetzt ist.

### Mehrere Anbieter-IDs

Listen Sie alle Anbieter-IDs in der Reihenfolge in der Sie sie präsentieren möchten durch Kommas getrennt auf, indem Sie das HTML-Attribut `data-anbieter-id="INSERT_ANBIETER_IDS_HERE` verwenden.\
**Beispiel:** `data-anbieter-id="1,2,5`.

### Destinationen oben anpinnen / Reihenfolge Ihrer Destinationen festlegen:
Listen Sie die Destination-IDs, die Sie zuerst anzeigen möchten, in der gewünschten Reihenfolge auf, indem Sie das HTML-Attribut `data-pin-destinations="INSERT_DESTINATION_IDS_HERE"` auf dem `<div id="product-finder-wrapper" ...>`-Tag verwenden.\
**Beispiel:** `data-pin-destinations="49,242"` zeigt Destination 49, 242 als zweites an und dann den Rest.

### Spracheinstellung
Verwenden Sie das HTML-Attribut `data-locale="..."` auf dem `<div id="product-finder-wrapper" ...>`-Tag, um die Sprache auszuwählen (derzeit mögliche Werte: "de", "en"). Verwenden Sie das HTML-Attribut `custom-translations-src="RELATIVE_PATH_TO_CUSTOM_TRANSLATIONS_JSON_FILE"` auf dem `<div id="product-finder-wrapper" ...>`-Tag, um die Standardtexte durch eigene zu überschreiben. Sie müssen die JSON-Datei der Übersetzungen derzeit auf Ihrer eigenen Website hosten. Anzeigen/Ausblenden des Sprachmenüs: `data-show-language-menu="true"` / `data-show-language-menu="false"` (Standard: `true`).

### Stil

#### Transparenten Hintergrund erstellen

Fügen Sie den folgenden Code zu Ihrem HTML-Code hinzu, um den Hintergrund transparent zu machen.

```html
<style>
  #product-finder {
    --main-bg: transparent !important;
  }
  
  #product-finder > div {
    box-shadow: none !important;
  }
</style>
```

#### Textfarbe ändern
```html
<style>
  #product-finder,
  #product-finder table {
    --main-text-color: IHRE_TEXTFARBE !important;
  }
</style>
```

#### Andere Farben ändern

Im Folgenden finden Sie die Standardfarben. Verwenden Sie !important, um die Farbregeln zu überschreiben.

```html
<style>
#product-finder {
  --main-bg: #edf0f3;
  --box-bg: white;
  --text-main-color: #424242;
  --selection-hover-bg-color: #e8f1ff;
  --selection-hover-text-color: black;
  --even-row-bg: rgb(250, 250, 250);
  --event-hover-color: var(--accent-color-very-light);
  --event-hover-text-color: var(--accent-color-light);
  --traffic-light-green: rgb(16, 185, 129);
  --traffic-light-yellow: rgb(245, 158, 11);
  --traffic-light-red: rgb(239, 68, 68);
  --discount-text-color: rgb(158, 158, 158);
}
```
</style>

##### Beispiel

Ändern Sie `--even-row-bg: rgb(250, 250, 250);` in `--even-row-bg: white !important;`.