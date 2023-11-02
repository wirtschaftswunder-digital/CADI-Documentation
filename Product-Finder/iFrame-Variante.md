---
layout: default
title: iFrame Code Variante
parent: Einbindung
nav_order: 5
---

# iFrame Code Variante
{: .no_toc }

## Inhaltsverzeichnis
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Einbindung

Kopieren Sie den folgenden Code-Abschnitt auf Ihre Webseite. Der Product Finder wird in das <div>-Element mit der ID "product-finder-wrapper" eingebettet.

### Code

```html
<!-- Product Finder START -->
<iframe id="product-finder-iframe"
        src="https://pf.camps.digital?pf-anbieter-id=INSERT_ANBIETER_ID_HERE&pf-host-id=INSERT_HOST_ID_HERE" width="100%"
        frameborder="0" scrolling="no" style="overflow: visible;"></iframe>
<script>
    const productFinderIframe = document.getElementById("product-finder-iframe")
    window.onmessage = function (e) {
        if (String(e.data).startsWith("resize-pf")) productFinderIframe.setAttribute("height", e.data.split(":")[1])
    };
</script>
<!-- Product Finder END -->
```

### Einrichtung

1. Ersetzen Sie `INSERT_ANBIETER_ID_HERE` durch Ihre Anbieter-ID.
2. Ersetzen Sie `INSERT_HOST_ID_HERE` durch Ihre Host-ID.

---

## Einstellungen

### Filter deaktivieren

Verwenden Sie den URL-Parameter `pf-disabled-filters` auf der `src` URL des `<iframe id="product-finder-iframe" ...>`-Tags, um Filter zu deaktivieren. Fügen Sie alle Filternamen ein, die Sie deaktivieren möchten, durch Kommas getrennt.
Filternamen: `holiday`, `ageGroup`, `region`, `eventType`, `tag`\
**Beispiel:** `pf-disabled-filters=region,eventType`

### Destinationen deaktivieren

Verwenden Sie den URL-Parameter `pf-disabled-destinations` auf der `src` URL des `<iframe id="product-finder-iframe" ...>`-Tags, um Destinationen zu deaktivieren. Fügen Sie alle Destination-IDs ein, die Sie aus dem Product Finder ausschließen möchten, durch Kommas getrennt.\
**Beispiel:** `pf-disabled-destinations=49,242`

### Individuelle Farbe des Designs

Verwenden Sie den URL-Parameter `pf-theme-color` auf der `src` URL des `<iframe id="product-finder-iframe" ...>`-Tags, um Ihre individuelle Farbe zu verwenden. Wenn Sie diesen URL-Parameter verwenden, wird die benutzerdefinierte Farbe und ihre automatisch generierten Schattierungen verwendet.

{: .note-title}
> Wichtig
>
> Die Farbe muss ein Hex-Wert sein (wie `#1490FB`)!

### Individuelle Subdomain

Verwenden Sie den URL-Parameter `pf-subdomain` auf der `src` URL des `<iframe id="product-finder-iframe" ...>`-Tags, um eine Subdomain auszuwählen. Der Standardwert, der verwendet wird, wenn `pf-subdomain` nicht vorhanden ist, ist `my`.

### Hintergrundbild des Filtermenüs

Verwenden Sie den URL-Parameter `pf-filter-background-img-src` auf der `src` URL des `<iframe id="product-finder-iframe" ...>`-Tags, um ein individuelles Hintergrundbild zu verwenden.

### Spalten ausblenden

Verwenden Sie den URL-Parameter `pf-hidden-columns` auf der `src` URL des `<iframe id="product-finder-iframe" ...>`-Tags, um Spalten auszublenden. Fügen Sie alle Spaltennamen ein, die Sie ausblenden möchten, durch Kommas getrennt.
Spaltennamen: `title`, `date`, `duration`, `price`, `availability`, `booking`\
**Beispiel:** `pf-hidden-columns=title,price`

### Lite-Modus

Der Lite-Modus ermöglicht es, alle Produkte zu verbergen, bis der Benutzer auf die Schaltfläche "Ergebnisse anzeigen" klickt. Mit dem Lite-Modus ist der Product Finder kompakt, wenn der Benutzer die Seite lädt.
Verwenden Sie den URL-Parameter `pf-lite-mode` auf der `src` URL des `<iframe id="product-finder-iframe" ...>`-Tags, um den Lite-Modus zu aktivieren. Der Lite-Modus ist standardmäßig deaktiviert und nur aktiv, wenn `pf-lite-mode` auf `true` gesetzt ist.

### Mehrere Anbieter-IDs

Verwenden Sie den URL-Parameter `pf-anbieter-id` auf der `src` URL des `<iframe id="product-finder-iframe" ...>`-Tags, um alle Anbieter-IDs in der gewünschten Reihenfolge aufzulisten. Trennen Sie die IDs mit einem Komma.\
**Beispiel:** `pf-anbieter-id=1,2,5`

### Destinationen oben anpinnen / Ihre Destinationen anordnen:

Liste Sie die Destination-IDs, die Sie zuerst anzeigen möchten, in der gewünschten Reihenfolge auf, indem Sie den URL-Parameter `pf-pin-destinations` auf der `src` URL des `<iframe id="product-finder-iframe" ...>` verwenden.\
**Beispiel:** `pf-pin-destinations=49,242` wird die Destination 49 als erstes, 242 als zweites und dann den Rest anzeigen.

### Spracheinstellung

Verwenden Sie den URL-Parameter `pf-locale` auf der `src` URL des `<iframe id="product-finder-iframe" ...>`-Tags, um die Sprache zu wählen. Anzeigen/Ausblenden des Sprachmenüs: `pf-show-language-menu=true` / `pf-show-language-menu=false` (Standard: `true`).