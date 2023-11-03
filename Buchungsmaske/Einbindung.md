---
layout: default
title: Einbindung
parent: Buchungsmaske
nav_order: 1
---

# Einbindung der Buchungsmaske
{: .no_toc }

## Inhaltsverzeichnis
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Möglichkeit 1: WordPress-Plugin

Dieser Weg der Einbindung **funktioniert nur bei WordPress Webseiten**. Da hier für die Konfiguration der Buchungsmaske kein Eingriff in den Quellcode der Webseite notwendig ist, empfehlen wir Ihnen diese Möglichkeit, falls Sie unsere Buchungsmaske auf einer WordPress Webseite einbinden möchten.

1. **Laden Sie das Buchungsmasken WordPress Plugin herunter**
   
   [Download Plugin](https://github.com/Leon-1207/CADI-Documentation/raw/main/cadi-booking-mask.zip)

2. **Melden Sie sich in Ihrem WordPress-Dashboard an**

3. **Installation des Plugins**:

   - Klicken Sie im linken Menü auf "Plugins". 
   - Anschließend klicken Sie auf "Installieren".
   - Klicken Sie oben auf der Seite auf den Button "Plugin hochladen".
   - Klicken Sie auf "Durchsuchen" und wählen Sie die zuvor heruntergeladene .zip-Datei des Plugins aus.
   - Klicken Sie auf "Jetzt installieren".

5. **Aktivieren Sie das Plugin**:

    Nachdem das Plugin erfolgreich hochgeladen wurde, klicken Sie auf "Plugin aktivieren".

6. **Setzen Sie den *Shortcode* ein**
   
   - Durch das Plugin erkennt WordPress den *Shortcode* `[cadi_booking_mask]` und ersetzt ihn beim Laden der Seite durch die Buchungsmaske.
   - Hier können finden Sie eine detaillierte Anleitung von WordPress zum Thema Shortcodes und wie sie verwendet werden können: [Anleitung auf WordPress.com](https://wordpress.com/de/support/wordpress-editor/bloecke/shortcode-block/){:target="_blank"}
  

7. **<u>Wichtig</u>**: Konfigurieren Sie erforderliche Plugin Einstellungen
   - Damit die Buchungsmaske die Daten Ihrer Reisen laden kann, müssen Sie ein paar Einstellungen vornehmen. Auf diese Weise kann unser System Sie zuordnen und die Daten korrekt verarbeiten.
   - Im folgenden Abschnitt [Konfiguration](/CADI-Documentation/buchungsmaske/Konfiguration) wird erklärt wo Sie die Einstellungen des Plugins finden und welche erforderlich für den Betrieb der Buchungsmaske sind.

---

## Möglichkeit 2: HTML Script

Kopieren Sie den folgenden HTML Code an die Stelle Ihrer Webseite an der Sie die Buchungsmaske anzeigen möchten.

{: .important-title }
> Konfiguration erforderlich
>
> In dem hier bereitgestellten Code müssen noch Ihre anbieterspezifischen Werte verwendet werden. Unter [Konfiguration](/CADI-Documentation/buchungsmaske/Konfiguration) erfahren Sie was Sie tun müssen.

{: .note-title }
> Hinweis
>
> Bei manchen Baukastensystemen für Webseiten wie zum Beispiel WordPress kann es vorkommen, dass der Code nicht als HTML Code sondern als Text interpretiert wird.

### Einbindungscode

```html
<!-- Booking mask START -->
<div id="booking-mask-wrapper" data-api-base-url="INSERT_YOUR_VALUE_HERE" data-subdomain="INSERT_YOUR_VALUE_HERE" data-anbieter-id="INSERT_YOUR_VALUE_HERE">
  <!-- booking mask gets inserted here -->
</div>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.6.0/jquery.min.js" integrity="sha512-894YE6QWD5I59HgZOGReFYm4dnWc1Qt5NtvYSaNcOP+u1T9qYdvdihz0PPSiiqn/+/3e7Jo4EaG7TubfWGUrMQ==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>
<script>
  (function($) {
    $(document).ready(function() {
      "use strict";
      const $bookingMaskWrapper = $("#booking-mask-wrapper");
      // send the request and get the response
      $bookingMaskWrapper.load(
        "https://main.d1u2qdrqduf5v6.amplifyapp.com/index.html",
        completeFunction
      );
      // complete function
      function completeFunction(responseText, textStatus, request) {
        if (textStatus == "error") {
          $bookingMaskWrapper.text(
            "An error occurred during your request: " +
            request.status +
            " " +
            request.statusText
          );
        } else {
          function checkStickyParents() {
            let parent = document.querySelector("#side-bar-wrapper");
            if (!parent) setTimeout(checkStickyParents, 500);
            else {
              while (parent) {
                const hasOverflow = getComputedStyle(parent).overflow;
                if (hasOverflow !== "visible") {
                  parent.style.setProperty("overflow", "visible");
                }
                parent = parent.parentElement;
              }
            }
          }
          checkStickyParents();
        }
      }
    });
  })(jQuery);
</script>
<!-- Booking mask END -->
```
